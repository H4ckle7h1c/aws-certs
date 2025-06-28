### Using SSE-KMS with S3

When using **S3 with SSE-KMS (Server-Side Encryption with AWS Key Management Service)**:
- Each time an object is uploaded to S3, AWS KMS is called to:
    - Generate a unique **Data Encryption Key (DEK)**.
    - Encrypt (cipher) the object using that DEK.
        

### Considerations

- **Cost**: Each KMS call incurs a charge, which can become expensive with high object upload volumes.
- **Throttling**: KMS has request limits. High volumes of encryption requests can lead to throttling, impacting performance.
    

### Solution: S3 Bucket Keys

- **S3 Bucket Keys** reduce the number of direct KMS calls.
- A **bucket-level DEK** is generated via KMS and used for a time-limited period to encrypt multiple objects.
- This improves **scalability** and reduces **cost** by minimizing KMS traffic.
- Replication preserve the settings including encryption ones 
- If replicating to a bucket using bucket keys, will encrypt the object in the destination (etag will change)