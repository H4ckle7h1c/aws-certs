Amazon EC2 Auto Scaling can determine the health status of an instance using one or more of the following:

- Status checks provided by Amazon EC2 to identify hardware and software issues that may impair an instance. The default health checks for an Auto Scaling group are EC2 status checks only.
- Health checks provided by Elastic Load Balancing (ELB). These health checks are disabled by default but can be enabled.
- Your custom health checks.


The goals is to automatically heal an asg: 

![[Pasted image 20260216142856.png]]
If health check grace period is too short maybe the app did not finish loading/configuring in the adequate time.
