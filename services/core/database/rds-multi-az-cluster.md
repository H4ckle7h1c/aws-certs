![[Pasted image 20260112101642.png]]

Multiple ways to access the cluster : 
- cluster endpoint -> points at the writer 
- reader endpoint -> direct any read to an available reader
- instance endpoint -> each instance in the cluster got an endpoint (only use for testing)
Summary :
- 1 writer + 2 readers 
- Faster HW, graviton + nvme 
- Fast write to local storage then -> ebs 
- Readers can be used for read 
- Faster failover ~35s + transaction logs 
- Writes are commited when 1 reader has confirmed
