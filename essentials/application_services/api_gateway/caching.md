# API Gateway Caching

- API Gateway will cache API responses so that duplicate API request do not have
  to hit your back-end
  - This reduces load on your back-end
  - Speeds up calls to your back-end
- You can configure a cache key and Time to Live (TTL) of the API response.
- Caching can be setup on a per API or per stage basis.
