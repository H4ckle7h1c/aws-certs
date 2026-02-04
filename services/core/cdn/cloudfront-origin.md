Cloudfront origin = where cloudfront goes to get data 
Origin group = resilience

Origins : 
- S3
- Media package channel
- AWS media store container 
- Everything else...


S3 Origin : 
- By default look at the root of the bucket -> optional path can be defined 
- Origin access : can restrict access to the S3 only through cloudfront 
- Custom origin header can be passed 
Custom origin : 
- Same origin path as S3 for subpath 
- Can define a minimum SSL protocol
- Origin protocol policy 
- **Custom port for HTTP/HTTPS** 


![[Pasted image 20260202140326.png]]