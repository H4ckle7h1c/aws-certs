
![[Pasted image 20250623213217.png]]
By default disabled.
When enabled can't be disabled again just suspended

disabled -> enabled <-> suspended

Versioning : 
- every operation modify an object will create a new version
- when disabled **id** is null 
- when enable an **id** is allocated 
- Latest version / current version is the last 
- When deleting will add a deleting marker if we don't specify an id:
	- Special version of an object
- Hard delete an object --> specify the id of the particular object 
- Undelete an object -> undelete the delete marker

Key points : 
- Can't be switched off
- Consuming space for each version of the object (=billed for all those versions)

MFA delete : 
- Enabled in versioning configuration
- MFA is required to change bucket versioning state 
- MFA is required to delete versions 
- Serial number + code