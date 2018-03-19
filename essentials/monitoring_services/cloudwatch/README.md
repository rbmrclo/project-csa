# CloudWatch

- Cloudwatch is used to monitor AWS services, such as EC2, ELB and S3.
- You monitor your environment by configuring and viewing CloudWatch metrics.
- Metrics are specific to each AWS service or resource, and include such metrics as:
  - EC2 per-instance metrics:
    - CPUUtilization
    - CPUCreditUsage
  - S3 Metrics
    - NumberOfObjects
    - BucketSizeBytes
  - ELB Metrics
    - RequestCount
    - UnhealthyHostCount

- Detailed vs. Basic Level Monitoring:
  - Basic: Data is available automatically in 5-minute periods at no charge
  - Detailed: Data is available in 1-minute periods

- CloudWatch Alarms can be created to trigger alerts (or other actions in your
  AWS accounts, such as an SNS topic), based on threshold you set on CloudWatch metrics.
- Auto Scaling heavily utilizes CloudWatch - relying on the threshold and alarms
  to trigger the addition (or removal) of instances from an auto scaling group.
