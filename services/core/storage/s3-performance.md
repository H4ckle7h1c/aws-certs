- Default PUT uploads :
	- Single data stream to s3 - PUT
	- Upload fails : require full restart 
	- Speed & reliability = limit of 1 stream
	- Limited to uploads up to 5GB
- Multiplart Upload :
	- Data is broken up 
	- At least 100MB
	- Max 10,000 parts from 5MB to 5GB
	- Last part can be < 5MB
	- Each part can be restarted if fails 
	- Transfert rate = sum of each individial parts
- S3 Accelerated transfer (by default fault):
	- When off use public internet routing
	- When on use edge locations to use AWS network
	- S3 need to be dns compatible in the domain name
	- Edge locations are direct access to the 
	- Furthest the customer is better transfer acceleration will work

https://s3-accelerate-speedtest.s3-accelerate.amazonaws.com/en/accelerate-speed-comparsion.html