# Classic Elastic Load Balancer

- A "classic" elastic load balancer is designed for **simple** balancing of
  traffic to multiple EC2 instances.
- There are no granular routing "rules" - all instances get routed to evenly,
  and no special routing request can be made based on specific content request
  from the user.
- Classic load balancing is best used when all instances (that are being served
  traffic) contain the same data.
