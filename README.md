# STRATEGY
1. Maximize communication.
    - Are we doing what we need to do?
    - Are we communicating as such?
2. Be confident.
    - How do we know we can trust this user?
    - How do we know we can trust this transaction?
3. Effectiveness is the culture.
    - Know with certainty we fulfill our requirements. 
    - Protect the Libra Payment System from abuse.




# INTRODUCTION
Novi Financial (Novi) maintains a global anti-money laundering (AML) program designed to fulfill its legal and regulatory obligations to prevent, detect, and report potentially suspicious use of digital wallets on the Libra Payment System (Libra). The program comprises interconnected protocols that are automatic, auditable, and referenceable.

![alt text](https://github.com/nirvanapatel/compliance/blob/master/images/Protocols.png?raw=true)

### Libra
The Libra Blockchain is a decentralized, programmable database designed to support a low-volatility cryptocurrency that will have the ability to serve as an efficient medium of exchange for billions of people around the world. All of the data in the Libra Blockchain is persisted in a single-versioned distributed database. The versioned database allows validators to:
- Execute a transaction against the ledger state at the latest version.
- Respond to client queries about ledger history at both current and previous versions.

The database stores a ledger of programmable resources, such as Libra coins. A resource adheres to custom rules specified by its declaring module, which is also stored in the database. A resource is owned by an account that is authenticated using public key cryptography. An account could represent direct end users of the system as well as entities, such as custodial wallets, that act on behalf of their users. An account’s owner can sign transactions that operate on the resources held within the account.


### AML Compliance Program Framework
![alt text](https://github.com/nirvanapatel/compliance/blob/master/images/Compliance%20Protocols.png?raw=true)

Adhere to the existing tenets of anti-money laundering compliance, but connect the concepts in such a way that allows for greater program efficiency.
1.	Risk assessment
    1.	Network landscape – what do participants do?
        1.	Products and their functionality (features, limits, controls)
        2.	Services
        3.	User categories
        4.	Geographies
        5.	Partners and vendors
    2.	Legal landscape – what do participants have to comply with?
    3.	Policy landscape – what are participants saying they do?
        1.	e.g., Can companies answer “yes” to everything required under FFIEC exam manual?
    4.	Business rules, processes, and procedures – how are participants doing what they say they do?
2.	AML Compliance Program
    1.	KYC
    2.	Transaction monitoring
        1.	Rules and reputation lists: what do participants care about now?
        2.	Supervised machine learning: what should participants care about?
        3.	Unsupervised machine learning: what do participants need to be aware of?
    3.	Investigations
    4.	Reporting


### Compliance as an information hub

Compliance is binary – Novi is either compliant or it is not. The effectiveness of all compliance systems is dependent on having access to all pertinent information. Compliance is a solvable information problem.

Centralized data makes compliance surveillance more effective. Anti-money laundering compliance comprises three concepts:
1.	Who do I do business with?
2.	What are they doing?
3.	Does this warrant informing the government?

AML compliance systems must be able to connect these three concepts, and do so in a way that allows businesses to not only measure the effectiveness of their anti-money laundering compliance programs, but also use the system as a tool to test business strategies.

An effective anti-money laundering compliance system must create connections between data from different sources and continuously monitor its health and effectiveness:

- Internal
  - Users
    - Does this user exist?
    - Is this user sanctioned?
    - Enhance user profiles with external data
  - Transactions
    - Is this transaction permissible?
    - Is this transaction fraudulent?
    - Should this transaction be denied due to sanctions or other reasons?
    - Is this transaction indicative of financial crime?
  - Records
    - Distributed ledger provides full audit trail of records
    - Consensus driven – is the record different than expected?
  - Web
    - Is the network behaving as expected?
    - Has any area of the network been breached?
- External
  - Transform laws and regulations into rule logic
  - Create news hub to screen customers and update rule logic


#### Compliance systems improve all areas of business
Using this framework for enterprise systems development, businesses can more effectively manage compliance risk and free capital for strategy and investment.
- Business
  - Trends in customer behavior can identify new sources of revenue
- Intelligence
  - Transparency across the business reduces regulatory risk
  - Information can be provided to law enforcement
  - System that searches for weaknesses in an institution’s controls
- Compliance
  - Create “trap door” events that stop the transaction and/or traffic and trigger immediate investigation by a response team
  - Reduce risk by actively monitoring the health of the company
  - Decrease compliance costs by eliminating superfluous functions
  - Actively updating the centralized data hub with external data
    - Proposed or final updates to laws and regulations generates and warning for compliance
      - System predicts how change to law or regulation would impact protocols
        - Compliance staff reviews system-generated analysis and closes warning
        - Confirm system-generated analysis and provide input back to system
        - Correct and update system-generated analysis and provide input back to system
        - If law or regulation is in effect
        - Update rule logic

#### Data
Centralizing data has been a goal for many businesses. By centralizing data, businesses believe they can enhance enterprise systems and more effectively identify trends and opportunities. This has largely proven true as companies continue to find new opportunities for automation, efficiency, and revenue growth. As data technology continues to advance, centralizing data has become less important. Instead, finding the most efficient methods to access all of a company’s data has become paramount. Further still, developing strategic hypotheses and testing those through machine learning models that rely on a company’s data has been touted as the future of all business.

While identifying new ways to use data may lead to future success for businesses, doing so is not without risks. Data security, privacy, and integrity are of principal importance to stakeholders – customers, companies, and governments. Compliance-focused systems must then keep these principles in mind.
Encryption improves security and privacy. Distributed ledgers improve integrity. Proper controls and audit logs improve security, privacy, and integrity. Successful compliance-focused systems will have all of these features.

#### Information exchange
Companies rely on many different systems and changing those systems would be costly and time-consuming. AML is not intended to replace those systems. AML is a compliance-focused system that establishes standards for encryption of data, sharing of data for compliance use, and decryption of member data by appropriate parties and auditable results, while addressing the three key anti-money laundering concepts.

Traditional implementation occurs in phases:
1. Optimization of anti-money laundering transaction monitoring alerts to reduce useless (i.e., false positive) alert volume. Doing so will improve the effectiveness of the transaction monitoring system, reducing the burden on investigative and other anti-money laundering compliance staff.
  1. Inputs = alert details, including typology, rule, thresholds, and disposition
  2. What threshold does the system predict will result in an alert generating?
  3. Adjust thresholds, reduce false positive alert volume
  4.	Rigorous quality assurance process to make corrections to all inaccurate alerts
  5.	Run model after corrections to further tune thresholds
2.	Typology analysis through unsupervised machine learning. Unsupervised machine learning further optimizes transaction monitoring systems by identifying noteworthy connections and patterns that may warrant escalation to the government. System-identified typologies can result in new rules, which can be further optimized by the system. This further reduces the compliance program’s reliance of staff.
  1.	Inputs = customer and transaction data
  2.	Who knows whom – graph database
  3.	Who transacts similarly – cluster analysis
  4.	What can I reasonably predict – each customer is represented by an agent that builds and continuously updates a profile of expected behavior for that customer (think, a network of Nest thermostats that anticipate customer actions)
3.	Neural network integration and query tool. The more information AML is provided, the more significant the impact the system can have. By monitoring the entirety of a company’s systems, AML can be used to query the system to generate strategies. Businesses can measure the impact changes to products or controls can have system-wide. Functions will transition from creators or doers to testers and generators. 



#### Design to recursively learn
1.	Perception – what is happening now?
2.	Notification – what do I need to know?
3.	Suggestion – what do you recommend?
4.	Automation – what should I always do?
5.	Prediction – what can I expect to happen?
6.	Prevention – what can I avoid?
7.	Situational awareness – what do I need to do right now?

# WHY WE CARE
### The Shadow Economy
The shadow economy is “the market-based production of and payment for legal goods and services that are deliberately concealed from public authorities”.[^1]  Also called the underground, informal, or parallel economy, the shadow economy includes not only illegal activities, but also unreported income from the production of legal goods and services, either from monetary or barter transactions. In other words, the shadow economy comprises all economic activities that would generally be taxable were they reported to the tax authorities.[^2]

Underground economies can typically be classified in one or more different ways:[^3]
1. The **illegal economy** consists of the income produced by those economic activities pursued in violation of legal statutes defining the scope of legitimate forms of commerce.
    - Illegal activities that involve monetary transactions include:[^4]
        - Trade in stolen goods;
        - Drug manufacturing, trafficking, and dealing;
        - Prostitution;
        - Gambling; 
        - Smuggling; 
        - Fraud; 
        - Human trafficking; and 
        - Weapons trafficking.
2.	The **unreported economy** consists of those economic activities that circumvent or evade the institutionally established fiscal rules as codified in tax code.
    - A summary measure of the unreported economy is the amount of income that should be reported to the tax authority but is not so reported.
3.	The **unrecorded economy** consists of those economic activities that circumvent the institutional rules that define the reporting requirements of government statistical agencies.
    - A summary measure of the unrecorded economy is the amount of unrecorded income, which represents a discrepancy between total income or output and the actual amount of income or output captured or enumerated by the statistical accounting system designed to measure economic activity.
4.	The **informal economy** comprises those economic activities that circumvent the costs and are excluded from the benefits and rights incorporated in the laws and administrative rules covering property relationships, commercial licensing, labor contracts, tors, financial credit, and social security systems.

The shadow economy accounts for approximately 16 percent of the global economy; however, developing and transition countries have disproportionally large shadow economies, averaging between 26 and 34 percent of the local economies.

### Illicit Fund Flows

Money from the illegal economy has to go somewhere – people cannot pay for everything with or hold an infinite amount of physical currency. Funds from the illegal economy flow to where they are most productive.

For a given market of a product (encompasses all goods and services), demand is the relation of the quantity that all buyers would be prepared to purchase at each unit price. People value products differently than one another. For example, two potential tenants may value an apartment differently – one potential tenant sees $1,500 per month as a value, while the other sees $1,500 as overpriced. While this difference could be for a combination of reasons, generally, high prices will limit most people’s ability to afford a given product.

Prices for legal goods and services _should_ be driven by demand from the legal economy. In this utopic world, all people have legal employment and contribute to economic growth through taxes collected. When people do not 

Participants of the legal economy and illegal economy demand products from the legal economy equally, i.e., every person has the same basic needs (water, food, shelter) that are provided by the legal economy. An increase in demand without a corresponding increase in supply leads to higher prices. These price increases impact more than the demand for expensive items typically considered valuable assets (e.g., real estate, art, jewelry). Everyday expenses, such as rent, groceries, and transportation are also affected. Individuals who profit from the illegal economy inflate demand and increase prices every time they introduce illegally obtained funds into the legal economy.

![alt text](https://github.com/nirvanapatel/compliance/blob/master/images/Inflated%20prices.png?raw=true)

The economic impact of illegal economy is worsened because most profit from the illegal shadow economy is not taxed appropriately, resulting in reduced income for countries.

### Money Laundering
In general, money laundering is _the conversion or transfer of property knowing that it is derived from a criminal offense for the purpose of concealing or disguising the illicit origin of the property or helping others to do so_.[^11]  Under U.S. law, to be criminally liable for money laundering, “a defendant must conduct or attempt to conduct a financial transaction[] knowing that the property involved in the financial transaction represents the proceeds of some unlawful activity, with one of […] four specific intents […] and the property must in fact be derived from a specified unlawful activity.”[^12]

Money laundering is the criminal practice of processing illicit funds through a series of transactions designed to "clean" the funds so they appear to be the proceeds of lawful activity (Federal Financial Institutions Examination Council). 

The _enable, distance, and disguise_ model (Stephen Platt, Criminal Capital: How the Finance Industry Facilitates Crime) describes money laundering in terms of the objectives of the criminal, who seeks to:
- Succeed in perpetrating a crime
- Avoid detection
- Benefit from the crime
- Retain those benefits

![alt text](https://github.com/nirvanapatel/compliance/blob/master/images/Enable%20Distance%20Disguise.png?raw=true)

Money laundering is a diverse and often complex process. From a financial perspective, it occurs via one or more discrete steps:
1. **Placement**: Introducing illicit funds into Libra, ideally without attracting the attention of financial institutions or law enforcement.
2. **Layering**: Moving funds within Libra and the broader financial system, often in a complex series of transactions, to create confusion about the source of funds and complicate the transaction trail.
3. **Integration**: The ultimate goal of money laundering--using illicit funds to purchase licit goods and services.

![alt text](https://github.com/nirvanapatel/compliance/blob/master/images/Placement%20Layering%20Integration.png?raw=true)

The _enable, distance, disguise_ model takes into account that a criminal can make beneficial use of illicit funds (i.e. launder them) without ever placing, layering, or integrating them. In either model, the underlying question is the same: _What advantage does the product or service confer upon a user?_ It is critical to understand how a product's features make it vulnerable to money laundering, and to what extent existing limits and controls mitigate that risk.

### Terrorist Financing
There is no universal definition of terrorism, but U.S. law is instructive in defining it as violet or dangerous acts that appear to be intended to:
- Intimidate or coerce a civilian population;
- Influence the policy of a government by intimidation or coercion; or
- Affect the conduct of a government by mass destruction, assassination, kidnapping, or hostage taking.

**Terrorist financing** is the provision or collection of funds with the intent that they be used, or with the knowledge that they will be used, in full or in part, to carry out an act of terrorism. The funds used for terrorist financing can be funds of any kind, however acquired (18 U.S.C. 2339C).

In contrast to money laundering, which involves the disguising of funds derived from illegal activity so they may be used without detection of the illegal activity, terrorist financing can involve the use of legally derived money to carry out illegal activities. The objective of money laundering is financial gain or the disguising of illicit proceeds, whereas with terrorism, the objective is to promote the agenda or cause of the terrorist organization. Both money launderers and terrorists, however, attempt to disguise the association between themselves and their funding sources.

Money laundering techniques “are essentially the same as those used to conceal the sources of, and uses for, terrorist financing. Funds used to support terrorism may originate from legitimate sources, criminal activities, or both. Nonetheless, disguising the source of terrorist financing, regardless of whether the source is of legitimate or illicit origin, is important. If the source can be concealed, it remains available for future terrorist financing activities. Similarly, it is important for terrorists to conceal the use of the funds so that the financing activity goes undetected.”[^13]

There is an overlap between money laundering and terrorist financing:

![alt text](https://github.com/nirvanapatel/compliance/blob/master/images/Overlap.png?raw=true)

### Tax Avoidance

The shadow economy comprises activity that if it were legitimate, would be taxable, and laundering money entails converting illicit funds into apparently licit funds. Funds derived from or related to tax crimes require laundering in the same way that any other types of illegally gotten gains do.[^14]  Indeed, “[c]riminals will seek to launder the proceeds from their crimes to pay for [luxury goods] in order to avoid detection by the tax or law enforcement authorities.”[^15]  After surveying 19 countries, the Organization for Economic Cooperation and Development found that “[m]ost countries report that the strategies and techniques used by their tax authorities to detect tax evasion and money laundering” specifically related to identity fraud were “successful in terms of:

- Improving identification of suitable cases to audit;
- Preventing revenue loss through proactive data mining;
- Enabling the prosecution of cases that otherwise may have never been detected; and
- Providing the quickest opportunity to review returns that potentially use a stolen identify before the refunds are issued and thereby likely irretrievable.”[^16]

The Tax Justice Network, a tax-related think tank, reports that as of 2010, using conservative estimates, as much as US$32 trillion in global private wealth was “invested virtually tax-free through the world’s still-expanding black hole of more than 80 ‘offshore’ secrecy jurisdictions.”[^17]



### Criminalization of Money Laundering

The International Monetary Fund estimates that laundered funds represent between two and five percent of global gross domestic product.[^5]  Using World Bank estimates for GDP and applying IMF's estimate, between $1.75 trillion and $4.38 trillion were laundered in 2019. Criminality is profitable.

In part in response to the scale of the problem, multiple international treaties call for the criminalization of money laundering as a starting point for any AML/CTF regime:
- United Nationals Convention against Illicit Traffic in Narcotic Drugs and Psychotropic Substances (1988) (Vienna Convention)
- United Nations Convention against Transnational Organized Crime (2000) (Palermo Convention)

Criminalization of money laundering in accordance with these conventions is FATF’s first recommendation.[^7]  As international standards have developed, the range of predicate offenses for money laundering has grown.[^8]  The Vienna Convention, Palermo Convention, and FATF Recommendation 1 call for “apply[ing] the crime of money laundering to all serious offenses, with a view to including the widest range of offenses as money laundering predicate offenses.”[^9]

### Anti-Money Laundering Laws and Regulations

Anti-money laundering and counter-terrorist financing (AML/CTF) laws and regulations help protect the international financial system from abuse, which promotes the integrity of that system and contributes to its safety and security.[^10]  The Financial Action Task Force (FATF) enumerates 11 pillars of a sound AML/CTF regime that the FATF assesses as part of its ongoing evaluation of countries’ performance in fighting the shadow economy:

| Num |	COMPONENT |	DESCRIPTION |
| --- | --------- | ----------- |
| 1  | Risk, policy, and coordination | Money laundering and terrorist financing risks are understood and, where appropriate, actions coordinated domestically to combat money laundering and the financing of terrorism and proliferation. |
| 2  | International cooperation | International cooperation delivers appropriate information, financial intelligence, and evidence, and facilitates action against criminals and their assets. |
| 3  | Supervision | Supervisors appropriately supervise, monitor[,] and regulate financial institutions and DNFBPs [designated non-financial businesses and professions] for compliance with AML/CFT requirements commensurate with their risks. |
| 4  | Preventive measures | Financial institutions and DNFBPs adequately apply AML/CFT preventive measures commensurate with their risks, and report suspicious transactions. |
| 5  | Legal persons and arrangements | Legal persons and arrangements are prevented from misuse for money laundering or terrorist financing, and information on their beneficial ownership is available to competent authorities without impediments. |
| 6  | Financial intelligence | Financial intelligence and all other relevant information are appropriately used by competent authorities for money laundering and terrorist financing investigations. |
| 7  | Money laundering investigation and prosecution | Money laundering [offenses] and activities are investigated and offenders are prosecuted and subject to effective, proportionate[,] and dissuasive sanctions. |
| 8  | Confiscation | Proceeds and instrumentalities of crime are confiscated. |
| 9  | Terrorist financing investigation and prosecution | Terrorist financing offenses and activities are investigated and persons who finance terrorism are prosecuted and subject to effective, proportionate[,] and dissuasive sanctions |
| 10 | Terrorist financing preventive measures and financial sanctions | Terrorists, terrorist organizations[,] and terrorist financiers are prevented from raising, moving[,] and using funds, and from abusing the NPO sector. |
| 11 | Proliferation financial sanctions | Persons and entities involved in the proliferation of weapons of mass destruction are prevented from raising, moving[,] and using funds, consistent with the relevant [UN Security Council Resolutions] |


# WHAT WE DO

The Libra Payment System was designed to be secure and safe.

The safest payment system is one based on trust. If members share information and work together to fight financial crime, the system itself becomes safer and more efficient. Information-sharing programs exist to assist in the fight against financial crime. However, those programs are inefficient due to a lack of central governance, standards, and accountability. Novi seeks to avoid these shortcomings. 

To effectively fight financial crime, Libra members must:
- Collectively validate users of the network;
- Share intelligence and detection models; and
- Work together to continuously improve.

Novi's AML program is based on trust. Much like Libra, it uses ledgers and Merkle trees to ensure appropriate information is collected, verified, and available for review. 
- Novi verifies all users, so they can transact quickly and with confidence.
- Novi reviews every transaction, so Libra can remain secure and safe.
- Novi communicates with its regulators and collaborates with peers on building effective controls.

Shared data creates connections between users. Novi's AML compliance framework links and validates user information, and allows activity across the entire network to be monitored.







### Risk Management
Many organizations use the _lines of defense_ model for risk management (Financial Stability Institute "Four Lines of Defense Model"). With this model, risk-management responsibilities are divided into general categories.
1. First line of defense: Business operations
    - As the first line of defense, businesses are responsible for assessing and managing the risks posted by their products. To that end, the first line of defense, with the support of the second line, is responsible for verifying that product offerings, processes, and operations are lawful and managed appropriately.
2. Second line of defense: Compliance and risk functions
    - The second line of defense is responsible for monitoring and reporting risk-related practices and information, and overseeing compliance-related issues. The second line of defense sets standards for lawful and ethical business operations. The second line of defense aids the first line in identifying, measuring, monitoring, and controlling risks.
3. Third line of defense: Audit
    - The third line of defense provides to management and the Board of Directors its assessment of the effectiveness of governance, risk management, and internal controls.
    
Libra's unique features and Novi's immutable AML database necessarily redefine the lines of defense model for virtual assets. By making compliance an inherent part of the transaction process, Novi can efficiently fulfill its compliance obligations, and prove it has done so.
1. First line of defense
    - Product risks are mitigated through the transaction processing process, which has built-in controls based on Move.
2. Second line of defense
    - Requirements are implemented as protocols.
3. Third line of defense
    - The entire program is transparent and queryable.


    
### Program components
- **Policies** outline how Novi ensures it conducts business lawfully.
- **Processes** implement policies.
- **Procedures** describe how to run processes.
- **Controls** evaluate risks, manage execution, and test effectiveness.


### Users
Store every available piece of information on a blockchain so that user input, system-generated connections, and the status, method, and proof of verification are included within the user record. 

- How do users transact?
  - Internal records
     - Accounts
     - Transactions
  - What do users own?
     - Internal records
     - Public records
  - What do users value?
     - Internal records
        - Transaction trends
- What influences users?
  - Social media connections
  - Family
- What do users share?
  - Social media
- What is a user’s income?
  - Internal records
  - Public records
- What can the system reasonably predict?



#### Types of information

Company-initiated:
- All user information required by law.
- All user information required by Novi.
- All user information requested by Novi.
   - Non-incentivized
      - Electronic information gathering
      - Optional online form fields
      - In-person information gathering
      - Mail campaigns
   - Incentivized
      - Users that do not have or use certain risky features do not require monitoring for typologies that involve that feature.
         - The fewer the number of users that require monitoring, the more efficient the AML program can be, reducing costs.
            - SARs require teams of educated humans to do things – they can never be eliminated. 
         - Incentivizing users to reduce their threats to our system, we can reduce cost per SAR, thereby freeing up resources once allocated to AML compliance.  
      - Feature limits  
         - For each risky feature the user does not opt-in to, provide user the equivalent in points of the average cost per SAR involving a product with that feature.
         - Products have tiered features customers opt-into. 
            - Riskier product features require additional information from the user. 
      - Payment source identification
         - Identification of the source of funds reduces the largest risk of payments.
         - White list payments from confirmed sources utilizing the 314(b) process or Plaid, requiring regular checks to confirm the connection.
      - Social network connectivity
         - Improve watch list and sanctions screening effectiveness through social network confirmation using available APIs.
         - Users are incentivized to do so through assurances of frictionless transactions.
         - Provide users with terms and conditions that guarantee their privacy.



### Monitoring
Transaction monitoring entails the automated or manual review of transactions to identify activity of concern; when appropriate, report it to authorities; and evaluate whether customer relationships should be discontinued (Wolfsberg Group Statement on AML Screening, Monitoring, and Searching, 2009). Novi's transaction-monitoring strategy calls for:
- A comprehensive understanding of products offered by Novi, which enables identification of their money-laundering vulnerabilities;
- Thorough and clear documentation and governance, which are pillars of a sustainable program; and
- Technologies that can help Novi prevent, detect, and report financial crime, mitigate compliance risk, and protect against abuse of Libra.

Novi's monitoring program targets the interconnectedness of Libra. 

Novi's monitoring program uses a framework based on four concepts:
1. **Typologies**, which are classifications of money-laundering behavior;
2. **Behaviors**, which are a discrete type or set of user-initiated activities;
3. **Red flags**, which are risky behaviors; and
3. **Rules**, which use calculations to generate alerts.

The monitoring process entails:
1. Identifing systems.  
2. Identifing connections between systems.  
3. Defining system participant roles.  
4. Defining normal behavior for each role.  
5. Defining features of each behavior.  
6. Observing user behavior on system.
7. Measuring distance between role behavior and user behavior.
8. Clustering measurements.

9. Creating graph = V(user)-send money->V(user)

    Properties of users = 
    ```
        {
          "unique_id": string,
          "Roles": tuple(string),
          "Feature_scores": tuple(float),
          "money_sent": float,
          "money_received": float,
          "transaction_count": int
        }
     ```  

    Properties of money_send = 
    ```
        {
          "originator_id": string,
          "beneficiary_id": string,
          "transaction_time": timedate,
          "transaction_amt": float
        }
     ```

10. Cluster users by property



##### Profiles

1.	Customers
    1. Name
    2. Government ID
    3.	Passport number
    4.	Government identification number
    5.	Primary address
    6.	Mailing address
    7.	Other address
    8.	Phone numbers
    9.	Email address
    10.	Alert history (alerts raised, frequency, disposition)
    11.	Politically exposed person status
    12.	Birth date
    13.	Access
        1. IP address
        2. Device ID
        3. Location
    14.	Beneficial owner
2.	Accounts
    1.	Age
        1. Since establishment
        2. Since last transaction
        3. Since last login
    2.	Types
        1.	Features
        2.	Business rules
            1.	Limits
            2.	Controls
    3.	Usage (e.g., velocity, dormancy)
    4.	Geography
    5.	Authorized users
    6.	Alert history (alerts raised, frequency, disposition)
    7.	Connections
3.	Transactions
    1.	Types
        1.	Debit
        2.	Credit
    2. Parties
        1. Internal
        2. External
    3.	Frequency
    4.	Direction
    5.	Associated accounts and customers
    6.	Alert history (alerts raised, frequency, disposition)


##### Transactions have shape

Transactions features:
1. Shape (inputs, outputs)
2. Value distribution
3. Input type
4. Input age


##### Implementation Plan
1. Identify threats
2. Document risks
3. Review authoritative sources
4. Review investigations narratives, if any
5. Define typology based on authoritative sources and observed behavior
6. Define features that enable risks
7. Define expected behavior
8. Define risky behavior
9. Choose behavior curve
10. Map behaviors to typologies
11. Draft requirements and logic
12. Build
13. Train
14. Test
15. Generate output
16. Investigate
17. Analyze results
18. Estimate frequency
19. Draft closing memo
20. Review prototype with stakeholders
21. Submit
22. Draft procedures
23. Conduct training


##### Features
```
{
    "behavior" : "The greater the number of addresses paid by one source, the greater the risk",
    "risks" : ["money laundering", "terrorist financing", "fraud"],
    "expected_behavior" : "One source sends funds to only one account",
    "risky_behavior" : "One source sends funds to many accounts",
    "measurement" : "count",
    "feature_name" : "shared source",
    "feature_description" : "scores when the number of shared sources is more than one",
    "feature_calculation" : "min(1,ln(number of addresses paid by source))",
}
{
    "behavior" : "The greater the number of users that share demographic information, the greater the risk",
    "risks" : ["money laundering", "terrorist financing", "fraud", "error"],
    "expected_behavior" : "User demographic information is unique",
    "risky_behavior" : "User demographic information is not unique",
    "measurement" : "count",
    "feature_name" : "shared demographics",
    "feature_description" : "scores when more than one user shares demographic information",
    "feature_calculation" : "min(1,ln(number of users with demographic information value))",
}
{
    "behavior" : "The more frequent the change in demographic information, the greater the risk",
    "risks" : ["money laundering", "fraud"],
    "expected_behavior" : "The user never updates demographic information",
    "risky_behavior" : "The user updates demographic information more than twice in a 3-month period",
    "measurement" : "frequency",
    "feature_name" : "frequent updates",
    "feature_description" : "scores when customer makes at least one update, maximum score at 3",
    "feature_calculation" : "min(1,ln(count of updates)/ln(3))",
}
{
    "behavior" : "The more frequent a user attempts transactions at the limit, the greater the risk",
    "risks" : ["money laundering", "terrorist financing", "fraud"],
    "expected_behavior" : "User never attempts transactions at the limit",
    "risky_behavior" : "All of user's transactions are at limit",
    "measurement" : "frequency",
    "feature_name" : "limit testing",
    "feature_description" : "scores increases with more attempts, maximum score at 10",
    "feature_calculation" : "min(1,ln(attempts at limit)/ln(10))",
}
{
    "behavior" : "The greater the difference between the observed transaction and average user transaction, the greater the risk",
    "risks" : ["money laundering", "terrorist financing", "fraud", "collusion"],
    "expected_behavior" : "User's transaction is within 3σ",
    "risky_behavior" : "User's transaction is the largest",
    "measurement" : "percentage",
    "feature_name" : "transaction magnitude",
    "feature_description" : "scores when transaction is 3 standard deviations from the mean",
    "feature_calculation" : "if(amount>(mean(past amounts)) + stdev(past amounts)*3),1,0)",
}
{
    "behavior" : "The more frequent an account is accessed from an unknown source, the greater the risk",
    "risks" : ["money laundering", "terrorist financing", "fraud"],
    "expected_behavior" : ""The account is accessed from known sources,
    "risky_behavior" : "The account is accessed from unknown sources",
    "measurement" : "frequency",
    "feature_name" : "unknown sources",
    "feature_description" : "score increases the more often an account is accessed from unknown sources, maximum score at or above 0.25",
    "feature_calculation" : "min(1,tanh((unknown sources/total sources)/tanh(0.25))",
}
{
    "behavior" : "The greater the number of out-of-pattern transactions compared to category, the greater the risk",
    "risks" : ["money laundering", "terrorist financing", "fraud"],
    "expected_behavior" : "Behavior is within cluster",
    "risky_behavior" : "Behavior is outside cluster",
    "measurement" : "count",
    "feature_name" : "out-of-pattern transactions",
    "feature_description" : "score increases the more transactions outside cluster, maximum score at 5",
    "feature_calculation" : "min(1,ln(sum((observation - mean)/stdev) + 1)/ln(5+1)",
}
{
    "behavior" : "",
    "risks" : ["money laundering", "terrorist financing", "fraud"],
    "expected_behavior" : "",
    "risky_behavior" : "",
    "measurement" : "count",
    "feature_name" : "",
    "feature_description" : "scores when ",
    "feature_calculation" : "",
}
{
    "behavior" : "",
    "risks" : ["money laundering", "terrorist financing", "fraud"],
    "expected_behavior" : "",
    "risky_behavior" : "",
    "measurement" : "count",
    "feature_name" : "",
    "feature_description" : "scores when ",
    "feature_calculation" : "",
}
```







# Notes

[^1] Emerging from the shadows: the shadow economy to 2025. July 6, 2017. Association of Chartered Certified Accountants, available at www.accaglobal.com.

[^2] Hiding in the Shadows: The Growth of the Underground Economy. March 2002. International Monetary Fund, available at www.imf.org.

[^3] Defining and Estimating Underground and Informal Economies: The New Institutional Economics Approach. 1990. Edgar L. Feige, University of Wisconsin-Madison, available at core.ac.uk. 

[^4] The Shadow Economy. 2013. The Institute of Economic Affairs, available at iea.org.uk.

[^5] Reference Guide to Anti-Money Laundering and Combating the Financing of Terrorism, World Bank (hereinafter, World Bank Report) at I-6, available at worldbank.org.

[^6] Id.

[^7] World Bank Report at V-2-3.

[^8] Id.

[^9] Id.

[^10] An effective system to combat money laundering and terrorist financing, Financial Action Task Force, available at http://www.fatf-gafi.org/publications/mutualevaluations/documents/effectiveness.html.

[^11] World Bank Report at I-2.

[^12] U.S. Dept. of Justice, Money Laundering Overview, available at justice.gov (emphasis in original).

[^13] World Bank Report at I-5.

[^14] See Money Laundering Awareness Handbook for Tax Examiners and Tax Auditors, Organization for Economic Cooperation and Development (2009) at 11, available at oecd.org.

[^15] Id. at 14.

[^16] Report on Identity Fraud: Tax Evasion and Money Laundering Vulnerabilities, Centre for Tax Policy and Administration, Organization for Economic Cooperation and Development (2006) at 11, available at oecd.org.

[^17] James S. Henry, The Price of Offshore Revisited: New Estimates for “Missing” Global Private Wealth, Income, Inequality, and Lost Taxes, Tax Justice Network (2012) at 5, available at taxjustice.net.

