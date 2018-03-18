# ElastiCache

- ElastiCache is a fully managed, in-memory cache engine
- ElastiCache is used to improve database performance by caching results of
  queries that are made to a database.
- ElasticCache is great for large, high-performance or high-taxing queries - and
  can store them inside of a cache (Elastic Cache Cluster) that can be accessed
  later (instead of repeat request continually hitting the primary database).
- So it reduces load on the database, which increases performance.
- ElastiCache allows for managing web sessions, and also caching dynamic
  generated data.
- Available engines to power ElastiCache
  - Memcached (Mem-Cache-D)
  - Redis
- Generally, the application needs to built to work with either Redis or Memchaced.
- Popular options like MySQL have Memchaced plugins, which allow an application
  to easily work with ElastiCache (if using Memcached as the engine).
