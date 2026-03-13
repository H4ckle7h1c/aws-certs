
---

### 🧩 Definition  
High Availability is the practice of **designing systems to ensure a defined level of performance and uptime** over an extended period — even in the face of failure.  
It aims to **minimize disruption time** and **keep systems continuously available**.

---

### 🎯 Goal  
- **Maximize uptime**  (or minimise any outage)
- Avoid system-wide failures  
- Reduce the impact of outages on users  

---

### ⚙️ How?  
- Use **redundant infrastructure**  
- Implement **failover mechanisms**  
- Have **spare equipment** (e.g., standby servers) ready to take over

---

### 🔢 Availability Levels  

| Availability | Downtime per Year      |
|--------------|------------------------|
| 99.9% (3 nines)   | ~8.77 hours              |
| 99.99% (4 nines)  | ~52.6 minutes            |
| 99.999% (5 nines) | ~5.26 minutes            |

---

### 💡 Solutions & Examples  
- One **standby server** ready to take over if the main one fails  
- **Multi-AZ deployments** in AWS  
- **Load Balancers** to distribute traffic across healthy instances  
- **Auto Scaling** groups for instance replacement

---

### Related Concepts  
- [[Fault Tolerance]]  
- [[Disaster Recovery (DR)]]  
- [[Elastic Load Balancing]()]()
