![[Pasted image 20260312143504.png]]

It's a Petabyte-scale data whare 
OLAP (Column based) not OLTP (row/transactions)
OLAP: online analytical processing
Redshift Spectrum => load data directly inside S3 without loading it 
Direct Query other DBs using **federated query***
Integrates with AWS tooling such as Quicksight
SQL like query engine 

=> Provisioned service as it used Server (not serverless)
It use a cluster architecture which are running in one AZ in a VPC
Leader Node - Query input, planning and aggregation
Compute node - performing queries of data (having portion of the workloaded, those slices are working in parallel)
Support VPC Security, IAM Permissions, KMS at rest, CW 
Monitoring...
**Redshift Enhanced VPC Routing -> VPC Networking !!** 



---
### Resilience and recovery : 

**![[Pasted image 20260312144321.png]]**

Automatics backups : every 8 hours or every 5GB of data 
Restoring for snapshot create a new cluster 