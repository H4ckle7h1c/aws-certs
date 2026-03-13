![[Pasted image 20260312142217.png]]
![[Pasted image 20260312142220.png]]
Elasticache is an in-memory database that provides **high performance**
Managed **Redis** & **Memcached**
-> Can be used to **cache data** for **read heavy** workloads with low latency
Reduce the database workloads (expensive)
Can be used to store Session Data (Stateless Servers)
-> Application need to be configures to use this caching 



Memcached vs redis
simple data structures vs advances structures
no replication / az
multiple nodes (sharding) / replication (scale reads)
no backups / B&R