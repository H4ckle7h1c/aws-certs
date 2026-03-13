Standard AWS account : account not part of an organizations. Within this standard organization -> create an organization. This account becomes the **Management** Account (previously **master** account, or can be called payer account). 

Within this account we can invite other standard account to join the organization. They change **standard** account -> **member** account

Organization is composed of :
- 1 management account 
- 0+ member account

Structure is hierarchical (inverted tree)
- Organization Root (!= aws account root user)
	- Organizational Unit (OU)
	- Just a container

Pro : 
- Consolidated billing.
- Member account pass its billing to the Management Account. 
- The payment method is passed to the mgt account.
- Consolidation of **reservations** and **volume discounts**

SCP : Will be checked later

Instead of inviting new account we can directly create them directly within the organization.

It changes the best practices. 
We don't need IAM users inside each organization.

Best practice : 
- 1 AWS account that contains all the identities to log into
- We can have on-premise ID that log the federated user account
- Management of roles and use **role switching**

1- log into the identity in the identity account
2- role switch to access other accounts