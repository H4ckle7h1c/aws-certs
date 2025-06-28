[https://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies.html](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies.html)

Key points : 
- Private by default 

---
### Core Concepts  

- **[[Ressource Policy]]**:  
	- Like id policies but attached to bucket
	- Ressource perspectives permission
	- ALLOW/DENY same or **different** accounts
	- ALLOW/DENY **Anonymous** principals
	- Principal : the presence of the principal in a policy indicate we deal with a ressource policy
-  [[Bucket Policy]]: 
	- Is a type of ressource policy associated to a bucket
	- Default when granting anonymous access to buckets
- ACLs : 
	- Define **access** on objects and **bucket**
	- Legacy
	- Inflexible & Simple permissions
- Block Public Access : 
	- Will apply on any anonymous principal

By default if anonymous access, no identity policy so bucket policy applies.