# Route 53

- Route 53 is a domain management service (DNS hosting solution) provided by AWS.
- It can manage external DNS for domain routing - routing requests for `www.robbiemarcelo.com`
  to the proper AWS resources such as a CloudFront distribution, ELB, EC2
  instance, or RDS server.
- Route 53 can also be used to manage internal DNS for custom internal hostnames
  within a VPC as long as the VPC is configured for it.
- Latency, GEO, basic, and failover routing policies allow for region-to-region
  fault tolerant architecture design.
- You can easily configure for failover to S3 (if website bucket hosting is
  enabled) or CloudFront.

### Key Features

##### Domain Registration

- Basically, to register domain names (i.e robbiemarcelo.com)

##### Domain Name System (DNS) Service

- Translates friendly domain names like `www.robbiemarcelo.com` into IP addresses like `192.0.2.1`
- Amazon Route 53 responds to DNS queries using a global network of
  authoritative DNS servers which reduces latency.

##### Health Checking

- Amazon Route 53 sends automated requests over the Internet to your application
  to verify that it's reachable, available, and functional.
