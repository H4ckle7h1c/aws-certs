- Serverless Interactive Querying Service
- AD-hoc queries on data - pay only on data consumed
- Schema-on-read 
- Original data **never changed** - remains on S3
- Schema translates data => relational-like when read 
- Output can be sent to others AWS services 

![[Pasted image 20260312140500.png]]Data is streamed through the schema while being read
No infrastructure is involved 
Good fit where loading/transformation isn't desired 
AWS Glue Data Catalog & Web Server logs  
W/ Athena Federated Query can use as well other data sources 