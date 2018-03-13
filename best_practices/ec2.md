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
