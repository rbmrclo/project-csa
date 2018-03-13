# Storage Options

## Elastic Block Store (EBS)

- EBS volumes are persistent, meaning that they can live beyond the life of the
  EC2 instance they are attached to.
- EBS backed volumes are network attached storage, meaning they can be
  attached/detached to or from various EC2 instances.
- However, they can only be attached to ONE EC2 instance at a time.
- EBS volumes have the benefit of being backed up into a snapshot - which can
  later be restored into a new EBS volume.

#### EBS Performance

- EBS volumes measure input/output operations in IOPS:
  - IOPS are input/output operations per second
  - AWS measures IOPS in 256KB chunks (or smaller)
  - Operations that are greater than 256KB are separated into individual 256KB
    chunks.
  - For example, a 512KB operation would count as 2 IOPS
- The type of EBS volume you specify greatly influences the I/O performance
  (IOPS) your device will receive.
- It is important as architects to understand if your application requires more
  (or less) I/O when selecting an EBS volume.
- Even volumes with "provisioned IOPS" may not produce the performance you
  expect. If this is the case, an EBS optimized instance type is required, which
  prioritizes EBS traffic.

#### Initializing EBS Volumes

- New EBS volumes no longer need to be "pre-warmed"
- New volumes will receive their maximum performance at the moment they are created.
- Volumes created from an EBS snapshot must be initialized.
- Initializing occurs the first time a storage block on the volume is read - and
  the performance impact can be impacted by up to 50%.
- You can avoid this impact in production environment by manually reading all
  the blocks.
