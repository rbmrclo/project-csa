# Bastion Host

- A **Bastion Host** is an EC2 instance that lives in a public subnet, and is
  used as a "gateway" for traffic that is destined for instances that live in
  private subnets.
- This means that we can use a bastion host as a "portal" to access EC2
  instances that are located in a private subnet.
- A bastion host is considered the **critical strong point** of the network - as
  all traffic must pass through it first.
- A bastion host should have increased and extremely tight security (usually
  with extra 3rd party security and monitoring software installed)
- A bastion host can be used as an access point to "ssh" into an internal
  network (to access private resources) without a VPN (virtual private network).

> "A system identified by the firewall administrator as a crucial strong point in
> the network's security. Generally, bastion hosts will have some degree of
> extra attention paid to their security, may undergo regular audits, and may
> have modified software." - Marcus J. Ranum
