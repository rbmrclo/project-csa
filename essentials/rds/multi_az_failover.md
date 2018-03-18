# RDS Multi-AZ Failover

- Multi AZ failover (Automatic AZ-Failover) synchronously replicates data to
  a backup (stand-by) database instance located in another availability zone
  (but in the same region).

- In the event of:
  - Service outage in an availability zone
  - Primary DB instance failure
  - Instance server type is changed
  - Manual failover initiated
  - Updating software version
  - AWS will automatically switch the CNAME DNS record from the primary instance
    to the stand-by instance.

- RDS backups are taken against the stand-by instance to reduce I/O freezes and
  slow down IF multi-az is enabled.

- In order for mutli-az to work, your primary database instance must be launched
  into a **"subnet group"**.
  - NOTE: An RDS instance must be launched into a subnet (inside a VPC), just
    like an EC2 instance. So the same security/connectivity rules, and highly
    available/fault tolerant concepts apply.
