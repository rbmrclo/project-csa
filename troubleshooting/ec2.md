# EC2 Troubleshooting

##### Connectivity issues to an EC2 instance

- Correct ports on the security group are may not be open

##### Cannot attach an EBS volume to an EC2 instance

- EBS volumes must live in the same availability zone as the EC2 instance they
  are to be attached to.
- You can create a snapshot from the volume and launch the volume in the correct
  availability zone.

##### Cannot launch additional instance

- You have probably reached the EC2 limit and need to contact AWS to increase limit.

##### Unable to download package updates

- The EC2 instance may not have a public / Elastic IP address, and/or does not
  belong to a public subnet.

##### Applications seeming to slow down on T2 micro instances

- T2 micro instances utilize CPU credits (for "burstable" processing), so
  chances are your application is using too much processing power and needs
  a larger instance or different instance type.

##### AMI unavailable in other regions

- AMI's are only available in the regions that they are created.
- An AMI can be copied to another region but will receive a new AMI id.

##### "Capacity error" when attempting to launch an instance in a placement group

- Start and stop all the instances in the placement group (AWS tries to locate
  them as close as possible).
