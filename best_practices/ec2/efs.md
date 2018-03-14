# Elastic File System (EFS)

- EFS is a storage option for EC2 that allows for a scalable storage option.
- EFS storage capacity is elastic.
  - The storage capacity will increase and decrease as you add or remove files.
  - Applications running on an EC2 instance using EFS will always have the
    storage they need, without having to provision and attach larger storage
    devices.
- EFS is fully-managed (no maintenance required)
- Supports the Network File System version 4.0 and 4.1 (NFSv4) protocols when mounting.
- Best performance when using an EC2 AMI with Linux kernel 4.0 or newer.

### Benefits of EFS

- The EFS file system can be accessed by one (or more) EC2 instance at the same time.
  - Shared file access across all your EC2 instances.
  - Application that span multiple EC2 instances can access the same data.
- EFS file systems can be mounted to on-premises servers (when connected to your VPC via AWS Direct Connect).
  - This allows you to migrate data from on-premise servers to EFS and/or use it
    as a backup solution.
- EFS can scale to petabytes in size, while maintaining low latency and high levels of throughput.
- You pay only for the amount of storage you are using.

### Security

- Control file system access through POSIX permissions.
- VPC for network access control, and IAM for API access control.
- Encrypt data at rest using AWS Key Management Service (KMS).

### When to use?

- Big Data and analytics
- Media processing workflows
- Web Serving & Content Management
