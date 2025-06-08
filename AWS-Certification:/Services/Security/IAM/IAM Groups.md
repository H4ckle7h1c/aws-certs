Definition : IAM Groups are containers for Users. Cannot log in into a group and do not have credentials. Used to organize users. 

Groups can have attached policies :
- Inline or Managed as well
- No hard limit on the max number of users inside a group (could contain the max 5k users)
- No nesting
- Soft limit of 300 groups per account (can be increased by the support)
- Group are not identity, can't be references as a principal in a policy
IAM User : 
- Can be a member of multiple IAM groups 

SCP : 
- Don't grant permissions
- Do define boundaries

Usage : 
- Allow List 
- Deny List 
- Default Policy : 
	- FullAWSAccess 

Allow list archi : If we activate SCP we have by default explicit deny with the FullAWSAccess. To have granular access we need to delete this policy and define our custom access list. Drawback is that we have to add every service identities want to use. 
Deny list archi is better for SCP as less admin overhead.


Effective permissions for identities in an account = overlap identities policies in account and scp

![[Pasted image 20250608193730.png]]
