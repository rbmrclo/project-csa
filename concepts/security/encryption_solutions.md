# Encryption Solutions

##### S3 has built-in features that allow you to encrypt your data

- AES-256 bit encryption that encrypts data-at-REST in an S3 bucket.
- AWS will decrpyt the data and sent to you when you download it.

##### EBS encrypted volumes

- You can select to have all data encrypted that is stored on an EBS for volume.
- If a snapshot is taken, that snapshot is automatically encrypted.

##### RDS encryption

- Aurora, MySQL, Oracle, PostgreSQL, and MS SQL all support this feature.
- Encrypts the underlying storage space for the instance.
- Automated Backups are encrypted (as well as snapshots)
- Read Replicas are encrypted.
- RDS provides SSL endpoints to encrypt a connection to a DB instance.
