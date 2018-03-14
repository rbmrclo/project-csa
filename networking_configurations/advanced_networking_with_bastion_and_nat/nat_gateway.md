# NAT Gateway

- A **NAT Gateway** is designed to provide EC2 instances that live in a private
  subnet with a route to the internet (so they can download software packages
  and updates).
- A NAT Gateway will prevent any hosts located outside of the VPC from
  initiating a connection with instances that are associated with it.
- A NAT Gateway will only allow incoming traffic through if a request for it
  originated from an instance in a private subnet.
- A NAT Gateway is needed because instances launched into private subnets can't
  communicate with the open internet.
- Placing instances in a private subnet creates a higher level of security, but
  also creates the limitation of the instances not being able to download
  software and software updates.

#### A NAT Gateway MUST:

- Be created in a public subnet
- Be part of the private subnets route table

#### NAT Instance

- A NAT Instance is identical to a NAT gateway in its purpose.
- However, it is executed differently by configuring an actual EC2 instance to do the same job.
- A NAT Instance is starting to become more of a legacy feature in AWS.
- However, questions about them may still appear on the exam.
