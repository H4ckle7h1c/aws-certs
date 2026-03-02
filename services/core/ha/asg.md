ASG = Auto Scaling Groups

Often/Always used with elb

- It's automatic scaling and se
- Uses **Launch Templates** or **Configuration**
- Has **Minimum**, **Desired** and **Maximum** Size (e.g 1:2:4)
- Keep running instances at the desired capacity by provisioning or terminationg instances
- Scaling polices are used to automate based on metrics
![[Pasted image 20260216134702.png]]

![[Pasted image 20260216134745.png]]
ASG are linked to a subnet in a vpc.

## Scaling Policies
- **Manual** Scaling: Manually adjust the desired capacity
- **Scheduled** Scaling: Time based adjustment
- **Dynamic** Scaling:
	- **Simple**: rule based on a metric => 'CPU above 50% +1', 'CPU Below 50 -1', memory, disks io, ...
	- **Stepped** Scaling - Bigger +/- based on difference
	- **Target Tracking** - Desired aggregate cpu = 40%, asg handle it
- **Cooldown Periods**.. how long to wait before making an other scale 

EC2 also detects the status of the instances, if an instance fails, asg will replace it.

![[Pasted image 20260216135356.png]]

## Scaling processes
![[Pasted image 20260216135724.png]]
## Key Points
![[Pasted image 20260216135854.png]]