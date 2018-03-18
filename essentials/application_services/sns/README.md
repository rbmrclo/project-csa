# Simple Notification Service (SNS)

- SNS coordinates and manages the sending and delivery of messages to specific endpoints.
- We are able to use SNS to receive notifications when events occur in our AWS Environment.
- SNS is integrated into many AWS services, so it is very easy to setup
  notifications based on events that occur in those services.
- With CloudWatch and SNS, a full-environment monitoring solution can be created
  that notifies administrators of alerts, capacity issues, downtime, changes in
  the environment, and more.
- This service can also be used for publishing IOS/Android app notifications,
  and creating automation based off of notifications.

### SNS Components

##### Topic

- The group of subscriptions that you send a message to.

##### Subscription

- An endpoint that a message is sent.
- Available endpoints include:
  - HTTP
  - HTTPS
  - Email
  - Email-JSON
  - SQS
  - Application, Mobile APP notifications (IOS/Android/Amazon/Microsoft)
  - Lambda
  - SMS (cellular text message)
- Publisher
  - The entity that triggers the sending of a message
  - Examples include:
    - Human
    - S3 Event
    - Cloudwatch Alarm
