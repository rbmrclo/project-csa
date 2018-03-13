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

## Network Access Control List

- ACLs operate at the network/subnet level
- They support ALLOW and DENY rules for traffic traveling into or out of
  a subnet.
- They are **stateless**, so return traffic must be allowed through an outbound
  rule.
- They process rules in number order when deciding wether to allow traffic.
- Rules are evaluated in order, starting with the lowest rule number - for
  example:
    - If traffic is denied at a lower rule number and allowed at a higher number
      rule, the allow rule will be ignored and the traffic will be denied.
- A network access control list (NACL) is an optional layer of security to your
  VPC that acts as a firewall for controlling traffic in and out of one or more
  subnets.
- Best practice is to increment numbers by 10 so if you have to place in a rule
  in a certain order it does not create an issue.

## Security Groups

- SGs are very similar to NACLs in that they allow/deny traffic
- However, security groups are security for the instance level (as opposed to
  the subnet level with ACLs)
- In addition, the way allow/deny rules work are different with ACLs:
  - SGs support only allow rules
  - They are **stateful**, so return traffic requests are allowed regardless of
    rules.
  - All rules are evaluated before deciding to allow traffic.
- Best practice is to allow ONLY traffic that is required.
