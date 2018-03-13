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

## Instance Types

Instance types describes the "hardware" components that an EC2 instance will run on:

- Compute power (processor/vCPU)
- Memory (RAM)
- Storage options / optimization (hard drive)
- Network performance (bandwidth)

As an architect, it's important to use the proper instance type to handle your
application's workload.

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
