Why using a proxy ? 
- Opening and Closing Connections consume ressources
- ...Takes time and create latency 
- With serverless (lambda...) a lot of open/close
- Handling db failure is hard and take management in our app
- DB proxies helps managing connection (scaling/resilience)
- Application(s) => Proxy (connection pooling) => Database
How : 
- Proxy maintain a long term connection pool
- Much quicker to establish connection to the db proxy
- Multiplexing is used 
- Prevent and manage the connection failover to the DB
When :
- Too many connections errors...
- Small instances or burst related (T2/T3)
- AWS Lambda -> cost saving by time saving while reusing the same connection
- Long running con (SAAS apps) - low latency
- Resilience to db failure is prio
- Reduce the **time for failover** event and make it **transparent** to the application
Key facts :
- Fully managed db proxy for rds/aurora
- Auto Scaling, highly available by default
- Provides connection pooling = reduce DB load
- ONLY accessible from a VPC
- Used a Proxy endpoint - no app changes
- Can enforce SSL/TLS
- Can reduce failover time by over 60% (mostly for aurora)
- Abstract failure away from our applications