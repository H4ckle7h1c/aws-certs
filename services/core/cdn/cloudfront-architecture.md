Terms : 
- Origin : the source location of the content (S3/Custom Origin)
- Distribution: The configuration unit of CloudFront
- EdgeLocation: Local cache of data
- Regional Edge cache: (less than Edge locations), larger versions of an edge location. Provide an other layer of cache 

![[Pasted image 20260129092033.png]]

First -> check edge
If edge doesn't have the object -> Regional Edge
If not origin fetch from S3

Cloud Front read only, no write for caching.

![[Pasted image 20260129093013.png]]
