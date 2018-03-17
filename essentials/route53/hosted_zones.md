# Route 53 Hosted Zones

- A Hosted Zones stores DNS records for your domain.
- Basically, it contains all the rules (record sets) that tells Route 53 what to
  do with DNS request.

- There are both public and private hosted zones:
  - A **public hosted zone** is a container that holds information about how you
    want to route traffic on the Internet for a domain, such as `robbiemarcelo.com`, and its subdomains.
  - A **private hosted zone** is a container that holds information about how you want
    to route traffic for a domain and its subdomains within one or more Amazon Virtual Private Clouds.

- After you create a hosted zone for your domain, you create resource record
  sets to tell the Domain Name System (DNS) how you want traffic to be routed
  for that domain.

- Hosted zones come pre-populated with NS (name server) and SOA (start of
  authority) record sets.
