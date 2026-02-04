![[Pasted image 20260129094657.png]]

When updating the original object.
Object stays as long as it's expiracy date is not reached
- When reached fetches the origin :
	- 304: not modified
	- 200 + new object : modified
Cache HITS = lower origin load
Default TTL = 24hours -> defined at the behaviour level
2 other values : 
- minimum ttl
- maximum ttl
Origin Headers : 
- Cache-Control max-age (seconds)
- Cache-Control s-age (seconds)
- Expires (date & time)

Cache Invalidation -> Performed on a distribution
Applies to all edge locations -> takes time 
Are defined by a path
Only use to correct data (not operational behavior)

Use versionned file names instead (!= S3 versionning)