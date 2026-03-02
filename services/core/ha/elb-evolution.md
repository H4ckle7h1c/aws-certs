There are 3 types of ELB in aws 
Splitted between v1(avoid) and v2 (prefer)
CLB classical lb V1 -> 2009
	No layer 7, 1 ssl per clb.
V2 : 
- Application Load Balancer (ALB) - v2 - http/https/websocket
- Network Load balancer - tcp/tls & udp
- Faster, cheaper, and support target groups and rules 