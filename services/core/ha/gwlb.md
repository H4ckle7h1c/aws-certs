![[Pasted image 20260216144313.png]]
In the case of multi tenant application = App + Secu are tied together 

![[Pasted image 20260216144318.png]]
Helps to run and scale 3rd party appliances, like FW, ids, ... 
With geneve they keep the same ip src,dst, creation time, ... 
Flow stickiness, 1 flow = 1 appliance

![[Pasted image 20260216144819.png]]

![[Pasted image 20260216144322.png]]In point 4, packets are encapsulated in Geneve protocol and return in 5 unaltered after security checks 