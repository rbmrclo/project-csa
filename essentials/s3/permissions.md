# S3 Permissions

- All buckets and objects are private by default - only the resource owner has access.
- The resource owner can grant access to the resources (bucket/objects) through S3
  "resource based policies" OR access can be granted through a traditional IAM
  user policy.

#### Resource based policies (for S3) are:

##### Bucket Policies

- Are policies that are attached only to the S3 bucket (not an IAM user)
- The permissions in the policy are applied to all objects in the bucket
- The policy specifies what actions are allowed or denied for a particular user of that bucket - such as:
  - Granting access to an anonymous user
  - Who (a "principal") can execute certain actions like PUT or DELETE
  - Restricting access based off of IP address (generally used for CDN management)

##### S3 Access Control Lists

- Grant access to users in other AWS accounts or to the public
- Both buckets and objects has ACLs
- Object ACLs allow us to share an S3 object with the public via a URL link
