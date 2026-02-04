Scalable ACU - Aurora Capacity Units
Aurora Serveless cluster has min & max ACU
Adjusts based on load
Can go to 0 and be paused
Comsuption billing per-second basis
Same resilience as Aurora (6 copies across AZs)


Serverless vs Provisioned

![[Pasted image 20260115112144.png]]
- Based n the load ACU are dynamically increased/decreased 
- Proxy fleet is managed to have a fluid scaling as it managed the connections to ACU
- Proxy fleed is managed by AWS
- Customer is managing the min/max ACU

Type of applications : 
- Infrequently used applications
- New application (unsured about the size of the instance)
- Variable workload
- Unpredictable workloads
- Dev and tests db
- Multi-tenant app