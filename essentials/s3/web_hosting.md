# S3 Static Web Hosting

- Amazon S3 provides an option for a low cost, highly reliable web hosting service
  for static websites (content that does not change frequently).

- When enabled, static web hosting will provide you with a unique endpoint (url)
  that you can point to any properly formatted file stored in an S3 bucket.
  Supported formats include:
  - HTML
  - CSS
  - JavaScript

- Amazon Route 53 can also map human-readable domain names to static web hosting
  buckets, which are ideal for DNS failover solutions.


#### Cross-Origin Resource Sharing (CORS)

- CORS is a method of allowing a web application located in one domain to access
  and use resources in another domain.

- This allows web applications running JavaScript or HTML5 to access resources
  in an S3 buckets without using a proxy server.

- For AWS, this (commonly) means that a web application hosted in one S3 bucket
  can access resources in another S3 bucket.
