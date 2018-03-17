# S3 Versioning

- S3 versioning is a feature to manage and store all old/new/deleted versions of an object.
- By default, versionins is disabled on all buckets/objects.
- Once versioning is enabled, you can only "suspend" version. It cannot be fully disabled.
- Suspending versioning only prevents new versions from being created.
  All objects with existing versions will maintain their older versions.
- Versioning can only be set on the bucket level and applies to ALL objects in the bucket.
- Lifecycle policies can be applied to specific versions of an object.
- Versioning and lifecycle policies can both be enabled on a bucket at the same time.
- Versioning can be used with lifecycle policies to create a great archiving and
  backup solution in S3.
