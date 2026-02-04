![[Pasted image 20260128104521.png]]
- Service used to create and manage APIs 
- Endpoint/Entry-point for applications 
- Highly available, scalable, authorisation, throttling, caching, CORS, transformations, OpenAPI spec, direct integration, ... 

![[Pasted image 20260128104528.png]]
![[Pasted image 20260128104532.png]]
APIs are deployed to stages, each stage has one deploy,ent. 
Canary = certain percentage of the trafic is sent to the canary which can be promoted to prod.

Errors : 
- 4xx - client/request errors 
- 5xx - server errors -> valid request but BE issue
- 400 - Bad request = generic 
- 403 - Access denied, authorizer denies or has been filters 
- 429 - Throttling, rate limit
- 502 - Bad GW exception, bad output returned by lambda
- 503 - Service unavailable 
- 504 - Integration Failure/Timeout - 29s limit 

Caching : 
- Configure per stage
- 500 up to 237Gb in size
- Can be encrypted
- Default ttl is 300s and can go from 0 to 3600s
![[Pasted image 20260128104538.png]]