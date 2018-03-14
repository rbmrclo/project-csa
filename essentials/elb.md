# Elastic Load Balancer (ELB)

- **Load Balancing** (as a concept) is a common method used for distributing
  incoming traffic among servers.
- An **Elastic Load Balancer** is an EC2 service that automates the process of
  distributing incoming traffic (evenly) to all the instances that are
  associated with the ELB.
- An elastic load balancer can load balance traffic to multiple EC2 instances
  located across multiple availability zones.
  - This allows for highly available and fault tolerant architecture.
- Elastic load balancing should be paired with **Auto Scaling** to enhance high
  availability and fault tolerance, AND allow for automated scalability and
  elasticity.
- An ELB has it's own DNS record set that allows for direct access from the open
  internet access.

#### Important facts

- When used within a VPC, an ELB can act as an internal load balancer and load
  balance to internal EC2 instances on private subnets (as often done with
  multi-tier applications).
- ELBs will automatically stop serving traffic to an instance that becomes
  unhealthy (via health checks)
- An ELB can help reduce compute power on an EC2 instance by allowing for an SSL
  certificate to be applied directly to the elastic load balancer.
