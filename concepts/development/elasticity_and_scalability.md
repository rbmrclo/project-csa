# Elasticity and Scalability

- **Proactive Cycle Scaling**: Scaling that occurs at a fixed interval.
- **Proactive Event-based scaling**: Scaling that occurs in anticipation of an event.
- **Auto-scaling based on demand**: Scaling that occurs based off of increase in
  demand for the application.

- Plan to scale out rather than up (Horizontal Scaling):
  - Add more instances to handle increases in capacity rather than increasing instance size.
  - Be sure to design for the proper instance size to start.
  - Use tools like Auto Scaling and ELB.
  - A scaled service should be fault tolerant and operationally efficient.
  - Scalable service should become more cost effective as it grows.

- DynamoDB is a fully managed NoSQL services from AWS.
  - With high availability and scaling already built in.
  - All the developer has to do is specify required throughput for the tables.

- RDS requires scaling in a few different ways:
  - RDS does not support a cluster of instances to load balance traffic across.
  - Because of this, there are few different methods to scale traffic with RDS:
    - Utilize read replicas to offload heavy read only traffic.
    - Increase the instance size to handle increase in load.
    - Utilize ElastiCache clusters for caching database session information.
