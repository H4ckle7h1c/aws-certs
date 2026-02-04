
# Encryption
- SSL/TLS is available for RDS -> can be mandatory
- RDS supports EBS volume encryption -> KMS
	- Encryption can't be removed if used
- RDS MSSQL and RDS Oracle Support TDE (Transparent Data Encryption)
	- Encryption is handled within the DB engine
	- RDS Oracle supports integration with CloudHSM
	- 
![[Pasted image 20260107143001.png]]

# IAM Authentication
- Configure RDS with IAM users authentication only
- ![[Pasted image 20260107143818.png]]
- 