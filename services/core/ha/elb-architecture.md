![[Pasted image 20260212134302.png]]
Internet facing LB can communicate with public & private EC2 instances. Recommended at least /27
subnet bc they need at least 8+ ip. 
/28 works but bare minimum

![[Pasted image 20260212134309.png]]


![[Pasted image 20260212134313.png]]Cross-zone LB = allow LB to distribute load to all the instances registered across the AZ (enabled by default now)

![[Pasted image 20260213134824.png]]
