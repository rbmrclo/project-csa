# VPC

#### Limits

- 5 VPCs per region (available upon request)
- 5 Internet Gateways per region
- 50 Customer Gateways per region
- 50 VPN connections per region
- 200 Route Tables per region / 50 entries per route table
- 5 Elastic IP Addresses
- 500 Security Groups per VPC
- 50 Rules per Security Group
- 5 Security Groups per network interface (security groups although generally
  referred to as being on the instance level are technically on the VPC level)

## Internet Gateway

- Only 1 IGW can be attached to a VPC at a time.
- An IGW cannot be detached from a VPC while there are active AWS resources in
  the VPC (such as an EC2 instance or RDS database).
- An IGW must be attached to a VPC if the resources inside the VPC need to
  connect to resources via the open internet.

## Route Table

- Best practice is to leave the default route table and create a new route table
  when new routes are needed for specific subnets.
- The "default" VPC already has a "main" route table.

## Subnets

- A subnet must be associated with a route table.
- A **public** subnet has a route to the internet.
  - It is associated with a route table that has an IGW attached.
- A **private** subnet does not have a route to the internet.
  - It is associated with a route table that does not have an IGW attached.
- Instances launched into a private subnet can't communicate with the internet.
  - This creates a higher level of security, but it creates a limitation of an
    instance not being able to download software and/or updates.
  - This issue is solved by routing traffic through a NAT instance.
- By default, all subnets traffic is allowed to each other available subnet
  within via the **local** target in the route table.
- A subnet is located in one specific availability zone, and does not span AZs.

