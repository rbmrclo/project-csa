# EMR Nodes

### Master node

- A node that manages the cluster by running software components which
  coordinate the distribution of data and tasks among other (slave) nodes for
  processing.

- The master node tracks the status of tasks and monitors the health of the
  cluster.

### Slave node

##### Core node

- A slave node has software components which run tasks AND stores data in the
  Hadoop Distributed File System (HDFS) on your cluster.
- The core nodes do the "heavy lifting" with the data.

##### Task node

- A slave node that has software components which only run tasks.
- Task nodes are optional.
