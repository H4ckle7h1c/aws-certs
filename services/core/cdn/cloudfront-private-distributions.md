Behaviours: 
- Public: Open Access to objects 
- Private: Requetes require Signed Cookie or url
1 behaviour = whole distrib either Public either Private
This require a signer: 
- Legacy - cloudfront key -> created by an account root user -> added as a trusted signer
- NEW - Trusted Key Groups : determine which key is used to create signed url/cookies


Signed URL vs Signed Cookies
- SignedURLS = provide access to one object, and if client doesn't support cookies
- Cookies: Provides access to groups of objects. Group of files / files of a type

![[Pasted image 20260202144945.png]]


