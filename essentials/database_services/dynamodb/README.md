# DynamoDB

- DynamoDB is a fully-managed, NoSQL, database service provided by AWS.
- It is similar to MongoDB, but is a home-grown AWS solution.
- Is schemaless, and uses a key-value store.
- You specify the required throughput capacity, and DynamoDB does the rest
  (being fully-managed).

#### Fully managed means

- Service manages all provisioning (and scaling) of underlying hardware.
- Fully distributed, and scales automatically with demand and growth.
- Built as a fault tolerant highly available service.
  - On the back end, it fully synchronizes the data across all of the
    availability zones within the region you created the DynamoDB tables in.

- DynamoDB also easily integrates with other AWS services, such as Elastic MapReduce.
  - Can easily move data to a hadoop cluster in Elastic MapReduce.

- Popular use cases include:
  - IOT (storing metadata)
  - Gaming (storing session information, leaderboards)
  - Mobile (storing user profiles, personalization)
