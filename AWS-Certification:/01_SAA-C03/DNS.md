13 DNS Root servers exist 
Managed by 12 Large Organisations 
IANA Manages the DNS Root Zone
Registry = maintains the zones for a tld
Registrat = relationships with the tld zone manager
# Record Types 
- Nameserver (NS) : 
	- Allow delegation to occur
- A and AAA :
	- A : Map host to IPv4 address
	- AAA : Map host to IPv6 address
- CNAME : canonical name
	- Host to Host record 
	- Used to A record
- MX :
	- Mail server 
	- 2 parts : 
		- Value : is an host inside a zone (or an other one using fqdn)
		- Priority : Choose the value to use (lower is better) if same priority it's random
	- How to find a mail server (smtp) for a domain
- TXT : 
	- Add arbitrary text
	- Mostly used to **prove** ownership to other external parties 
### TTL :
- Numeric value in seconds
- Be carefull with high value TTL if domain change
- Lower TTL days/week before changes if planend

![[Pasted image 20250531175144.png]]
