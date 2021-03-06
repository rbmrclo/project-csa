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

| Family | Specialty | Use case |
| ------ | --------- | -------- |
| F1 | Field Programmable Gate Array | Hardware acceleration for your code |
| I2 | High Speed Storage | NoSQL DBs, Data Warehousing, etc |
| G2 | Graphics Intensive | Video Encoding | 3D Application Streaming |
| H1 | High Disk Throughput | MapReduce-based workloads, distributed file systems such as HDFS and MapR-FS |
| T2 | Lowest Cost, General Purpose | Web Servers, Small DBs |
| D2 | Dense Storage | Fileservers / Data warehousing / Hadoop |
| R4 | Memory Optimized | Memory Intensive Apps / DBs |
| M4 | General Purpose | Application Servers |
| C4 | Compute Optimized | CPU Intensive Apps / DBs |
| P2 | Graphics / General Purpose GPU | Machine Learning, Bitcoin Mining |
| X1 | Memory Optimized | SAP HANA / Apache Spark, etc |

## Shared Responsibility Model

The AWS shared responsibility model describes the responsibility of both parties
(AWS & you) for managing varying elements of AWS resources.

- The customer (you) is responsible for managing the software level security on instances, including:
  - Security groups
  - Firewalls (IP tables, Firewalld, etc)
  - EBS encryption provided by AWS (snapshots can also use EBS encryption)
  - Additional encryption methods include encrypting entire file system using an
    encrypted file system.
  - Applying an SSL Certificate to the ELB (Elastic Load Balancer)

- AWS is responsible for managing the hypervisor and physical layer of security
  for EC2:
  - DDOS protection
  - Port scanning protection (not allowed even in your own environment without
    permission from AWS)
  - Ingress network filtering

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
