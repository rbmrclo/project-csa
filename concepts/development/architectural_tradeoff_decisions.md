# Architectural Trade-off Decisions

### Storage Trade-off Options

##### S3 Standard Storage

- 99.99999999999% (eleven nines) durability and 99.99% availability, but is the
  most expensive.

##### S3 Reduced Redundancy Storage (RRS)

- Reduced redundancy durability is 99.99%, but the storage cost is cheaper.
- Should be used for easily reproducible data, and you should take advantage of
  lost object notification using S3 events.

##### Glacier

- Requires and extended timeframe to check-in and check-out data from archiving.
- Costs are significantly reduced compared to S3 storage options.

### Database Trade-off Options

##### Running databases on EC2 instances

- Have to manage the underlying operating system
- Have to build for high availability
- Have to apply your own backups
- Can use additional software to cluster MySQL
- Requires more time to manage than RDS

##### Managed RDS database provides

- Fully managed database updates and does not require managing of the underlying OS.
- Provides automatic point in time backups.
- Easily enable Multi-AZ failover, and when a failover occurs, the DNS is
  switched from the primary instance to the standby instance.
- If Multi-AZ is enabled then backups are taken against the stand-by to reduce
  I/O freezes and updates are applied to the standby then is switched to the
  primary.
- Easily create read replicas.
