# Auto Scaling

- **Auto Scaling** is a service (and method) provided by AWS that automates the
  process of increasing or decreasing the number of provisioned on-demand
  instances available for your application.
- Auto scaling will increase or decrease the amount of instances based on chosen **Cloudwatch** metrics.
- For example: If your application's demand increases un-expectantly,
  auto-scaling can automatically scale up (add instance) to meet the demand and
  terminate instances when the demand decreases.
  - This is known as **elasticity** in the AWS environment.

### Auto scaling has two main components

#### `Launch Configuration`

The EC2 "template" used when the auto scaling group needs to provision an
additional instance (i.e AMI, instance type, user data, storage, security groups, etc)

#### `Auto Scaling Group`

All the rules and settings that govern if/when an EC2 instance is automaticall
provisioned or terminated.

- Number of MIN & MAX allows instances
- VPC & AZ to launch instances into
- If provisioned instances should receive traffic from a ELB
- Scaling policies (cloudwatch metrics thresholds that trigger scaling)
- SNS notifications (to keep you informed when scaling occurs)

### Best practice

For architecture to be considered **highly available** and **fault tolerant**
- it must have an ELB serving traffic to and ASG with a MIN of **2** instances located in separate availability zones.
