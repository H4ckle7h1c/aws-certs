Regional service.

Everything that can be done in AWS account can be logged. 

Purpose : Logs api calls/activities as a CloudTrail Event
90 days of history by default for no cost
To customize service -> create a trail

Management events and Data event (+insights events)

Mgt control plane information
Data : data plane, (uploading objects to S3 or ...)

Trail : way to configure cloudtrail
- one region trail : only logs events for that region
- all region trail : collection of trails in all regions but managed as 1 trail

Global services : 
- Logs to `us-east-1`
- Global service event that need to be activated in the trail

Logs generated are stored in a S3
JSON formatted 
Can be injected into CloudWatch logs 

Take home :
- enabled by default (**90 days of retention**)
- No storage into S3 unless we create a trail
- **Trails** are config of S3 and CWLogs
- Mgt event **only** by default 
- **Global service events** need to be activated to catch global service (IAM, STS, Cloudfront )
- NOT REALTIME -> delay 