# DDoS Mitigation

- When mitigating aginst DOS/DDOS attacks, use the same practice you would use
  on your on-premise components:
  - Firewalls:
    - Security groups
    - Network access control lists
    - Host-based firewalls
  - Web Application Firewalls (WAF)
  - Host-based or inline IDS/IPS (Trend Micro)
  - Traffic shaping/rate limiting

- Along with your traditional approaches for DoS/DDoS attack mitigation, AWS
  provides capabilities based on its elasticity:
  - You can potentially use CloudFront to absorb DoS/DDoS flooding attacks.
  - A potential attackers trying to attack content behind a CloudFront
    distribution is likely to send most requests to CloudFront edge locations,
    where the AWS infrastructure will absorb the extra requests with minimal to
    no impact on the back-end customer web servers.

- We must have permission to do Port Scanning on any of your EC2 instances.
- INGRESS filtering on all incoming traffic onto their network.
