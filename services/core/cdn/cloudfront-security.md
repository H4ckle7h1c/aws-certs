Origin: Origin of the data
Network: CF network -> edge location
Public: Customer/Viewer side

![[Pasted image 20260202143604.png]]

oai: Origin Access Identity

OAI is a type of identity -> can be **associated** with CF Distribution
CF becomes the OAI and this OAI can be used in **S3 Bucket Policies**
On a general basis **DENY** all but allo one or more **OAI's**

![[Pasted image 20260202143855.png]]



![[Pasted image 20260202144130.png]]If the call go though the CF distributionm Custom headers will be injected