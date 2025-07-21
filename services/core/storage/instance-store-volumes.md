Instance store volumes provides block storage devices
physically connected to one ec2 host 
instances on that host can access them 
hight storage performance in AWS 
included in instance price
**attached at launch time**

The virtual devices for instance store volumes are `ephemeral[0-23]`. Instance types that support one instance store volume have `ephemeral0`. Instance types that support two instance store volumes have `ephemeral0` and `ephemeral1`, and so on.


Instance storage optimized : 
- D3 - 4.6GBps throughput 
- I3 (nvme) = 16GBps 

Take home :
- Local to EC2 host 
- Attached at launch only 
- Lost on instance move, resize, or HW failure
- High perf
- You pay for it anyway
- Temporary
