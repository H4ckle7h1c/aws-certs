 
 Definition : Attached to AWS identities and ALLOW or DENY access to AWS ressoures

Identity Policies : 
- Set of security statements
- Grant or Deny access to AWS prod/feat to identities that uses that policy

IAM Policy Document : 
- One or more statements that grant or deny access

---
Core Concepts  

Statement : 
- State id or SID : human readable identification of a statement
- Only applies if the statement matches the actions and the ressources
- Actions : can match on or multiple specific operations. Can use wildcards, individual actions or a list
- Ressource : same as action but match ressources
- Effect : either 'Allow' or 'Deny', define what is happening if the 'action' and 'ressource' matches the statement

--- 
The challenge is when there is an overlap in the statements 

- Priorities :
	1. Explicit Deny : Always take priority
	2. Explicit allow : Access if no explicit deny
	3. Default Deny (Implicit) 

DAD : Deny-Allow-Deny	   

Exception given for the root account


---
Type of affectation
Inline Policy : Apply a Json to individual identities
- Not scalable
- Used for exceptional access rights
Managed policy : Json with statement into it
- Assign it to identities 
- Reusables
- Low Management Overhead
- Used for normal default business rights

2 Main types : 
- AWS managed policies
- Customer managed policies : more granular


If multiple policies attached, (inlined, group, ...) AWS merge those policies into a single set to check 