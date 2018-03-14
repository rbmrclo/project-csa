# AWS Lambda

- Lambda is a "serverless" computing platform.
- Serverless means that you can run code without provisioning or managing servers.
  - So if you want to run code, you don't have to spin up an EC2 instance and
    install software, you can just create a "lambda function", drop your code in
    it, and execute it.
- Lambda scales the required compute power automatically with your code.
- You pay only for the compute time you consume (to the millisecond).
- By default, it is highly available, fault-tolerant, scalable, elastic, and cost efficient.
- Lambda integrates with many other AWS services.
- Current supported languages include:
  - Node.js
  - Java
  - C#
  - Python

#### When should you use Lambda over EC2?

- Generally you want to use Lambda when you want to run code that is in response
  to events, such as:
  - Changes to Amazon S3 buckets
  - Updates to an Amazon DynamoDB table
  - Custom events generated by your applications or devices