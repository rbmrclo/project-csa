# S3 Objects

- Objects are static files that contain metadata information.
  - Set of name-key pairs
  - Contain information specified by the user, and AWS information such as storage type

- Each object must be assigned a storage type, which determines the object's
availability, durability, and cost.

- By default, all objects are private.

- Objects can:
  - Be as small as 0 bytes and as large as 5 TB
  - Have multiple versions (if versioning is enabled)
  - Be made publicly available via a URL
  - Automatically switch to a different storage class or deleted (via lifecycle policies)
  - Encrypted
  - Organize into "sub name" spaces called folders

#### Object Encryption

- SSE (Server Side Encryption)
  - S3 can encrypt the object before saving it on the partitions in the data
    centers and decrypt when it is downloaded.
  - AES-256

- Or you can use your own encryption keys
  - Considered client side encryption where you encrypt the data before upload

- SSL terminated endpoints for the API
