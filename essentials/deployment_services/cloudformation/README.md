# CloudFormation

CloudFormation is the pure definition of infrastructure as code.

- You can "convert" your application's architecture into a JSON formatted
  template (so your architecture is literally code).

- You can then use that JSON template to deploy out updated or replicated copies
  of that architecture to multiple regions.

### Benefits

- Saves time - you don't have to manually create duplicate architecture in additional regions.
- Since your infrastructure is now code, you can version control your infrastructure.
  Allowing for rollbacks to previous versions of your infrastructure if a new
  version has issues.
- Allows for backups of your infrastructure.
- Great solution for disaster recovery.
