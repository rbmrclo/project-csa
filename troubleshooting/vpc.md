# VPC Troubleshooting

##### New EC2 instances are not automatically being assigned a public IP address

- Modify the Auto Assign Public IP setting on the subnet.

##### NAT Gateway is configured but instances inside a private subnet still cannot download packages

- Need to add `0.0.0.0/0` route to the NAT gateway on the route table for private subnets.

##### Traffic is not making it to the instances even though security group rules are correct

- Check the NACL to ensure the proper ports from the proper sources are open. (also check your IGW and route table settings)

##### Error when attempting to attach multipler internet gateways to a VPC

- Only one internet gateway can be attached to a VPC at any given time.

##### VPC Security group (for EC2 instances) does not have enough rules for the required application

- Assign the EC2 instance to multiple security groups.

##### Cannot SSH / communicate with resources inside of a private subnet

- Either you have not setup a VPN, or you have not connected to an EC2 instance (bastion host) within the VPC to launch a connection from.

##### Successful site-to-site VPN connection but unable to access extended resources

- Need to add on-premise routes to the Virtual Private Gateway route table.

##### Failure to create a VPC peering connection between two VPC's in differnet regions

- Peering connections can only be created between two VPC's in the same region.
