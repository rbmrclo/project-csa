# AWS Direct Connect

- AWS Direct Connect is a service that provides a dedicated network connection
  between your network and one of the AWS Direct Connect locations.
- This is done through an authorized Direct Connect Provider (i.e Verizon or other ISPs)
- Does not require hosting any router/hardware at the Direct Connect Partner
  location, only requires a Direct Connect location and a participating backbone provider.
- An AWS Direct Connect location provides access to the AWS region it is associated with.
- It does not provide access to other AWS regions.

### Benefits

- Reduce network costs:
  - Reduce bandwidth commitment to corporate ISP over public internet.
  - Data transferred over direct connect is billed at a lower rate by Amazon (data in/out).

- Increase network consistency:
  - Dedicated private connections reduce latency (over sending the traffic via public routing)

- Dedicated private network connection to on-premise:
  - Connect the direct connect connection to a VGW in your VPC for a dedicated
    private connection from on-premise to VPC.
  - Use multiple VIF (Virtual Intefaces) to connect to multiple VPCs.

