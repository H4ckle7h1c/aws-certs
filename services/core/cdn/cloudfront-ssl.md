Default cname : https://xxx.cloudfront.net
SSL supported by default : *.cloudfront.net cert

Alternate Domain names (cnames) can be added with alternate domain name
Verify the ownership of certificate that match the distribution
Global service -> create or add cert in **us-east-1**


Both can be allowed. HTTP or HTTPS, HTTP => HTTPS Only 
Both connections need valid public certificates (doesn't work with self signed certs)


Historically (bef 2003) each ssl needed it's own ip
Encryption -> tcp level
Host headers happen at the layer 7 // application


SNI -> server name identifier : added in tls1.0 in 2003 allowing multiple certificates on a single ip

Old browser doesn't support SNI -> CF charge more for this as it require a dedicated IP (~600$)

![[Pasted image 20260202104307.png]]