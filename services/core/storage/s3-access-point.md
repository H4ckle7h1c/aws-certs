Purpose : 
- Simplifying managing access to S3 bucket/objects
- Rather than 1 bucket w/ 1 policy 
- create many ap
	- with a dedicated policy for each
	- different network access controls
- `aws s3control create-access-point --name xxx --account-id xxx --bucket xxx`
- Each access point has a unique `DNS` address ...