
'A' record = IP address -> name

cname = map name -> name (www.catagram.io => catagram.io)

But cname is invalid for naked/apex (catagram.io)

With cname - catagram.io -> elb is invalid


ALIAS : 

ALIAS record maps a name to AWS ressource
Can be used for nakes/apex and normal records 
There is no charge when a pointing to aws ressources 
For AWS service -> default picking ALIAS
Should be same type as the record it's pointing to 