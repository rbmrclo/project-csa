# EMR Phases

### Map Phase

- Mapping is a function that defines the processes which splits the large data
  file for processing.
- During the mapping phase, the data is split into 128MB "chunks".
- The larger the instance size used in our EMR cluster, the more chunks you can
  map and process at the same time.
- If there are more chunks than nodes/mappers, the chunks will queue for
  processing.

### Reduce Phase

- Reducing is a function that aggregates the split data back into one data source.
- Reduced data needs to be stored (in a service like S3) as data processed by
  the EMR cluster is not persistent.
