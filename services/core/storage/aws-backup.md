![[Pasted image 20260209103900.png]]
- Backup and restore product 
- Consolidate management into one place, across accounts & regions
- Supports a wide range of AWS Products 

Backup plan = frequency window, lifecycle(transfert to a cold storage + expiracy), vault, region copy, ...
Continuous backup support PITR (point in time recovery)
Backup ressources = what is being backed-up ? 
Vault = destination of the backup
Vault Lock = write-once read many (WORM), 72h cool off and then even AWS can't even delete it.
On demand manual backups 

This product is continuously evolving : https://aws.amazon.com/backup-restore/services/