Be careful bc the **enqueue timestamp** of the msg is unchanged and used for the retention period 

Let's say a msg is send 1 day after being queued into the dlq and the max retention period is 2 days -> will remain only 1 more day in the dlq