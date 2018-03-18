# API Gateway

- API Gateway is a fully-managed service that allows you to create and manage
  your own APIs for your application.
- API Gateway acts as a "front door" for your application, allowing access to
  data/logic/functionality from your back-end services.

### Main Features

- Build RESTful APIs with:
  - Resources
  - Methods (i.e GET, POST, PUT)
  - Settings
- Deploy APIs to a "Stage" (different envs: i.e dev, beta, production)
  - Each stage can have it's own throttling, caching metering, and logging.
- Create a new API version by cloning an existing one.
  - You can create and work on multiple versions of an API (API version control).
- Roll back to previous API deployments.
  - A history of API deployments are kept.
- Custom domain names
  - Custom domain names can point to an API or stage
- Create and manage API keys for access AND meter usage of the API keys through Amazon CloudWatch Logs
- Set throttling rules based on the number of request per second (for each HTTP method)
  - Request over the limit throttled (HTTP 429 response)
- Security using Signature v.4 to sign and authorize API calls
  - Temporary credentials generated through Amazon Cognito and Security Token Service

### Benefits

- Ability to cache API responses
- DDoS protection via CloudFront
- SDK generation for iOS, Android, and JavaScript
- Supports Swagger (a very popular framework of API dev tools)
- Request/response data transformation (i.e JSON IN to XML OUT)

