
---
### Definition 

Identity used for anything requiring long-term access e.g. Humans, Applications or service accounts

---
### Core concepts 
- Principal : 
	- Individual person, group of ppl, applications,...
	- Need to be authorized to access ressources 
	- Request IAM to interact with users 
	- Need to authenticate with an Identity within IAM
- Auth : 
	- Principal prove that it is an identity that he claims to be 
	- U&P or Access Keys
	- After auth -> Authenticated Identy = is that he is the identity he claimed to be. (e.g. a user Ludo givin U&P)
	- Authenticated entity will be checked if author
- Authentication = prove iam id he claimed to be 
- Authorization = IAM check statement applying to authenticated identity

Amazon Resource Name (ARN) : Uniquely identify single resources within AWS Accounts

arn:aws:s3:::catgifs -> Bucket
arn:aws:s3:::catgifs/* -> Object in the bucket

Key figures : 
- 5,000 IAM users per account
- IAM user can be a member of 10 groups  