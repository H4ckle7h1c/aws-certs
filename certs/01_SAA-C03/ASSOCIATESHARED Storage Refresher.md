[Direct attached storage] : 
- Attached to EC2 instance directly
- If physical device fails, data is lost

[Network attached storage] : 
- Delivered over the network (EBS)

[Ephemeral Storage] : 
- Temp 

[Persistent storage] : 
- Live past on the lifetime of the instance

[Block Storage] :
- Volume presented to the OS as a collection of blocks, no structure provided. 
- Usually a FS is installed
- Mountable
- Bootable. 

[File Storage] : 
- Presented as a file share with a structure. Mountable but not Bootable.
[Object Storage] :
- Collection of flat objects
- Not mountable 
- Not bootable


Storage Performance : 
IO (block) size X IOPS = Throughput

![[Pasted image 20250702092536.png]]
