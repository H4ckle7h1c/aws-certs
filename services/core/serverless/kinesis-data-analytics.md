Provide data analytics
- Realtime data processing of data using SQL
- Ingest data from Kinesis Data streams of firehose
- Sent to destinations:
	- firehose (S3,redshift, elasticSearch & splunk) => data near real time
	- AWS Lambda
	- Kinesis DS 

![[Pasted image 20260204104350.png]]

Input and Output are defined in the Kinesis Application
Reference data is static data that can be used to enrich data 

Which use cases : 
- Streaming data needing **real-time sql processing**
- Time-series analytics **election/e-sport**
- **Leaderboards** for games
- Real-time metrics - **Security & Response** teams
Really complex data analysis in real-time -> kinesis