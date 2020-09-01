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
    5.	Primary address (number, street, city, state, zip code, country)
    6.	Mailing address (number, street, city, state, zip code, country)
    7.	Other address (number, street, city, state, zip code, country)
    8.	Phone numbers
    9.	Email address
    10.	Alert history (alerts raised, frequency, disposition)
    11.	Politically exposed person status
    12.	Birth date
    13.	IP address
    14.	Beneficial owner
2.	Accounts
    1.	Tenure
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

