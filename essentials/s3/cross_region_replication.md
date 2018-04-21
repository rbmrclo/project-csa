# S3 Cross Region Replication

- Versioning must be enabled on both the source and destination buckets
- Regions must be unique
- Files in an existing bucket are not replicated automatically. All subsequent
  updated files will be replicated automatically.
- You can sync the existing files from source bucket to destination bucket via
  CLI (i.e `aws s3 cp`)
- You cannot replicate to multiple buckets or use daisy chaining (at this time)
- Delete markers are replicated
- Deleting individual versions or delete markers will not be replicated.
