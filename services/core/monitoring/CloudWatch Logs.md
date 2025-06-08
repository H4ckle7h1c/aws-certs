
- Public Service 
- Store, Monitor, access Logging data
- Built-in integration with other services : EC2, VPC flow logs, Lambda, Cloudtrail, R53, ...

Others services need role to write logs.

2 ways 
- AWS Service integration 
- Unified CW agent

Can generate metrics based on logs - metric filter 

![[Pasted image 20250608191633.png]]

- 1 log stream (/var/log/messages for 1 instance) is an order set of a log events for a specific source for a specific thing
- 1 log group is a container of multiple log stream