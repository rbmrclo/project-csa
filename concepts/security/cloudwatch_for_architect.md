# CloudWatch Security

- Request are signed with an HMAC-SHA1 signature, calculated from the request
  and the user's private key.
- CloudWatch control API is only accessible via SSL encrypted endpoints.
- CloudWatch access is given via IAM permission policies, essentially giving
  users permissions that are only needed (only give access to CloudWatch if they
  need access to CloudWatch).
- Use CloudWatch and CloudTrail to monitor changes inside the AWS environment.
  - We can ask CloudWatch to notify us (via SNS) if there has been changes to:
    - Changes to IAM security credentials
    - Assigning access policies to users.
    - Adding/deleting users.
  - It is important to know how we can use CloudWatch for security in our AWS environment.
