Migrations are complex things to perform.

DMS is a manage database migration service :
- Runs using a **replication instance**
- **Source** and **Destination Endpoints** at **Source** and **Target** Databases
- One endpoint MUST be on AWS

![[Pasted image 20260115120920.png]]

Note: 
- Full load capture everything at a given time, add CDC to also include the changes performed during the migration on the source
- Can also just capture the bulk data using a native tool and then use DMS with CDC

SCT : Standalone tool
- SCT is used when converting **one database** engine to **another** 
- SCT is not used when migrating between DB's of the same type
- Works with OLTP DB Types (MySQL, MSSQL, Oracle)
- And OLAP (Teradata, Oracle, Vertica, Greenplum)

DMS & Snowball
![[Pasted image 20260115122934.png]]