---

---
---
### Scope & Resilience  
- **Service Type**: Public
- **Scope**: Global 
- **Resilience Level**:  
  - AZ-resilient ✅  
  - Region-resilient ✅
  - Global-resilient ✅ 

---
### Purpose  

Register domains, manage DNS records, and route traffic using highly available, scalable domain name system services.

---
### What is it?  
Amazon Route 53 is a **scalable and highly available Domain Name System (DNS) web service**.  
It provides domain registration, DNS routing, health checking, and traffic flow capabilities.  
It operates **globally**, with DNS servers distributed across edge locations.


---

### Core Concepts  
- Zone file : create zone file (db) and create associated ns
-  Hosted Zone (dns as a service )
	- Create and manage : Zone files (db)
	- Hosted on managed NS : 
		- can be public 
		- private (linked to a VPC)
- Store records
		
---

### Key Features  (ex: animals4life.org)
1. Check with the registries that a TLD (top level domain is available)
2. Create a zone file for the domain registered (db file)
3. Allocate manage nameservers for this zone and distribute them globally (usually 4 servers)
4. Communicate with the .org (PIR) to register the ns reccord entry into its associated TLD

---

