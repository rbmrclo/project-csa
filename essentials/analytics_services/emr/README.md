# Elastic MapReduce

- Amazon EMR is a service which deploys out EC2 instances based off of the
  Hadoop big data framework.
- EMR is used to analyze and process vast amounts of data.
- EMR also supports other distributed frameworks, such as:
  - Apache Spark
  - HBase
  - Presto
  - Flink

### General Workflow

- Data stored in S3, DynamoDB, or Redshift is sent to EMR
- The data is **mapped** to a "cluster" of Hadoop **Master/Slave nodes** for processing.
- Computations (coded/created by the developer) are used to process the data.
- The processed data is then **reduced** to a single output set of return information.

### Important Facts

- You (the admin) has the ability to access the underlying operating system.
- You can add user data to EC2 instances launched into the cluster via bootstrapping.
- EMR takes advantage of **parallel processing** for faster processing of data.
- You can resize a running cluster at any time, and you can deploy multiple clusters.
