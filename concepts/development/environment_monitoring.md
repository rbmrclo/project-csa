# AWS Environment Monitoring

### Use CloudWatch for

- Shutting down inactive instances
- Monitoring changes in your AWS environment with CloudTrail integration
- Monitor instances resources and create alarms based off of usage and availability:
  - EC2 instances have "basic" monitoring which CloudWatch supports out of the
    box, and includes all metrics that can be monitored at the hypervisor level.
  - Status Checks which can automate the recovery of failed status checks by
    stopping and starting the instance again.
  - EC2 metrics that include custom scripts to work with CloudWatch:
    - Disk Usage; Available Disk Space
    - Swap Usage; Available Swap
    - Memory Usage; Available Memory

### Use CloudTrail for

- Security and compliance
- Monitoring all actions taken against the AWS account.
- Monitoring (and being notified) of changes to IAM accounts (with CloudWatch/SNS integration)
- Viewing what API Keys/Users performed any given API action against an
  environment (i.e view what user terminated a set of instances or an individual instance)
- Fulfilling auditing requirements inside of organizations.

### Use AWS Config for

- Receiving detailed configuration information about an AWS environment.
- Taking a point in time "snaphot" of all supported AWS resources to determine
  the state of your environment.
- Viewing historical configurations within your environment by viewing the "snapshots"
- Receiving notifications whenever resources are created, modified, or deleted.
- Viewing relationships between resources, i.e which EC2 instances an EBS volume
  is attached too.
