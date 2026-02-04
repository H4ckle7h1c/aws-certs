- Read replica has no use if no application awareness 
- Synchronous = AZ
- Asynchronous = Read Replicas

![[Pasted image 20260112103623.png]]
Why using read replicas ? 
- Improvements of read perf (up to x5)
- RR can have a lag (time for the replicas to synch the data)
- Global performance improvement for the read 
RTO/RPO improvements : 
- Snapshots & Backups improve rpo
- RTO are a pb (time to restore a snapshot)
- RR's offer a nr 0 RPO
- RR can be promoted quickly RTO 
- Failure only but data corruption is an issue if we promote it 
- Global availability is improved, global resilience...