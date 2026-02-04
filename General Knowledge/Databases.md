# Types of database 
## Relational 
- SQL : Structured Query Language 
	- Key characteristics : Structure **in** & **between** tables -> rigid schema 
# Non-Relational
- NoSQL - not one single thing : everything that doesn't fit in a database
	- Much more relaxed schema
- Type of NoSQL :
	- Key-Value DB
		- Simple key value pairs
		- In memory caching is also KV db
	- Wide Column Store 
		- KEY1(Partition Key) - KEY2(Other Key)
		- Dynamo DB
	- Document DB: 
		- Store structured value like json, xml,... 
		- Same idea as Key-Value DB 
		- Collection, ordered db, ... 
		- Ideal Scenarios: Interacting with whole documents or deep attribute interactions
	- Column DB: 
		- RowStore (MySQL) : (order id;product;colour;size;price) -> OLTP Online Transaction Processing everything in row 
		- Column Store (Redshift) : Data is the same but stored together in column
	- Graph DB
		- Nodes are values stored as KV
		- Nodes have relationships and directions
		- Relaction may have a value as well
		- Data is pulled out as is 
		![[Pasted image 20260105095410.png]]

# Transaction Models

CAPT Theorem -> Consistency, Availability, Partition Tolerant (resilience)
[https://en.wikipedia.org/wiki/CAP_theorem](https://en.wikipedia.org/wiki/CAP_theorem)
ACID = Consistency
Base = Availability

[https://en.wikipedia.org/wiki/ACID#Consistency](https://en.wikipedia.org/wiki/ACID#Consistency)

[https://en.wikipedia.org/wiki/Eventual_consistency](https://en.wikipedia.org/wiki/Eventual_consistency)

[https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/transactions.html](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/transactions.html)
## ACID
![[Pasted image 20260105235931.png]]

Atomic = **ALL** or **NO** component of a transaction succeeds or fails
Consistent = transaction move from one valid state to another. Nothing in-between
Isolated=If multiplae transactions at once, they don't interfere with each other. 
Durable= Once committed transactions are durable, store on non-volatile mem,
## Base 
Basically Available= READ and WRITE are available as much as possible but without any consistenty
Soft State=DB doesn't enforce consistency, app/user handle this
Eventually Consistent= If we wait long enough, reads from the system will be consistent

![[Pasted image 20260106000532.png]]




EC2 DB vs RDS :
If we have DB on EC2 we lack the following

![[Pasted image 20260107140559.png]]