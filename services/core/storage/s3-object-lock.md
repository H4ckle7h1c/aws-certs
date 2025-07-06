- Object lock can be enabled when creating a new bucket but can't be enabled on already existing bucket (support req)
- Write-Once-Ready-Many (worm) : no delete, no override 
- Require versioning 
	- 1: retention period
	- 2: legal hold

---
## Retention period 

- Specified in **days** or **months**
- 2 modes exits : 
	- Compliance:  can't be adjusted, deleted or overwritten
		- ..even the root user
		- Until 
	- Governance : special permissions can be granted allowing lock settings to be adjusted 
		- s3:BypassGovernanceRetention
		- x-amz-bypass-governance-rentention:true
	- S3 Object Lock - Legal Hold 
		- Object version locking
		- ON/OFF system
		- No retention
		- No delete or changes until removed 
		- S3:PutObjectLegalHold
