# Storage Transit Services

### Single Operation Upload

- A single operation upload is "traditional" upload where you upload the file in one part.
- A single operation upload can upload a file up to 5GB in size, however any file over 100MB should use multipart upload.

### Multipart Upload

- Multipart upload allows you to upload a single object as a set of parts
- Allows for uploading parts of a file concurrently
- Allows for stopping/resuming file uploads
- If transmission of any part fails, you can retransmit that part without
  affecting other parts.
- After all parts of your object are uploaded, Amazon S3 assembles these parts
  and creates the object.
- Required for objects 5GB and large, and highly suggested for use when objects
  are 100MB and larger.
- Can be used to upload a file up to 5TB in size.

### AWS Import/Export

- AWS Import/Export gives the ability to take on-premise data and physically
  snail mail it to AWS (using a device that you own).-
- AWS will import the data to either S3, EBS, or Glacier within one business day
  of the physical device arriving at AWS.

##### Benefits

- Off-site backup policy
- Quickly migrate LARGE amounts of data to the cloud (up to 16TB per job)
- Disaster recovery (AWS will een take S3 data and ship it back to you)

### Snowball

- Snowball is a petabyte-scale data transport solution
- Snowball uses an AWS provided secure transfer appliance
- Quickly move large amounts of data into and out of the AWS cloud

### Storage Gateway

- Connects local data center software appliances to cloud based storage such as Amazon S3.
- It does this through the Storage Gateway virtual appliance, which connects
  directly to your local infrastructure as a file server, a local disk volume,
  or as a virtual tape library (VTL).
- It can maintain frequently accessed data on-premises (providing low-latency
  performance) while storing all other data in:
  - S3
  - EBS
  - Glacier
- Storage Gateway also integrates your data with:
  - AWS encryption
  - Identity Management
  - Monitoring

##### Gateway-Cached Volumes

- Create storage volumes and mount them as iSCSI devices on the on-premise servers
- The gateway will store the data written to this volume in Amazon S3 and will
  cache frequently access data on-premise in the storage device.

##### Gateway-Stored Volumes

- Store all the data locally (on-premise) in storage volumes
- Gateway will periodically take snapshots of the data as incremental backups
  and stores them on Amazon S3.
