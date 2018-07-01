# S3 Storage Classes

A storage class represents the "classification" assigned to each object in S3.
Current Storage Class types include:

- Standard
- Reduced Redundancy Storage (RRS)
- Infrequent Access (S3 IA)
- Glacier

Each storage class has varying attributes that dictate things like:

- Storage cost
- Object availability
- Object durability
- Frequency of access (to the object)

| Storage Class | Durability | Availability |
| ------------- | ---------- | ------------ |
| Standard (S3) | 99.999999999% | 99.99% |
| Reduced Redundancy (RRS) | 99.99% | 99.99% |
| Infrequent Access (IA) | 99.999999999% | 99.90% |
| One-Zone Infrequent (OZ-IA) | 99.999999999% | 99.5% (Single AZ) |

#### Standard

- Designed for general, all-purpose storage
- Is the default storage option
- 99.999999999% object durability (eleven nines)
- 99.99% object availability
- Is the most expensive storage class

#### Reduced Redundancy Storage (RRS)

- Designed for non-critical, reproducible objects
- 99.99% object durability
- 99.99% object availability
- Is less expensive than the standard storage class

#### Infrequent Access (S3-IA)

- Designed for objects that you do not frequently access, but must be
  immediately available when accessed.
- 99.999999999% object durability
- 99.90% object availability
- Is less expensive than the standard/RRS storage classes

#### Glacier

- Designed for long-term archival storage (not to be used for backups)
- May take several hours for objects stored in Glacier to be retrieved
- 99.999999999% object durability
- Is the cheapest S3 storage class (very low cost)
