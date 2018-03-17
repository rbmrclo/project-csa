# Route 53 Record Sets

- Record sets are instructions that actually match domain names to IP addresses.
- Record sets are comprised of various options, including:
  - Record type
  - Standard / alias
  - Routing policy
  - Evaluate target health

#### Common record types include:

| Record Type | Description |
| ----------- | ----------- |
| A           | Used to point a domain to an IPv4 IP address |
| AAAA        | Used to point a domain to an IPv6 IP address |
| CNAME       | Used to point a host/name to another host/name |
| MX          | Used to route email (mail exchange) |

#### Alias Record Sets

Instead of an IP address (standard record sets), an **alias** record set
contains a pointer to an AWS specific resource, such as:

- An elastic load balancer
- CloudFront distribution
- Elastic Beanstalk environment
- Amazon S3 bucket that is configured as a static website

#### Routing Policy


| Policy | Description |
| ----------- | ----------- |
| Simple      | Route all traffic to one endpoint |
| Weighted    | Route traffic to multiple endpoints (manual load balancing) |
| Latency     | Route traffic to an endpoint based on the users latency to various endpoints |
| Failover    | Route traffic to a "secondary" endpoint if the "primary" is unavailable |
| Geolocation | Route traffic to an endpoint based on the geographical location of the user |

#### Evaluate Health Check

- Can monitor the health of your application and trigger an action
