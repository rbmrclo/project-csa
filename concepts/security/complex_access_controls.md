# Complex Access Control

- Through IAM policies, AWS gives us the ability to create extremely complex and
  granular permission policies for our users (all the way down to the resource level)
- IAM policies with resource level permissions:
  - ECS: Create permissions for instances such as reboot, start, stop, or
    terminate based all the way down to the instance ID.
  - EBS volumes: Attach, Delete, Detach.
  - EC2 actions that are not one of these above are not governed by
    resource-level at this time.
- This is not EC2 limited, it can also include services such as RDS, S3, etc.
- Additional security measures, such as MFA authentication are also available
  when action on certain resources:
  - For example, you can require MFA before an API request to delete an object
    within an S3 bucket.
