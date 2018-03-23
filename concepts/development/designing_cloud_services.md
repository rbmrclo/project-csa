# Designing Cloud Services & Best Practices

- **Design for failure**, and create self-healing application environments.
- Always design applications with instances **in at least two availability zones.**
- Guarantee that you have "reserved" capacity in the event of an emergency by
  purchasing reserved instances in a designated recovery availability zone (AWS
  does not guarantee on-demand instance capacity).
- Rigorously test to find single points fo failure and apply high availability.
- Always enable RDS Multi-AZ and automated backups (InnoDB table support only for MySQL)
- Utilize Elastic IP addresses for fail over to "stand-by" instances when auto
  scaling and load balancing are not available.

- Use Route 53 to implement failover DNS techniques that include:
  - Latency based routing
  - Failover DNS routing

- Have a disaster recovery and backup strategy that utilizes:
  - Multiple Regions
  - Maintain up to date AMI's (and copy AMI's from one region to another)
  - Copy EBS snapshots to other regions (use CRON jobs that take snapshots of EBS)
  - Automate everything in order to easily re-deploy resources in the event of a disaster.
  - Utilize bootstrapping to quickly bring up new instances with minimal
    configuration and allows for "generic" AMI's

- Decouple application components using services such as SQS (when available).
- "Throw away" old or broken instances.
- Utilize CloudWatch to monitor infrastructure changes and health.
- Utilize MultiPartUpload for S3 uploads (for objects over 100MB)
- Cache static content on Amazon CloudFront using EC2 or S3 Origins.
- Protect your data at rest using encrypted file systems or EBS/S3 encryption options.
- Connect to instances inside of the VPC using a bastion host or VPN connection.
- Use IAM roles on EC2 instances instead of using API keys.
- Never store API keys on an AMI
