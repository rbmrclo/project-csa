# EBS Snapshots

Snapshots are point-in-time backups of EBS volumes that are stored in S3.

#### Snapshot properties

- Snapshots are incremental in nature
- A snapshot only stores the changes since the most recent snapshot, thus
  reducing costs (by only having to pay for storage for the "incremental
  changes" between snapshots).
- However, if the "original" snapshot is deleted, all data is still available in
  all the other snapshots.
- Even though snapshot storage only charges you for the amount of incremental
  data in each snapshot all prior data is still there.
- Snapshots can be used to create fully restored EBS volumes.

#### Important notes

- Frequent snapshots of your data increases data durability - so highly recommended
- When a snapshot is being taken against the EBS volume, it can degrade
  performance so snapshots should occur during non-producton or non-peak load
  hours.
