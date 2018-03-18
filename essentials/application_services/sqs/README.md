# Simple Queue Service

- SQS provides the ability to have hosted/highly available queries that can be
  used for messages being sent between servers.
- This allows for the creation of distributed/decoupled application components.
- SQS is used to create decoupled application environments.
- Messages between servers are retrieved through polling.

### Types of Polling

##### Long Polling (1-20 seconds)

- Allows the SQS service to wait until a message is available in a queue before
  sending a response, and will return all messages from all SQS services.
- Long polling reduces API requests (over using short polling).

##### Short Polling

- SQS samples a subset of servers and returns messages from just those servers.
- Will not return all possible messages in a poll.
- Increases API requests (over long polling), which increases costs.

### Important Facts

- Each message can contain up to 256KB of text (in any format)
- Amazon SQS offer two different types of queues:
  - **Standard Queue**: Guarantees delivery of each message at least once BUT
    DOES NOT guarantee the order (best effort) in which they are delivered to
    the queue.
  - **First-in-first-out (FIFO) Queue**: Designed for applications where the
    order of operations and events is critical, or where duplicates can't be
    tolerated.
- SQS is also highly available and redundant.

### SQS Workflow

- Generally a "worker" instance will "poll" a queue to retrieve waiting messages for processing.
- Auto Scaling can be applied based off of queue size so that if a component of
  your application has an increase in demand, the number of worker instances can increase.
