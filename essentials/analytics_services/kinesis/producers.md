# Kinesis Producers

- Producers are devices that collect data for Kinesis processing.
- You build producers to continuously input data into a Kinesis stream.
- Producers can include (but not limited to):
  - IoT Sensors
  - Mobile devices (cell phones)
- You can have literally thousands of different producers and scale based on need.
  - The more data you want to process, the more "shards" you add to your Kinesis stream.
  - Each "shard" can process 2MB of read data per second, and 1MB of write data per second.
