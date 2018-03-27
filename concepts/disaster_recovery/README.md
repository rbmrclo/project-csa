# Disaster Recovery

### Business disaster recovery key words

##### Recovery time objective (RTO)

Time it takes after a disruption to restore operations back to its regular
service level, as defined by the companies operational level agreement. (i.e if
the RTO is 4 hours, you have 4 hours to restore service back to an acceptable
level).

##### Recovery point objective (RPO)

Acceptable amount of data loss measured in time. (i.e if the system goes down at
10PM, and RPO is 2 hours, then you should recover all data as part of the
application as it was before 8PM).

Not only should you design for disaster recovery for your applications running
on AWS, you can also use AWS as a disaster recovery solution for your on-premise
applications or data. The AWS services used should be determined based off of
the business RTO and RPO operational agreement.

##### Pilot light

A minimal version of your production environment that is running on AWS. This
allows for replication from on-premise servers to AWS, and in the event of
a disaster the AWS environment spins up more capacity (elasticity/automatically)
and DNS is switched from on-premise to AWS. It is important to keep up to date
AMI and instance configurations if following pilot light protocol.

##### Warm Standby

Has a larger foot print than a pilot light setup, and would most likely be
running business critical applications in "standby". This type of configuration
could also be used as a test area for applications.

##### Multi-Site Solution

Essentially close to your "production" environment, which can either be in the
cloud or on-premise. Has an active-active configuration, which means instances
size and capacity are all running in full standby and can easily convert at the
flip of a switch. Methods like this could be used to "load balance" using
latency based routing or Route 53 failover in the event of the issue.

##### Services Examples:

- Elastic Load Balancer and Auto Scaling
- Amazon EC2 VM Import Connector
- AMI's with up to date configurations
- Replication from on-premise database servers to RDS
- Automated the increasing of resources in the event of a disaster
- Use AWS Import/Export to copy large amounts of data to speed up replication
  times (also used for offsite archiving).
- Route 53 DNS Failover/Latency Based Routing Solutions
- Storage Gateway (Gateway-cached volumes/Gateway-stored volums)
