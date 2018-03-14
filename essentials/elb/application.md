# Application Elastic Load Balancer

- An "Application" elastic load balancer is designed for **complex** balancing
  of traffic to multiple EC2 instances using **Content-based** rules.
- Content-based rules (setup on the listener) can be configured using:
  - **Host-based rules**: Route traffic based on the host field of the HTTP header
  - **Path-based rules**: Route traffic based on the ULR path of the HTTP header
  - This allows you to structure your application as smaller services, and even
    monitor/auto-scale based on traffic to specific **target groups**.
- An Application ELB also supports ECS Containers, HTTPS, HTTP/2, WebSockets,
  Access Logs, Sticky Sessions, and AWS WAF (Web Application Firewall).
