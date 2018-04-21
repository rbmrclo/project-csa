# Simple Storage Service (S3)

An AWS main storage service, S3 can serve many purposes when designing highly
available, fault tolerant, and secure application architecture. Including:

- Bulk (basically unlimited) static object storage
- Various **storage classes** to optimize cost vs. needed object availability/durability
- Object versioning
- Access restrictions via S3 bucket policies/permissions
- Object management via lifecycle policies
- Hosting static files & websites
- Origin for CloudFront CDN
- File shares and backup/archiving for hybrid networks (via AWS Storage Gateway)

### Important Facts

- Objects stay within an AWS region and are synced across all AZ's for extremely
  high availability and durability.
- You should always create an S3 bucket in a region that makes sense to it's purpose:
  - Serving content to customers
  - Sharing Data with EC2

### S3 Read Consistency Rules

- All regions now support read-after-write consistency for PUTS of new objects into s3.
  - Object can be immediately available after "putting" an object in S3.
- All regions use eventual consistency for PUTS overwriting existing objects and
  DELETES of objects.

