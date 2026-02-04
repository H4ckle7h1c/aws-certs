

VPC minimum is **/28** (16 IPs), and maximum is **/16** (65536 Ips)
Avoid common ranges 

1 VPC = 1 region

- Custom VPC: 
	- VPC is a regional service
	- Isolated network
	- Nothing **IN** or **OUT** without explicit configuration
	- Hybrid networking (for on-premises)
	- IPv4 Private CIDR Blocks:
		- Each private VPC has a dedicated IPv4
		- Min /28 and Max /16 
		- Optional secondary IPv4
		- Optional single assigned IPv6 /56 CIDR Block
	- DNS : 
		- Provided by R53
		- IP@ is Base IP +2, 192.168.1.0/24 -> 192.168.1.2
		- enableDnsHostnames -> gives instances DNS names
		- enableDnsSupport -> enable dns resolution in VPC