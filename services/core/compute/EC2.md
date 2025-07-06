### Purpose  

---
### What is it?  

EC2 instances are virtual machines (OS+Ressources) that run on EC2 hosts.

---
### Core Concepts  
- **Shared Hosts:** Host is shared between multiple customers
- **Dedicated Host**: Cost is allocated to the host and not the instance
- **Hosts = 1AZ** : AZ resilient
- Everything is linked to AZ : Storage, network, volumes, ...

---

### Key Features  
- Stores 
	- [[Instance Store]] : store linked to the host
	- Network store: [[EBS]] 

---
### When to chose EC2 ? 
- Traditional OS + compute 
- Long Running compute 
- Server Style Applications
- Burst or steady-state load
- Monolithic application stack
- Migrated application workload or disaster recovery 

