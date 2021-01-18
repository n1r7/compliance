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
