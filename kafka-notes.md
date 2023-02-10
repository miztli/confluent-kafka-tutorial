
### Broker

- 

### Consumer

- acknowledgement: the broker waits until the consumer acknowledge the message

### Producer

- message delivery guarantees:
    
  - acks = 0 
    - at most 1
    - fire and forget
    - data loss
  - acks = 1
    - at least 1
    - producer waits for acknowledgement
    - higher latency
  - acks = all
    - ack happens once data is replicated across replicas
    - \+ durability
    - \- latency
  - acks = return ack when more than min.insync.replicas is reached

- idempotency
  - property: enable.idempotency = true
  - sequence is sent as metadata along the message

### Transaction coordinator:
