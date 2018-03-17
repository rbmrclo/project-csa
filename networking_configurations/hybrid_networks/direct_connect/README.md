# AWS Direct Connect

- AWS Direct Connect is a service that provides a dedicated network connection
  between your network and one of the AWS Direct Connect locations.
- This is done through an authorized Direct Connect Provider (i.e Verizon or other ISPs)
- Does not require hosting any router/hardware at the Direct Connect Partner
  location, only requires a Direct Connect location and a participating backbone provider.
- An AWS Direct Connect location provides access to the AWS region it is associated with.
- It does not provide access to other AWS regions.

##### Benefits

- Reduce network costs:
  - Reduce bandwidth commitment to corporate ISP over public internet.
  - Data transferred over direct connect is billed at a lower rate by Amazon (data in/out).

- Increase network consistency:
  - Dedicated private connections reduce latency (over sending the traffic via public routing)

- Dedicated private network connection to on-premise:
  - Connect the direct connect connection to a VGW in your VPC for a dedicated
    private connection from on-premise to VPC.
  - Use multiple VIF (Virtual Intefaces) to connect to multiple VPCs.

### Cross-network Connection (Cross Connect)

The physical connection between your network and the direct connect authorized partner,
which then handles the routes and connections to the AWS networks.

### Private Virtual Interface

- A Private Virtual Interfaces allows you to interface with an AWS (VPC)
  - With automatic route discovery using BGP
  - Requires a public or private ASN number
- Can only commmunicate with internal IP addresses inside of EC2
- Cannot access public IP addresses, as Direct Connect is NOT an internet provider.
- For best practice, use two Direct Connect connections for active-active or active-failover availability.
- You can also use VPN as a backup to direct connect connections
- You can create multiple private virtual interfaces to multiple VPC's at the same time.

### Public Virtual Interface

- A Public Virtual Interface allows you use a Direct Connect connection to
  connect to public AWS endpoints:
  - Any AWS service (for example, DynamoDB and Amazon S3)
- Requires public CIDR block range
- And even though we are accessing public endpoints, the connection maintains
  consistent traffic consistency as it is sent over your dedicated network.
