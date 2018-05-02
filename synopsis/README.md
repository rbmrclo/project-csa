# Synopsis

#### S3 Request Rate and Performance Considerations

- Workloads that include a mix of request types (GET, PUT, DELETE, or GET
  Bucket), choosing appropriate key names for your objects ensures better
  performance by providing low-latency access to the Amazon S3 index. It also
  ensures scalability regardless of the number of requests you send per second.
  - Example 1: Add a **`Hex Hash Prefix`** to Key Name
  - Example 2: **`Reverse``** the Key Name String

- Workloads that are GET-intensive - If the bulk of your workload consists of
  GET requests, we recommend using the Amazon CloudFront content delivery
  service.
  - You should use Amazon CloudFront for performance optimization.
  - You will also send fewer direct requests to Amazon S3, which will reduce
    your costs.
  - Example: Suppose that you have a few objects that are very popular.
    CloudFront fetches those objects from Amazon S3 and caches them. CloudFront
    can then serve future requests for the objects from its cache, reducing the
    number of GET requests it sends to Amazon S3.

- Reference: https://docs.aws.amazon.com/AmazonS3/latest/dev/request-rate-perf-considerations.html
