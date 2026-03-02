3 ways an elb can maintain ssl session :

- Bridging:
	- 1 client create one or more connections to the ELB
	- Connection is terminated on the elb and needs a certificate for the domain name
	- ELB initiates new SSL connection to BE
	- Every EC2 instance in the BE need to perform crypto operations -> warning at scale
- Pass-through:
	- Client connects but the NLB doesn't decrypt the connection and pass it to the isntance
	- Instance still has the SSL cert instance
	- Layer 4 level
	- Entirely cert managed by us
- Offload:
	- Client connects to the ELB 
	- ELB use HTTP to connect to the EC2 
	- No certificate on the EC2 instance
- ![[Pasted image 20260216143822.png]]

Using stateless app that's fine but if state is required we need to centralize the state.
A feature is using cookie at the elb level so sessions are always sent to the same service.
Server failure = breaks the stickiness as user is sent to a new server
Cookie expiracy = new server allocated to a user session
=> uneven load at the backend level

![[Pasted image 20260216143115.png]]