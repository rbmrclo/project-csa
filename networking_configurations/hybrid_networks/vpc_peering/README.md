# VPC Peering

- VPC peering is used to extend your private network from one VPC, or one
  subnet, or specifically one instance, to another VPC.
- This is for sharing internal resources, via private IP addresses.
- VPC peering can occur between two VPCs that are in the same region, or two
  VPCs that are in different regions (called inter-region VPC peering).
- You can configure VPC peering between two VPCs in different accounts
  (inter-region VPC peering is also possible across accounts).
- To peer VPCs, they must have separate (non-overlapping) CIDR block ranges.
- Transitive connections are not allowed.
- You can configure the peering to connect the entire VPC, or just specific subnets.
