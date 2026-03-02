Elastic File System (EFS) is a managed implementation of NFS which allows for the creation of shared 'filesystems' which can be mounted within multi EC2 instances.

![[Pasted image 20260209103101.png]]
Implementation of NFSv4
Can be mounted in Linux 
Shared between multiple EC2 instances
Limitation for media (video, images,...)
By default isolated to a VPC and accessed via mount targets 
Can be accessed using VPN/Direct Connect for on-premises access
Linux Only
2 perf modes: GP(default for 99.9% users) and Max I/O (for //sation)
Throughput Modes: Bursting vs Provisioned
2 Storages classes : Standard (default) and infrequent access, lifecycle policies to move data between classes