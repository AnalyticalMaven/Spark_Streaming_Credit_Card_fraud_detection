Project Summary for GitHub
With the rising number of fraud cases, RetailCorp Inc.'s primary focus is to ensure a delightful and secure shopping experience for its customers. This project aims to build a real-time fraud detection solution using Kafka, Spark, and NoSQL databases. ce3f47ca-ee94-4bd3-946c-1c1c30e342ef-Capture9
![Uploading image.png…]()

Key Features:

Fraud Detection: Classifies transactions as fraudulent or genuine based on predefined rules.
Customer Information Update: Continuously updates relevant customer information for real-time support.
Components:

Data Sources:

Card Member Data: Stored in AWS RDS.
Historical Transactions: Provided as a CSV file.
Real-time Transactions: Streamed from POS systems to Kafka.
Data Processing:

Load Historical Transactions: Ingest into a NoSQL database.
Ingest AWS RDS Data: Load into Hadoop for processing.
Create Lookup Table: For quick access to UCL, last transaction details, and credit scores.
Real-time Transaction Processing: Validate transactions based on UCL, credit score, and ZIP code distance.
Update Lookup and Transactions Tables: Maintain accurate and up-to-date records.
Validation Rules:

Upper Control Limit (UCL): Derived from the moving average and standard deviation of the last 10 transactions.
Credit Score: Transactions declined if the score is below 200.
ZIP Code Distance: Checks for improbable travel distances between consecutive transactions.
Tasks:

Task 1: Load transaction history into NoSQL.
Task 2: Ingest AWS RDS data into Hadoop.
Task 3: Create and populate the lookup table.
Task 4: Ingest real-time data from Kafka and validate transactions.
Task 5: Update transaction status and lookup table based on validation results.
Deliverables:

Python Script (spark-streaming.py): Contains code for processing input data streams.
PDF Document (CodeLogic.pdf): Explains the logic and commands used.
Output ZIP Files:
Console-output file: Summarized input tables.
Timebased-KPI.zip: JSON files for time-based KPIs.
Country-and-timebased-KPI.zip: JSON files for country- and time-based KPIs.
Validation:

Historical transactions count: 53,292
AWS RDS data count: 999 records
Final transaction count: Over 59,000
This project ensures efficient and secure transaction processing, enhancing customer experience while mitigating fraud risks.
