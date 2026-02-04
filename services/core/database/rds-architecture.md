
General informations
- ~~Database as a Service~~ (DBaaS) -> Database Server as a Service (DBSaaS)
- Multiple db on one server (instance)
- Choice of DB Engines (MySQL, MariaDB, PG, ORacle, microsoft,...)
- RDS is a Managed service, ... no access to OS or SSH.

-> RDS run inside a VPC
-> Each instance as its own dedicated storage EBS 
-> Primary and standby db alway primary -> standby
![[Pasted image 20260107142040.png]]
![[Pasted image 20260107141843.png]]
1. We're billed as an instance and not usage.
2. Multi AZ or not
3. Storage type & Amount
4. Data transferred : billed by GB in and out of the DB
5. Backups & Snapshots, per GB/months
6. Licensing (optional)
