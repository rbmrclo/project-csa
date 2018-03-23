# ECS Workflow

### Dockerfile

- A plain text file (script) that specifies all of the components that are included in the container.
- Basically, it's the instructions for what will be placed inside a given container.

### Container/Docker Image

- A container/Docker image is built from a Dockerfile
- The container/Docker image contains all the downloaded software, code,
  runtime, system tools, and libraries (as outlined in the Dockerfile).
  - i.e If the Dockerfile specifies PHP to be downloaded and installed, then the
    container/Docker Image will have PHP downloaded and installed.

### Container Registry

- A container registry is a repository where container/docker images are stored
  and accessed from when needed.
- A container registry can by:
  - Located on AWS via the ECR service (EC2 Container Registry)
  - A 3rd party repository like Docker Hub
  - Self-hosted registry

### Task Definition

- A JSON formatted text file that contains the "blueprint" for your
  application, including:
  - Which container/docker image to use.
  - The repository (container registry) the image is located in.
  - Which ports should be open on the container instance.
  - What data volumes should be used with the containers.

### ECS Agent

- An ECS agent runs on each EC2 instance in the ECS cluster.
- It communicates information about the instances to ECS, including:
  - Running tasks
  - Resource utilization
- The ECS agent is also responsible for starting/stopping tasks (when told to by ECS)

### ECS Task

- An ECS task is the actual representation of the Task Definition on an EC2
  instance inside of your container cluster.
- The ECS agent will start/stop these tasks based on instruction/schedule.
