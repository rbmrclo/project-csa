# CloudFront

- CloudFront is a global CDN which delivers content from an "origin" location
  (the source of the content) to an "edge" location (AWS CDN data center).

- CloudFront can integrate with Route 53 for "alternative" CNAMEs.
  - This allows you to create a URL such as `http://cdn.example.com` that works
    with your distribution.

### Benefits

- Users experience lower latency and content load time.
- Reduces load on your applications resources (origin services) - thus reducing cost.

### Updating cached files

- Caching is done based off the object name
- In order to serve a new version of an object, either create a new object with
  a new name or create an "invalidation" on the CloudFront distribution based
  off the object name.
- "Invalidations" have a cost, so if you have to invalidate a large CloudFront
  distribution then perhaps you should just create a new distribution and move
  DNS names.
- cached objects can also be set with a specific expiration time/date, or set to
  not cache at all.

### Signed URLs

- Signed URLs allow access to "private content" by creating a temporary,
  one-time use URL based off the number of seconds you want it to be accessible.
- Signed with a `X.509` certificate

### Origin

- An origin location is the source of the content (static objects)
- An origin can be an:
  - S3 Bucket
  - Elastic Load Balancer that distributes requests among origin EC2 instances.

### Edge Location

- An edge location allows the caching of static objects from the origin location.
- An edge location is an AWS datacenter which does not contain AWS services.
- Instead, it used to deliver content to parts of the world.

- An example would be CloudFront, which is a CDN.
  - Cached items such as PDF file can be cached on an edge location which
    reduces the amount of "space/time/latency" required for a request from that
    part of the world.

