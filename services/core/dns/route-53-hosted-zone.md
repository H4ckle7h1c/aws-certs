- Route 53 is a database for domain names 
- It's Globally resilient
- Host DNS records 
A hosted zone har db referenced via delegation using nameserver record. It's authoritative for a domain name.

Route 53 resolver = IP + 2

It's a dabaze zone file hosted by R53 (public name server)
Accessible from VPS and public internet 
Hosted on 4 R53 name servers (ns) for the zone 
Externally registered domains can point to R53 public Zone

![[Pasted image 20260211095821.png]]




![[Pasted image 20260211100850.png]]
Associated with VPC. 
Ex : show internal users internal website and public user public site under the same domain




![[Pasted image 20260211101117.png]]