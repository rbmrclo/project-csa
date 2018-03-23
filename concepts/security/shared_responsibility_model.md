# Shared Security Responsibility Model

- AWS is responsible for portions of the cloud, and you as the customer have
  portions of the cloud that you are responsible for - thus creating shared
  security responsibility.

- Reduces the operational burden (on you) as AWS operates, manages, and controls
  the components from the host operating systm and virtualization layer, down to
  the physical security of the facilities in which the service operate.

- As the customer (you), using AWS means you assume the responsibility and
  management of the guest operating system (including updates and security
  patches), other associated applications software, as well as configuration of
  the AWS-provided security group firewall.

- You are also responsible for your own coded applications and custom
  applications built on top of the cloud.

### AWS is responsible for (EC2 example)

- Facilities
- Physical security of hardware
- Network infrastructure
- Virtualization infrastructure

### As a customer, you are responsible for (EC2 example)

- Amazon Machine Images (AMIs)
- Operating Systems
- Applications
- Data-in-transit
- Data-at-rest
- Data stores
- Credentials
- Policies and configuration
