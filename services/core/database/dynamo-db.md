NoSQL database as a service
Public service
Key-Value or Document db
No self-manage or infra to manage compared to rds or aurora 
**Manual**/**Automatic** provisionned IN/OUT or **On Demand**
Resilient across AZs
Backups, PTR


--
![[Pasted image 20260309132305.png]]

Dynamo DB is a 'table as a service'
A table is a grouping of ITEMS with the same Primary Key :
- Simple (Partition)
- Composite (Partition + Composite key)
Item = 400KB max
More perf = more capacity : 
- Writes: 1WCU 1KB/s
- Reads:  1RCU 4kb/s 

On demand backups : 
- Retained until removed
- Restore 

PITR : Point in time recovery
- 35 days window 


![[Pasted image 20260309132313.png]]

![[Pasted image 20260309132320.png]]


![[Pasted image 20260309132406.png]]
Billed on rcu, wcu, storage and features


--- 

Operations : 

- On-demand: for unknown, and unpredictable load and requires low admin
	- It prices per M of R or W units
- Provisionned: 
	- RCU and WCU set per tables
	- Every operation consumes a leat 1RCU/WCU
	- 1RCU is 4kb/s max 
	- 1WCU = 1KB/s
		- Burst pull 300s 
		- If pull is used then error is raised and then it's throttled 

Query operation : 
- Way of retrieving data 
- Start with a partition key (can add a sort key)
- More efficient to fetch multiple items per operation

![[Pasted image 20260309133332.png]]
![[Pasted image 20260309133342.png]]

Scan is the least efficient operation => scan the entire table = more data consumed 


### DynamoDB Consistency Model

![[Pasted image 20260310132402.png]]

Write always occurs on the reader not that's why write cost more than the read. 

2 types of read: 
- Eventually consistent : 
	- Double amount of data for the same RCU -> 50% price reduction
	- Latest data is not guaranteed
- Strongly Consistent: 
	- Always read the leader node to get the most up2date data

WCU calculation. 
For example we store 10 ITEMS per second 2.5K avg size per item
Always fallback to items/s 
Calculate **WCU** per item -> round up (item size/1kb)
Multiply by average number per second 

RCU calculation: retrieve 10 items per second... 2.5kb
RCU per item round up (item size/4kb)

With strongly consisteny -> 10 RCU
Eventually consisten = 5rcu


### Indexes 

Query can only work on 1 PK value at a time
Query is the most efficient operation in DDB
LSI = local secondary indexes & **must** be create with a table 
Local Secondary Indexes (LSI) and Global Secondary Indexes (GSI)
MAX 5LSI's per base table
It's an alternative **SK** on the table
Shares the RCU and WCU with the table
Attributes = ALL, KEYS_ONLY & INCLUDE 

![[Pasted image 20260310134403.png]]
In this case, sorting on the 'Sunny Day' attribute this would trigger a scan as it's not the PK which is not efficient at all.

![[Pasted image 20260310134408.png]]

Can be created at any time
Default limit of 20 per table 
Alternative PK and SK 
They have they own RCU/WCU


Careful with projection => KEYS_ONLY, INCLUDE, ALL.
By default use GSI and LSI only when **strong consistency**

---
### Dynamo DB Streams & Triggers 
It's a time oredered list of **ITEM CHANGES** in a table
24h rolling window (kinesis behind the scene)
Records INSERTS, UPDATES and DELETES

![[Pasted image 20260310135603.png]]

![[Pasted image 20260310135928.png]]

Item change -> generate an event
Contains the data which changes 
An action is taken using that data
AWS = Streams + Lambda
Reporting & Analytics
Aggregation, Messageing or notifications

---

### Global Tables
All tables are the same and viewed as **multi-master cross-region** replication
Tables are created in multiple regions and added to the same global table
**Last writer wins** is used for conflict resolution
**Read** & **Writes** can occur to **any region**
Generally **sub-second** replication between regions
Stongly consisten reads **ONLY** in the same region as writes 

![[Pasted image 20260310140447.png]]


---

### DAX 

It is an in-memory cache.
![[Pasted image 20260312135021.png]]
This first implementation lacks of integration with database software. 
The second one is better, 1 set of api call using one sdk.

![[Pasted image 20260312135025.png]]

Dax operate inside a VPC within a primary AZ. 
There are 2 types of cache: 
- Item cache 
- Query cache

Dax is a cluster: 
- Primary Node (writes) and replicas (read)
- Nodes are HA... primary failure = election
- in-memory cache - scaling much faster reads, reduced costs 
- Scale UP and Scale OUT (Bigger or More)
- Supports write-through 
- DAX is Deployed WITHIN a VPC

Great 

---
### DynamoDB TTL 

![[Pasted image 20260312140103.png]]

