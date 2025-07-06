### 🟢 **S3 Standard (Default)**

- **Durability**: 99.999999999% (11 9s)
    
- **Availability**: Data is stored across **at least 3 Availability Zones (AZs)**
    
- **Data Integrity**: Uses **Content-MD5 checksums** and **CRCs** for consistency checks
    
- **Replication**: Automatically replicates data across 3 AZs
    
- **Billing**:
    
    - Charged **per GB per month (GB/m)**
        
    - **Data transfer out** is billed separately per GB
        
    - Charges apply **per 1,000 requests**
        
    - **No retrieval fees**
        
- **Performance**: Low latency; optimized for **frequent access**
    
- **Use Case**: Frequently accessed, critical data with high durability and availability needs
    

---

### 🟡 **S3 Standard-IA (Infrequent Access)**

- **Durability & AZs**: Same as S3 Standard (11 9s, across 3 AZs)
    
- **Cost**: ~50% cheaper than S3 Standard
    
- **Retrieval Fee**: Charged **per GB of data retrieved**
    
- **Minimums**:
    
    - **30-day storage charge** applies, even if deleted earlier
        
    - **128 KB minimum object size**
        
- **Use Case**: Long-lived data that is **accessed infrequently** but must remain **highly durable**
    

---

### 🟠 **S3 One Zone-IA**

- **Durability**: Lower than Standard-IA (still high, but only in 1 AZ)
    
- **Storage**: Stored in **a single AZ only** (no replication across AZs)
    
- **Other specs**: Same cost and retrieval behavior as Standard-IA
    
- **Use Case**: Long-lived, **non-critical**, replaceable data with **infrequent access** (e.g., backups, secondary copies)


---

### 🧊 **S3 Glacier Instant Retrieval**

- **Purpose**: Designed for **long-lived, rarely accessed data** that still needs **immediate access** when requested.
- **Access Time**: **Milliseconds** (same as S3 Standard-IA)
- **Durability**: 99.999999999% (11 9s), like other S3 storage classes
- **Minimum Storage Duration**: **90 days**
    - You'll be charged for 90 days of storage even if the object is deleted earlier.
- **Cost Considerations**:
    - Lower cost per GB than S3 Standard-IA
    - **Retrieval fees apply** (per GB)        
- **Recommended Usage**:
    - Data that is accessed **once per quarter or less**
    - Suitable for archives that require **instant access** (e.g., compliance data, active archives)
---
### 🧊 **S3 Glacier Flexible**

- **Purpose**:  
    Designed for **archival storage** that still requires **immediate access**.  
    Data is stored across **3 Availability Zones**, providing high durability and availability.
- **Access Time**:  
    **Milliseconds** — same as **S3 Standard-IA**, suitable for on-demand access.
- **Durability**:  
    **99.999999999% (11 9s)** — consistent with all S3 storage classes.
- **Minimum Storage Duration**:  
    **90 days** — you are charged for 90 days even if the object is deleted earlier. 
- **Minimum Storage Size**:  40KB
- **Retrivals jobs types**: 
	- Expedited (1-5minutes)
	- Standard (3-5hours)
	- Bulk (5-12hours)
	- Faster = more expensive
	- First byte latency = minute or hours 

S3 Glacier Deep Archive : 
- Data in a frozen state : 
	- 40 KB min size 
	- 180 day min duration
	- No publicly accessible objects
- Retrieval : 
	- Standard (12 hours)
	- Bulk (up to 48hours)
- Purpose : 
	- Rarely if ever need to be accessed
	- Hours of days for retrievals
	- (Legal or regulation)

---

S3 Intelligent-Tiering
- Multiple layer of storage
	- Frequent acces
	- Infrequence access 
	- Archive IA
	- Archive access
	- Deep Archive
- Purpose : 
	- Monitors and moves automatically objects not accessed for 30 days to low cost infrequent access tier and eventually archive instant acces or lower 
![[Pasted image 20250628161101.png]]
