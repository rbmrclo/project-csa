# RDS Read Replicas

- Read replicas are asynchronous copies of the primary database that are used
  for read only purposes (only allow "read connections").
- When you write new data to the primary database, AWS copies it for you to the
  read replica.
- You can create, and have multiple read replicas for a primary database.
- Read replicas can be created from other read replicas (so no performance hit
  on the primary database).
- MySQL, MariaDB, PostgreSQL, and Aurora currently support read replicas.
- You can monitor replication tag using CloudWatch.

#### Benefits

- Read replicas allow for all read traffic to be redirected from the primary
  database to the read replica. This will greatly improve performance on the
  primary database.
- Read replicas allow for elasticity in RDS - you can add more read replicas as
  demand increases.
- You can promote a read replica to a primary instance
- MySQL
  - Replicate for importing/exporting data to RDS
  - Can replicate across regions

#### When should you use Read Replicas?

- High volume, non-cached database read traffic (elasticity)
- Running business function such as data warehousing.
- Importing / Exporting data into RDS.
- Rebuilding indexes:
  - Ability to promote a read replica to a primary instance
