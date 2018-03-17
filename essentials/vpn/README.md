# Virtual Private Network (VPN)

- A virtual private network enables the ability to extend a subnet from one
  geographic location to another geographic location on two separate networks.
- Extending the subnets allows the network at location "A" to communicate
  internally with all resources at location "B".
- This is essentially "extending" the on-premise network to the cloud, or the
  cloud to the on-premise network.
- For AWS, this allows us to communicate with all resources (like an EC2
  instance) internally without the need for public IP addresses and an internet gateway.
- It also provides an additional level of security by ensuring that traffic sent
  using the VPN is encrypted.
- The VPN connection has two parallel routes (IPsec tunnels), which is for redundancy.
- Only one Virtual Private Gateway can be attached to a VPC (just like only one
  IGW can be attached to a VPC).
- A VPC can have both a VPG and an IGW attached at the same time.
- Both VPG and a Customer Gateway are required to establish a VPN connection.

### Virtual Private Gateway

- A **Virtual Private Gateway** acts as the "connector" on the VPC (AWS) side of the VPN connection.
- The VPG is connected to the VPC.

### Customer Gateway

- A **customer gateway** is a physical device or software application at the
  on-premise location that acts as the "connector" to the VPN connection.
- In your AWS account, the customer gateway component is where you configure the
  public IP (internet routable static IP) address of the physical device or
  software application at the on-premise location.

### VPN Connection

- The VPN connection is the actual link between the virtual private gateway and the customer gateway.
- This connection is setup and managed in AWS.
- Each connection uses two IPsec tunnels for redundancy.
