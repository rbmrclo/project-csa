# EC2 Container Service (ECS)

- ECS is a container management service that supports Docker.
- It allow you to easily create and manage a fleet of Docker containers on
  a cluster of EC2 instances.

### Why use ECS/Containers?

- Create distributed applications and Microservices
  - Create application architecture comprised of independent tasks or processes (microservices).
  - For example, you can have separate containers for various components of your application
    - Webserver
    - Application server
    - Message queue
    - Backend servers
  - This allows you to start, stop, manage, monitor, and scale each container independently.

- Batch and ETL Jobs
  - Package batch and ETL jobs into containers and deploy them into a shared EC2 cluster(s).
  - Run different versions of the same job or multiple jobs on the same cluster.
  - Share cluster capacity with other processes and/or grow job dynamically
    on-demand to improve resource utilization.

- Continuous integration and Deployment
  - By using Docker's Image versioning, you can use containers for continuous
    integration and deployment.
  - Build processes can pull, build, and create a Docker Image that can be
    deployed into your containers.
  - This allows you to avoid an application from working in a developer
    environment and not working in a production environment because the Docker
    daemon is the same across all environments.
