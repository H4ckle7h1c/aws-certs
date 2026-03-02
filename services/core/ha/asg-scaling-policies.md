ASG don't need scaling policies
- Manual scaling - min,max & desired
- Simple scaling - monitoring a single metric but inflexibale
- Step Scaling - define a sequence of steps to follow for scaling (eg if cpu 50-75% add)
- Target tracking : based on metric and target value, like cpu avg 50% 
- Scaling based on SQS - **ApproximateNumberOfMessagesVisible**

![[Pasted image 20260216140920.png]]


![[Pasted image 20260216140927.png]]
