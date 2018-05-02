# Synopsis

## Whitepapers

- [AWS Storage Services Overview](https://d0.awsstatic.com/whitepapers/Storage/AWS%20Storage%20Services%20Whitepaper-v9.pdf)

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

#### S3 Protecting Data Using Server-Side Encryption

- Use **Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3)** - each
  object is encrypted with a unique key employing strong multi-factor
  encryption.
  - It encrypts the key itself with a master key that `it regularly rotates`.
  - S3 server-side encrption uses one of the strongest block ciphers available,
    256-bit Advanced Encryption Standard (AES-256), to encrypt your data.
  - Ref: https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingServerSideEncryption.html

- Use **Server-Side Encrption with AWS KMS-Managed Keys (SSE-KMS)** - similar to
  SSE-S3, but with some additional benefits along with some additional charges
  for using this service.
  - There are separate permissions for the use of an `envelope key` (that is,
    a key that protects your data's encryption key) that provides added
    protection against unauthorized access of your objects in S3.
  - SSE-KMS also provides you with an audit trail of when your key was used and
    by whom.
  - Additionally, you have the option to create and manage encryption keys
    yourself, or use a default key that is unique to you, the service you're
    using, and the region you're working in.
  - Ref: https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingKMSEncryption.html


