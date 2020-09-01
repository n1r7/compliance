Monitor.

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
{
  "unique_id": string,
  "Roles": tuple(string),
  "Feature_scores": tuple(float),
  "money_sent": float,
  "money_received": float,
  "transaction_count": int
}  

   Properties of money_send = 
{
  "originator_id": string,
  "beneficiary_id": string,
  "transaction_time": timedate,
  "transaction_amt": float
}

10. Cluster users by property
