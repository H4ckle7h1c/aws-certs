There are 2 types of backup like : 
	- Automated backups 
		- From 0 to 35 days of backup retention
		- Also backup transactions logs every 5 minutes 
	- Snapshots in AWS managed S3
		- Not automatic
		- Stored in S3
		- First snapshot is **full** then onward incremental
		- Can be restored but a new instance is created
We can see backup in the rds console but not in our S3. 

Most of the time taken from standby instance by default (if multi-az or main instance)


Restore : 
- Creates a new rds instance = new address
- Snaptop = sigle point in time
- Automated = any 5 min point in time 
- Backup is restored and transaction logs are replayed to bring the DB to a desired point in time (GOOD RPO)