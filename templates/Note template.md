# {{ServiceName}}

---
### Scope & Resilience  
- **Service Type**: Public / Private  
- **Scope**: Global / Regional / AZ-Scoped  
- **Resilience Level**:  
  - AZ-resilient ✅  
  - Region-resilient ✅ / ❌  
  - Global-resilient ✅ / ❌

---
### Purpose  
Briefly describe why this service exists and what problems it solves.

---

### What is it?  
A concise description of the service.

---

### Access  
- CLI  
- Console (GUI)  
- SDK / API  

---

### Core Concepts  
- **Concept 1**: Description  
- **Concept 2**: Description  
- **Concept 3**: Description  

*(Add more as needed)*

---

### Key Features  
- Feature 1  
- Feature 2  
- Feature 3  

---

### Important Terms  
| Term         | Definition or Explanation                | Notes / Links            |
|--------------|------------------------------------------|--------------------------|
| [[Namespace]] | Container for monitoring data             | Related to CloudWatch    |
| [[Metric]]    | Time-series data points                    |                          |
| [[Dimension]] | Key-value pairs to filter metrics          |                          |

---

### Usage Examples / Commands  
```bash
# Example CLI command or usage
aws cloudwatch get-metric-statistics --metric-name CPUUtilization --namespace AWS/EC2 ...
