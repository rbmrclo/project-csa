# Elastic Cloud Compute (EC2)

## Configuration

- EC2 instances are designed to mimic traditional on-premise servers, but with
  the ability to be commissioned and decommissioned on-demand for easy
  scalability and elasticity.

- EC2 instances are primarily comprised of the follow components:
  - **Amazon Machine Image (AMI)**: The operating system (and other settings)
  - **Instance Type**: The hardware (compute power, RAM, network bandwidth, etc.)
  - **Network Interface** (public, private, or elastic IP addresses).
  - **Storage**: The instances "hard drive" (including two options).
    - Elastic Block Store (EBS) - which is "network persistent storage"
    - Instance Store - which is "ephemeral storage"

## Purchasing Options

#### `On-Demand`

On-demand purchasing allows you to choose any instance type you like and provision/terminate it at any time (on-demand).

- Is the **most expensive** purchasing option
- Is the **most flexible** purchasing option
- You are only charged when the instance is **running**:
  - **Per second pricing**: Amazon Linux and Ubuntu AMIs (60 seconds billing minimum)
  - **Hourly pricing**: Windows, RHEL, and any other AMIs where per second pricing is not indicated.
- You can provision/terminate an on-demand instance at any time.

#### `Reserved`

This purchasing option allows you to purchase an instance for a set time period of one (1) or three (3) years.

- This allows for a significant price discount over using on-demand.
- You can select to pay upfront, partial upfront, no upfront.
- Once you buy a reserved instance, you own it for the selected time period
  and are responsible for the entire price - regardless of how often you
  use it.

#### `Spot`

Spot pricing is a way for you to "bid" on an instance type, and only pay for and
use that instance when the spot price is equal to or below your "bid" price.

- This option allows Amazon to sell the use of **unused instances**, for short
  amounts of time, at a **substantial discount**.
- Spot prices fluctuate based on supply and demand in the spot marketplace.
- You are charged by the minute or hour (same AMI conditions as on-demand instances)
- When you have an active bid, an instance is provisioned for you when the spot
  price is equal to or less than your bid price.
- A provisioned instances automatically terminate when the spot price is greater
  than your bid price.
- Bid on unused EC2 instances for "non production applications".

## Instance Types

Instance types describes the "hardware" components that an EC2 instance will run on:

- Compute power (processor/vCPU)
- Memory (RAM)
- Storage options / optimization (hard drive)
- Network performance (bandwidth)

As an architect, it's important to use the proper instance type to handle your
application's workload.

## IP Addresses

#### `Private IP Address`

- All EC2 instances are automatically created with a PRIVATE IP address.
- The private IP address is used for internal (inside the VPC) communication
  between instances.

#### `Public IP Address`

- When creating an EC2 instance, you have the option to enable (or auto-assign)
  a public IP address.
- A public IP address is required if you want the EC2 instance to have direct
  communication with resources across the open internet.
  - For example, if you want to directly SSH into the instance or have it
    directly serve web traffic.
- Auto-assigning is based on the setting for the selected subnet that you are
  provisioning the instance in.

#### `Elastic IP Address (EIP)`

- An EIP is a static IPv4 address designed for dynamic cloud computing.
- An EIP is a public IPv4 address.
- With an EIP you can attach a public IP address to an EC2 instance that was
  created with only a private IP address or...
- You can mask the failure of an instance or software by rapidly remapping the
  address to another instance in your account. (i.e detaching the EIP from one
  instance and attaching it to another).
- Attaching an EIP to an instance will replace it's default public IP address
  for as long as it is attached.

## Virtualization

- Virtualization is the process of creating a "virtual" version of something
  rather than the actual version of that thing.
- In AWS EC2, virtualization refers to using a "portion" of a server's computing
  power and storage to setup and run an operating system.
- Virtualization for EC2 is run using the Xen Hypervisor Software.
- The maintenance of the physical AWS server and the Xen Hypervisor is handled by AWS.

### `Linux AMI Virtualization Types`

#### `HVM AMIs (Hardware Virtual Machine)`

- This virtualization type provides the ability to run an operating system
  directly on top of a virtual machine without any modification, as if it were
  run on the bare-metal hardware.
- The Amazon EC2 host system emulates some or all of the underlying hardware
  that is presented to the guest.
- Unlike PV guests, HVM guests can take advantage of hardware extensions that
  provide fast access to the underlying hardware on the host system.

#### `PV AMIs (Paravirtual)`

- Guests can run on host hardware that does not have explicit support for
  virtualization, but they cannot take advantage of special hardware extensions
  such as enhanced networking or GPU processing.
- Historically, PV guests had better performance than HVM guests in many cases,
  but because of enhancements in HVM virtualization and the availability of PV
  drivers for HVM AMIs, this is no longer true.

## Important Facts

- A security group must be assigned to an instance during the creation process.
- Each instance must be placed into an existing VPC, availability zone, and
  subnet.
- Automated (bootstrapping) custom launch commands can be passed into the
  instance during launch via "user-data" scripts.
- "Tags" can be used to help name and organize provisioned instances.
- Encrypted key pairs are used to manage login authentication.
- There are limits on the amount of instances you can have running in a region
  at any particular time.
