https://docs.aws.amazon.com/AmazonS3/latest/userguide/replication-what-is-isnot-replicated.html
https://docs.aws.amazon.com/AmazonS3/latest/userguide/replication.html
### S3 Replication Types

- **Same-Region Replication (SRR):**  
    Source and destination buckets are in the **same AWS region**.
    
- **Cross-Region Replication (CRR):**  
    Source and destination buckets are in **different AWS regions**.
    

---

### Account Considerations for Replication

- **Same Account:**  
    Replication is straightforward as the source and destination buckets are managed within the same AWS account.
    
- **Different Accounts:**
    
    - The **destination account must trust the IAM role** used by the source account to perform replication.
        
    - To enable this, you need to add a **bucket policy on the destination bucket** that explicitly **trusts the source account’s replication role**.
---
## S3 Replication Option
- We can define all objets or a subset 
- Storage Class : default is the same
- Ownership : default is the source account  (if different accounts the owner is the other aws account but can be overriden to by default give ownership to the dest account)
- Replication Time Control (SLA) the replication time is 15 mins when activated

Key points : 
- By default not retroactive & versionning has to be enabled
- Batch replication can be used (to replicate existing objects)
- One-way replication (or bi-directionnal)
- Unencrypted, SSE-S3 & SSE-KMS (with extra config), SSE-C
- No Glacier/Glacier Deep Archive
- NO DELETES markers are enabled by default