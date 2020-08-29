Compliance comes down to:
1. Words: Am I doing what I need to do? Am I communicating as such?
2. Efficiency: How do I know I am doing what I need to? What are my costs?

Effectiveness is the culture. We know with certainty we fulfil our requirements. We help law enforcement fight crime that harms our users.

The program is clear communication of:
1. How do I know I can trust this transaction?
2. How do I know I can trust this user?
3. How often have I assisted with a law enforcement initiative?
4. How many former users have been convicted?


Legal compliance:
1. Parse ECFR to docs
2. Split docs to sentences
3. Train byte-level tokenizer
4. Train BERT model
5. Fine tune BERT model with ECFR sentences

Classification:
Text -> BERT -> Dropout -> FC -> Softmax -> Class


1. Can the model identify requirements? Use deontic logic expressions.
2. Who reviews the re




# Monitoring
Identify systems.
Identify connections between systems.
Define system participant roles.
Define normal behavior for each role.
What are the features of that behavior?

Observe user behavior on system.
Measure distance between role behavior and user behavior.
Cluster measurements.

Create graph = V(user)-send money->V(user)
Properties of users = 
{
  "unique_id": string
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
  "transaction_amt": float,
}

Cluster users by property

  
  
 
 
 
 

 
 
 

