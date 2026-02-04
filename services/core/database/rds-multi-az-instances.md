There is a standby instance in an other AZ in which there is synchronous replication

DB cname -> primary db 

![[Pasted image 20260112101122.png]]

 - In case of the failover, cname is switched to the standby which becomes the primary.
- Failover time -> 60 to 120s time to cname update 
- Backups can be taken frmo the standby instance 