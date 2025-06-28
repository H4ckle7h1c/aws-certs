- Client-Side encryption :
	- e2e encryption from client -> s3 endpoint -> storage
- Server-Seive encryption : 
	- Data at rest encrpytion 
	- plain text user -> s3 endpoint
	- ciphertext s3-> s3 storage 

- 3 types of SSE : 
	- SSE-C : Encryption key provided by customer
		- Manages encryption
		- Delegating the cipher operation to s3
		- Give the plaintext and key to s3
		- Store ciphertext object & key hash
		- S3 is 'discarding' the key after use
		- To be used when we need to manage our keys
	- SSE-S3 (default) AES256: Amazon S3-Manages Keys
		- Manages encryption & keys
		- Generate a master 'key'
		- Generate an object-key to encrypt plaintext
		- Cipher the object key & discard the plaintext object-key
		- No control on the rotation of the keys, ...
		- Role separations = s3 admin can access the data
	- SSE-KMS: Keys stores in AWS KMS
		- Create, configure & manage permissions 
		- Same per object key but use the KMS manage key to cipher the object key
		- Role separation with Encryption / Decryption + access to kms key
			- Admin can manage key but if no decryption permission can't access the data

- SSE is now mandatory on objects in S3 

![[Pasted image 20250628152114.png]]
#security #sse