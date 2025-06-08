
---
### Definition
A **role** is a type of identity within an AWS account (the other common type is an **IAM user**).

- **IAM User:** Typically used for a single, specific principal (e.g., a person or application).
    
- **IAM Role:** Designed for **multiple** entities (internal or external) that need temporary access.

Roles are used to grant temporary access to AWS ressources. It represent a set of permission inside an AWS account.

2 types of policies that can be attached to a role:
- Trust Policy : defines who can. assume the role
- Permission Policy : defines what is the role able to do

AWS Organization -> MGT of multiple accounts
STS : Secure Token Service `sts:AssumeRole` 

---
### Purpose  
IAM Roles allow secure, temporary access to AWS resources for trusted entities whether they are internal AWS services, users in your organization, or external third parties. They are commonly used for cross-account access, federated users, or granting temporary permissions to applications.

---

### Core Concepts

- **Trust Policy:**
    - Specifies **who is allowed** to assume the IAM Role.
    - Can include AWS services, users, or external accounts.
    - When the role is assumed, **temporary security credentials** are generated.
    - These credentials **expire** and must be **reassumed** when needed.
- **Permissions Policy:**
    - Defines **what actions** are allowed once the role is assumed.
    - Temporary credentials are evaluated against this policy.
    - If the permissions are updated, previously issued credentials may become invalid.
 ---
### Key Concepts  
- **AWS Organizations:** Used to centrally manage multiple AWS accounts.
- **STS (Security Token Service):** Used to generate temporary credentials when a role is assumed (via `sts:AssumeRole`).
- **Service-linked roles** : IAM role linked to a specific AWS service. Predefined by a service an provided a set of permissions this service need to interact with other AWS services. This can't be deleted unless it's not used anymore. https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create-service-linked-role.html
- **PassRole permission**: Allow user/service to pass an IAM role to another AWS service.

---
### When to use IAM roles ? 

AWS services is an example of ressource that use roles. 

##### 1st example :  AWS Lambda 
- By default no permission
- Not an identity
- Just a script

**Lambda Execution Role** :
- Trust policy that **trust** the lambda service
- Permission policy that grant access to AWS **products** and **services**
- **sts:AssumeRole** to generate a temporary security token and access to other ressources

Why a role ? We would need to hardcode the permissions of some access keys...
Why an IAM role ? We don't know how much lambda could be invoked 

###### 2nd example :  Emergency
Monitoring with Read-Only on ressources 
Customer got an emergy on a ressource ? Ex need to shutdown an EC2 -> temporary privileged permissions to shut it down.

Break Glass Situation :
We could have an emergency role that can be assume on certain situations. I can be logged an traced. 

3rd ex: On-premises identity management (active directory)
Situation -> AD with SSO or > 5000 identities 
How ? IAM role in the aws account that can be assumed by AD user to access S3 

ID federation : Managed small amount of roles internally and allow external identities to access it 

WEB identities federation : we trust external identities and we give them a role
- google
- twitter
- fb 
- ...
 
PRO : 
- No AWS credential used on the app !
- Use already existing user accounts for customer logins
- Scales to 100,000,000's of accounts