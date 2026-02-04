![[Pasted image 20260115113112.png]]
-> Maximum of **16** replicas 
Replication is at the storage level (**=No impact of perf**)
When to use global DB ? 
- Cross-Region DR (Disaster Recovery) and BC (Business Continuity)
	- Ability of promoting a replication to primary instance with R/W operations
- Global Read Scaling -> low latency perf improvements 
- ~1s or less from primary to secondary regions (1way replication)
- No impact on DB perf -> storage level
- MAX **5** secondary regions