- Allows access via HTTP
- **Index** and **Error** document are set
- custom domain via r53 -> bucket name matters

Use cases : 
- Offloading : 
	- Reduce the load on a compute service by storing media on s3
- Out-of-band pages 
	- Redirect users for custom page (for eg maintenance or outtage)