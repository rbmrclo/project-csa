# S3 for DNS Failover

- By using a failover routing policy in a Route 53 DNS record set, an S3 bucket
  can be used as a failover endpoint.

- This can provide an extremely reliable backup solution if your primary
  endpoint fails.

- And even though S3 should only be used for static web hosting, it gives you
  the opportunity to provide your users with some type of information until the
  primary endpoint is working again.

- An S3 bucket can also be used as a primary endpoint, if you just want to host
  a simple static site.


##### Note

For a DNS record to use an S3 bucket as an endpoint, the bucket name MUST be the same as the domain name.
