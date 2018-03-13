# IP Addresses

### `Private IP Address`

- All EC2 instances are automatically created with a PRIVATE IP address.
- The private IP address is used for internal (inside the VPC) communication
  between instances.

### `Public IP Address`

- When creating an EC2 instance, you have the option to enable (or auto-assign)
  a public IP address.
- A public IP address is required if you want the EC2 instance to have direct
  communication with resources across the open internet.
  - For example, if you want to directly SSH into the instance or have it
    directly serve web traffic.
- Auto-assigning is based on the setting for the selected subnet that you are
  provisioning the instance in.

### `Elastic IP Address (EIP)`

- An EIP is a static IPv4 address designed for dynamic cloud computing.
- An EIP is a public IPv4 address.
- With an EIP you can attach a public IP address to an EC2 instance that was
  created with only a private IP address or...
- You can mask the failure of an instance or software by rapidly remapping the
  address to another instance in your account. (i.e detaching the EIP from one
  instance and attaching it to another).
- Attaching an EIP to an instance will replace it's default public IP address
  for as long as it is attached.

