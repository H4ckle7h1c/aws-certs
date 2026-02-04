ACM can be used as a **public** or **private** Certificate Authority (CA)
- Private CA: Applications in a private org
- Public CA: Browsers trust a list of providers 
ACM -> generate / import Certificates
If generated -> automatically renew them

Supported AWS Services **ONLY** (e.g. CloudFront, and ALBs)
For eg -> if we manage an instance (EC2) with root access we have a way to manage the certs. Supported services are services in which we need a secure way to deploy and manage them 
ACM is a regional service.

**Certificates can't leave the region they are generated/imported**
For **ALB** cert in the same region the service is running.

For **CloudFront** operate through eu-east-1


![[Pasted image 20260129101318.png]]

Cross region deployment = not supported
Cloudfront -> acm us-east-1