- Provide data ingestion
Concepts :
- Kinesis is **scalable streaming** services = designed to consume huge amount of data from multiple of inputs
- Producers **send** data into a kinesis **stream**
- Stream store a **24-hour** moving data -> can be increased to 365 days but with additional cost
- Good use case: analytics and dashboards 
![[Pasted image 20260204102733.png]]
Type of arch : Shard architecture 
More shard -> more cost -> more perf 

Data stored in data record with a max size of **1MB**

**Kinesis firehose** to move data into S3

SQS vs Kinesis

- Ingestion of data -> Kinesis N producers <> N consumers
- **Decoupling** services, **async** communication, ... -> SQS = 1 prod group <> 1 consumption group
- **No persistence** of message, **no window** in sqs
- Kinesis = huge scale ingestion, multiple consumers, rolling window, ingestion, analytics, monitorinc, app clicks, ...