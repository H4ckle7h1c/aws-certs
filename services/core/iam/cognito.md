Service provides :
- Authenticated, Authorization and user management for web/mobile apps

User Pools -> Sign-in and get a JSON Web Token (JWT)
- User directory management, profiles, sign-up & sign-in, MFA, and other security features
Identity Pools -> Allow to offer acces to temporary AWS Credentials
- Unauticated Identities - Guest Users 
- Federated Identities - SWAP - Google, FB, ..., SAML2.0 & User Pool for short term AWS Credentials 


Key takeway :
- User pool -> Signin/Signup
- Id pool -> Swapping external id with a temp token (called identity federation)
![[Pasted image 20260205110005.png]]
Those cognito issued token can't be used to access AWS ressources.

![[Pasted image 20260205110014.png]]
Cognito has 2 roles : 
- Authenticated
- Unauthenticated 
Temp cred are issued and then renewed 



Final Arch:
- User pool = 1 set of user to manage -> outcome = user token returned to the app
- Cognito pass this token for temp aws credential
![[Pasted image 20260205110023.png]]