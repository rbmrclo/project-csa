# EC2 Placement Groups

- A placement group is a cluster of instances within the same availability zone.
- Used for applications that require an extremely low latency network between them.
- AWS attempts to place all the instances as close as physically possible in the
  data center to reduce latency.
- Instances within a placement group have a low latency, 10 Gbps network
  connection between them.
- Instances that are in the placement group need to have enhanced networking in
  order to maximize placement groups.

#### Troubleshooting Placement Groups

- If an instance in a placement group is stopped, once it is started again it
  will continue to be a member of the placement group.
- It is suggested to launch all the required instances within a placement group
  in a single request, and that the same instance type is used for all the
  instances within the placement group.
- Is is possible, if more instances are added at a later time to the placement
  group OR if a placement group instance is stopped and started again, to
  receive an "insufficient capacity error".
  - Resolve the capacity error by stopping all instances in the member group and
    attempting to start them again.

#### Important facts

- Instances not originally launched/created in the placement group cannot be
  moved into the placement group.
- Placement groups cannot be merged together.
- A placement group cannot span multiple availability zones.
- Placement group names must be unique within your own AWS account.
- Plaement groups can be "connected".
- Instances must have 10 gigabit network speeds in order to take advantage of
  placement groups (proper instance type).

