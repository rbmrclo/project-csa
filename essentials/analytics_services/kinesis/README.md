# Kinesis

- Kinesis is a real-time data processing service that continuously captures (and
  stores) large amounts of data that can power real-time streaming dashboards.
- Using the AWS provided SDKs, you can create real-time dashboards, integrate
  dynamic pricing strategies, and export data from Kinesis to other AWS services.
- Including:
  - EMR (Analytics)
  - S3 (Storage)
  - RedShift (Big Data)
  - Lambda (Event Driven Actions)

### Components

- Stream
- Producers (data creators)
- Consumers (data consumers)
- Shards (processing power)

### Benefits

##### Real-time processing

- Continuously collect and build applications that analyze the data as it's generated.

##### Parallel processing

- Multiple Kinesis applications can be processing the same incoming data
  streaming concurrently.

##### Durable

- Kinesis synchronously replicates the streaming data across thre data centeres
  within a single AWS region and preserves the data for up to 24 hours.

##### Scales

- Can stream from as little as a few megabytes to several terabytes per hour.

### When to use

##### Gaming

- Collect gaming data such as player actions and feed the data into the gaming
  platform, for example, a reactive environment based off of real-time actions
  of the player.

##### Real-time analytics

- Collect IOT (sensors) from many sensors and high amounts of frequency and
  process it using Kinesis to gain insights as data arrives in your environment.

##### Application alerts

- Build a Kinesis application that monitors incoming application logs in
  real-time and trigger events based off the data.

##### Log / Event Data collection

- Log data from any number of devices and use Kinesis application to
  continuously process the incoming data, power real-time dashboards and store
  the data in S3 when completed.

##### Mobile data capture

- Mobile applications can push data to Kinesis from countless number of devices
  which makes the data available as soon as it is produced.
