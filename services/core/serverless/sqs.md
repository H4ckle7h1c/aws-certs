- Public service 
- Fully managed, highly-available, regional resilient 
- FIFO or Standard
- Max msg size = 256 kB
- Received MSG = msg are hidden (visibility timeout = time the processor has to process a msg)
- The consumer has to delete the msg from the queue, otherwise will reappear
- **Dead-Letter** queues can be used for pb msg


![[Pasted image 20260128104649.png]]
ASG = autoscaling groups 
Continuously monitoring the length of the queue and scale the worker pool based on amount of msg to process.


![[Pasted image 20260128104654.png]]

When 1 input = multiple output -> fanout 
1 sqs queue is subscribing to each type of output 
Only 1 event is generated for an upload so


Standard = at-least once, FIFO = exactly-once

FIFO (Perf) 3,000 msg per s with batching or up to 300 per s without 
Billed based on requets 
1 request = 1-10 msg up to 64KB total
Not cost effective if we poll it recently 
Short (immediate) vs Long (waitTimeSeconds) Polling
Can wait up to 14days 
Encryption at rests exists for data at rest (long waiting msg) & in-transit
queue policy


Standard vs FIFO

- Performance traded for order 
- Need .fifo suffix 

![[Pasted image 20260128110730.png]]