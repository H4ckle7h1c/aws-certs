**Conditions** : 
![[Pasted image 20260302141117.png]]
**DependsOn**: Allows to establish 
![[Pasted image 20260302141732.png]]![[Pasted image 20260302141931.png]]
**WaitCondition**
Route cause, EC2 instance will be in `CreateComplete` long before the EC2 bootstrap is finished and CloudFormation has no way to know that. 
Cfn Signal is an utility that allow to send a signal back to cloudformation.
![[Pasted image 20260302143005.png]]

![[Pasted image 20260302143156.png]]
![[Pasted image 20260302142455.png]]

**Nested Stacks**
![[Pasted image 20260302143651.png]]
Stacks are isolated 
There is a limit of 500 ressources into stacks 

![[Pasted image 20260302143655.png]]
Templates are reused, not ressources.

![[Pasted image 20260302143659.png]]
When to use ? 
![[Pasted image 20260302144941.png]]
**Cross Stack References**
![[Pasted image 20260302145238.png]]
![[Pasted image 20260302145700.png]]
![[Pasted image 20260302145245.png]]