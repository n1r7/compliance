# Monitor

1. Identify systems.  
2. Identify connections between systems.  
3. Define system participant roles.  
4. Define normal behavior for each role.  
5. What are the features of that behavior?  

6. Observe user behavior on system.
7. Measure distance between role behavior and user behavior.
8. Cluster measurements.

9. Create graph = V(user)-send money->V(user)

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



### Profiles

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


### Transactions have shape

Transactions features:
1. Shape (inputs, outputs)
2. Value distribution
3. Input type
4. Input age


### Plan
1. Identify threats
2. Document risks
3. Review authoritative sources
4. Reivew investigations narratives, if any
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
    "feature_calculation" : "min(1,ln(number of users with deographic information value))",
}
{
    "behavior" : "The more frequent the change in deographic information, the greater the risk",
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
