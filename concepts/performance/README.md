# Performance

- The performance efficiency pillar focuses on how to use computing resources
  efficiently to meet your requirements and how to maintain that efficiency as
  demand changes and technology evolves.

#### Design Principles

- Democratize advanced technologies
- Go global in minutes
- Use server-less architectures
- Experiment more often

#### 4 Areas of Performance

- Compute
- Storage
- Database
- Space-time trade-off

#### Best Practices - Compute

- When architecting your system it is important to choose the right kind of
  server. Some applications require heavy CPU utilization, some require heavy
  memory utilization etc.

- With AWS servers are virtualized and at the click of a button (or API call)
  you can change the type of server in which your environment is running on. You
  can even switch to running with no servers at all and use AWS Lambda.

##### Questions

- How do you select the appropriate instance type of your system?
- How do you ensure that you continue to have the most appropriate instance type
  as new instance types and features are introduced?
- How do you monitor your instances post launch to ensure they are performing as
  expected?
- How do you ensure that the quantity of your instances matches demand?

#### Best Practices - Storage

- The optimal storage solutions for your environment depends on numbers of
  factors. For example:
  - Access method - Block, File, or Object
  - Patterns of Access - Random or Sequential
  - Throughput Required
  - Frequency of Access - Online, Offline or Archival
  - Frequency of Update - Worm, Dynamic
  - Availability Constraints
  - Durability Constraints

##### Questions

- How do you select the appropriate storage solution for your system?
- How do you ensure that you continue to have the most appropriate storage
  solution as new storage solutions and features are launched?
- How do you monitor your storage solution to ensure it is performing as
  expected?

#### Best Practices - Database

The optimal database solution depends on a number of factors. Do you need
database consistency, do you need high availability, do you need No SQL, do you
need DR etc?

With AWS, you get a LOT of options. RDS, DynamoDB, Redshift, etc.

##### Questions

- How do you select the appropriate database solution for your system?
- How do you ensure that you continue to have the most appropriate database
  solution and features as new database solution and features are launched?
- How do you monitor your databases to ensure performance is as expected?
- How do you ensure the capacity and throughput of your databases matches
  demand?

#### Best Practices - Space-Time trade-off

Using AWS, you can use services such as RDS to add read replicas, reducing the
load on your database and creating multiple copies of the database. This helps
to lower latency. You can use Direct Connect to provide predictable latency
between your HQ and AWS.

You can use the global infrastructure to have multiple copies of your
environment, in regions that is closest to your customer base. You can also use
caching services such as ElastiCache or CloudFront to reduce latency.

##### Questions

- How do you select the appropriate proximity and caching solutions for your
  system?
- How do you ensure that you continue to have the most appropriate proximity and
  caching solutions as new solutions are launched?
- How do you monitor your proximity and caching solutions to ensure performance
  is as expected?
- How do you ensure that the proximity and caching solutions you have matches
  demand?

#### Key AWS Services

- Compute: Autoscaling
- Storage: EBS, S3, Glacier
- Database: RDS, DynamoDB, Redshift
- Space-Time Trade-Off: CloudFront, ElastiCache, Direct Connect, RDS Read Replicas, etc
