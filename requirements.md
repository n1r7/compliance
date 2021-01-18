![alt text](https://github.com/nirvanapatel/compliance/blob/master/images/Application%20Layers.png?raw=true)




Legal compliance:
1. Parse ECFR to docs
2. Split docs to sentences
3. Train byte-level tokenizer
4. Train BERT model
5. Fine tune BERT model with ECFR sentences

Classification: Text -> BERT -> Dropout -> FC -> Softmax -> Class


1. Can the model identify requirements? Use deontic logic expressions.
2. Who reviews the re




## Parse ECFR to docs
```python
import requests
from lxml import etree
import re



# Define function to load XML content
def request_content(url):
    page = requests.get(url)
    print(page)
    page_content = page.content
    return page_content


# Define functions to strip new line tags
def remove_new_lines(page_content):
    cleaned_page_content = page_content.replace(b'\n', b'')
    print("Removed new-line tags.")
    return cleaned_page_content


# Define functions to parse content with lxml
def parse_to_tree(cleaned_page_content):
    parser = etree.XMLParser()
    tree = etree.fromstring(cleaned_page_content, parser)
    print("Parse complete.")
    return tree


# Define functions to strip <I> tags so each <P> tag pulls in full
def strip_tags(tree, tags_to_strip):
    etree.strip_tags(tree, tags_to_strip)
    print("Tags removed.")
    return tree


# Define function to parse tree to list
def parse_tree_to_list(tree):
    header = str(tree.xpath('//TITLESTMT/TITLE/text()')[0])

    ECFR = []
    
    ECFR.append(header)

    chapters = tree.xpath('//DIV3')

    for chapter in chapters:
        chapter_content = chapter.xpath('.//*')
        for i in chapter_content:
            if i.text:
                ECFR.append(i.text)
            
    print("List created.")
            
    return ECFR


banking_urls = ['https://www.govinfo.gov/bulkdata/ECFR/title-12/ECFR-title12.xml', 
                'https://www.govinfo.gov/bulkdata/ECFR/title-31/ECFR-title31.xml']

banking_content = []

for url in banking_urls:
    page_content = request_content(url)
    cleaned_page_content = remove_new_lines(page_content)
    tree = parse_to_tree(cleaned_page_content)
    tags_to_strip = ['HED', 'PSPACE', 'I']
    strip_tags(tree, tags_to_strip)
    title_content = parse_tree_to_list(tree)
    
    banking_content.append(title_content)


# Inverted index datastructure for searching
import nltk
from collections import defaultdict
from nltk.stem.snowball import EnglishStemmer  # Assuming we're working with English
 
class Index:
    """ Inverted index datastructure """
 
    def __init__(self, tokenizer, stemmer=None, stopwords=None):
        """
        tokenizer   -- NLTK compatible tokenizer function
        stemmer     -- NLTK compatible stemmer 
        stopwords   -- list of ignored words
        """
        self.tokenizer = tokenizer
        self.stemmer = stemmer
        self.index = defaultdict(list)
        self.documents = {}
        self.__unique_id = 0
        if not stopwords:
            self.stopwords = set()
        else:
            self.stopwords = set(stopwords)
 
    def lookup(self, word):
        """
        Lookup a word in the index
        """
        word = word.lower()
        if self.stemmer:
            word = self.stemmer.stem(word)
 
        return [self.documents.get(id, None) for id in self.index.get(word)]
 
    def add(self, document):
        """
        Add a document string to the index
        """
        for token in [t.lower() for t in nltk.word_tokenize(document)]:
            if token in self.stopwords:
                continue
 
            if self.stemmer:
                token = self.stemmer.stem(token)
 
            if self.__unique_id not in self.index[token]:
                self.index[token].append(self.__unique_id)
 
        self.documents[self.__unique_id] = document
        self.__unique_id += 1           
 
 
index = Index(nltk.word_tokenize, 
              EnglishStemmer(), 
              nltk.corpus.stopwords.words('english'))
              

# Add sentences to index
for string in ECFR:
    index.add(string)

# Create search function
def search(search_term):
    lookup = index.lookup(search_term)
    return lookup

# Test search function
search('customer')


import pandas as pd

df = pd.DataFrame(title12)
df["Definition"] = False
df["Requirement"] = False
```

## PDF parse to sentences
```python
import sys
import io
import functools
import timeit

from pdfminer.converter import TextConverter
from pdfminer.pdfinterp import PDFPageInterpreter
from pdfminer.pdfinterp import PDFResourceManager
from pdfminer.pdfpage import PDFPage

import re

from nltk import tokenize

import pandas as pd

def extract_text(pdf_path):
    content = []
    
    resource_manager = PDFResourceManager()
    fake_file_handle = io.StringIO()
    converter = TextConverter(resource_manager, fake_file_handle)
    page_interpreter = PDFPageInterpreter(resource_manager, converter)
 
    with open(pdf_path, 'rb') as fh:
        for page in PDFPage.get_pages(fh, 
                                      caching=True,
                                      check_extractable=True):
            page_interpreter.process_page(page)
 
        text = fake_file_handle.getvalue()
 
    # close open handles
    converter.close()
    fake_file_handle.close()
 
    if text:
        return text

    content.append(text)

    
@functools.lru_cache(maxsize=128)
def sentence_tokenizer(content):
    sents = tokenize.sent_tokenize(content)
    return sents


path = 'Wolfsberg_tax.pdf'

pdf = extract_text(path)
pdf = re.sub('\x0c \d\d\d', '', pdf)
pdf = pdf.replace('\uf0d8', '')

sentences = sentence_tokenizer(pdf)
sentences

pd.set_option('display.max_colwidth',0)
df = pd.DataFrame(data=sentences)
df.head(20)

```

## FFIEC NLP
```python
import nltk
import spacy
import re

import requests
from bs4 import BeautifulSoup as bs

from collections import OrderedDict


# Read csv as list

URLS = '../data/ffiec_urls.csv'

with open(URLS, mode='r') as f:
    pages = f.readlines()
    pages = [re.sub("\\n","",i) for i in pages]
    pages = [i.replace(' ', '') for i in pages]
    pages.pop(0)
    
# Run loop for each page

list_of_soup = []

for page in range(len(pages)):
    
    content = requests.get(pages[page])    
    soup = bs(content.content)
    
    list_of_soup.append(soup)
    

# Extract content and append to one list

def get_content_list(soup):

    page_content = []

    content = soup.find('section', id="content")
    content_container = content.findAll(['h3','p','h4','h6','li'])

    for i in content_container:
        text = i.text
        cleaned_text = text.replace('\r\n', '').replace('\n', '').replace('       ', '')
        page_content.append(cleaned_text)

    return page_content


extracted_content = list(map(get_content_list, list_of_soup))

count = 0
for listElem in extracted_content:
    count += len(listElem)  


print(  len(extracted_content),"   =  Number of extracted sections")
print(count," =  Number of extracted objects")


# Flatten nested list

from itertools import chain
ffiec_content = list(chain(*extracted_content))

if len(ffiec_content) == count:
    print("PASS: ITEM COUNTS MATCH")
else:
    print("ERROR: ITEM COUNT MISMATCH\nMISSING DATA")
    
    

# NLTK Sentence Tokenizer

import functools
@functools.lru_cache(maxsize=128)
def sentence_tokenizer(content):
    sents = nltk.tokenize.sent_tokenize(content)
    return sents



sentences = []

for i in extracted_content:
    for j in i:
        sentences.append(sentence_tokenizer(j))
        
nltk_sentences = list(chain(*sentences))


print(len(ffiec_content))
print(len(nltk_sentences))


# Inverted index datastructure for searching
import nltk
from collections import defaultdict
from nltk.stem.snowball import EnglishStemmer  # Assuming we're working with English
 
class Index:
    """ Inverted index datastructure """
 
    def __init__(self, tokenizer, stemmer=None, stopwords=None):
        """
        tokenizer   -- NLTK compatible tokenizer function
        stemmer     -- NLTK compatible stemmer 
        stopwords   -- list of ignored words
        """
        self.tokenizer = tokenizer
        self.stemmer = stemmer
        self.index = defaultdict(list)
        self.documents = {}
        self.__unique_id = 0
        if not stopwords:
            self.stopwords = set()
        else:
            self.stopwords = set(stopwords)
 
    def lookup(self, word):
        """
        Lookup a word in the index
        """
        word = word.lower()
        if self.stemmer:
            word = self.stemmer.stem(word)
 
        return [self.documents.get(id, None) for id in self.index.get(word)]
 
    def add(self, document):
        """
        Add a document string to the index
        """
        for token in [t.lower() for t in nltk.word_tokenize(document)]:
            if token in self.stopwords:
                continue
 
            if self.stemmer:
                token = self.stemmer.stem(token)
 
            if self.__unique_id not in self.index[token]:
                self.index[token].append(self.__unique_id)
 
        self.documents[self.__unique_id] = document
        self.__unique_id += 1           
 
 
index = Index(nltk.word_tokenize, 
              EnglishStemmer(), 
              nltk.corpus.stopwords.words('english'))
              

# Add sentences to index
for string in nltk_sentences:
    index.add(string)

# Create search function
def search(search_term):
    lookup = index.lookup(search_term)
    return lookup
    

# Test search function
search('responsible')


# Define requirement terms
search_terms = ['shall', 'must', 'require', 'need', 'make', 'ensure', 'responsible']

# Pass search terms to search function
result0 = search(search_terms[0])
result1 = search(search_terms[1])
result2 = search(search_terms[2])
result3 = search(search_terms[3])
result4 = search(search_terms[4])
result5 = search(search_terms[5])
result6 = search(search_terms[6])

# Concatenate results in a set
all_results = {*result0, *result1, *result2, *result3, *result4, *result5, *result6}

print(len(all_results)," =  Number of extracted requirements")

# Prepare file for export
req_export = []
for num,req in enumerate(all_results, start=1):
    item_num = num
    item_req = req
    temp_entry = [item_num, item_req]
    
    req_export.append(temp_entry)
    

# Export list to CSV

import csv

    
with open('../data/ffiec_requirements.csv', 'a') as outcsv:   
    #configure writer to write standard csv file
    writer = csv.writer(outcsv, lineterminator='\n')
    for item in req_export:
        #Write item to outcsv
        writer.writerow(item)
        
        

# TEST AND COMPARE SPACY RESULTS TO NLTK
# instantiate spacy model
import en_core_web_sm
nlp = en_core_web_sm.load()


doc = nlp(ffiec_content[22])
for num, sent in enumerate(doc.sents):
    print(f"[{num}] {sent.text}")
    

from spacy.pipeline import Sentencizer
sentencizer = Sentencizer()

spacy_sentences = []

for i in ffiec_content:
    doc = nlp(i)
    sents = doc.sents
    for s in sents:
        txt = s.text

        spacy_sentences.append(txt)
        

print(f"Spacy: {len(spacy_sentences)}")
print(f"NLTK : {len(nltk_sentences)}")
print(f"Diff : {len(spacy_sentences)-len(nltk_sentences)}")
```

