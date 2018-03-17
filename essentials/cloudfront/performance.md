# CloudFront Performance Considerations

CloudFront performance can be affected by different factors.

- File size and type of file
- Having to remake the request from the Edge location to the origin
  - Downloading the object from the origin takes time
  - As well as writing it to cache and responding to the end user request
  - The more requests that have to go to the origin, the higher the load is on
    your source. Which can also cause latency and load performance issues.
- The end location that the user's request goes to is dependent upon a "DNS
  check" to determine the closes EDGE location. So slow DNS issues can cause
  performance issues.
- Query strings (request to the origin to serve a specific object) reduce cache "hits":
  - For example: `http://cdn.example.com/?querythis=that`
  - It reduces performance because query strings are often unique so it reduces
    the cache hits and also requires extra work in order to forward to the
    origin location.
- CloudFront Performance can be increased by:
  - Longer cache periods increases performance (less frequent request to the source)
