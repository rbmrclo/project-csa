# Kinesis Consumers

- Consumers consume the stream's data
- This is done concurrently (multiple consumers can consume the same data at the same time)
- Consumers include (but are not limited to)
  - Real-time dashboards
  - S3
  - RedShift (data warehouse)
  - EMR
- Any application (one you create) can consume the streams data.
- Kinesis keeps 24 hours of streaming data stored by default, but can be
  configured to store up to 7 days.
