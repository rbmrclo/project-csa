# S3 Event Notifications

An S3 events notifications allows you to setup automated communication between
S3 and other AWS services when a selected event occurs in an S3 bucket.

##### Common event notification triggers include:

- `RRSObjectLost` (used for automating the recreation of lost RRS objects)
- `ObjectCreated` (for all or the following specific APIs called)
  - PUT
  - POST
  - COPY
  - CompleteMultiPartUpload

##### Events notification can be sent to the following AWS services:

- SNS
- Lambda
- SQS Queue
