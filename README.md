# Node.js Dockerized Application

This repository contains a simple Node.js application Dockerized for easy deployment in containers.

## STAR Analysis

### Situation
You want to create a simple Node.js application, Dockerize it, and run it in a container.

### Task
1. Create a Node.js application using Visual Studio Code.
2. Write a Dockerfile to containerize the Node.js application.
3. Encounter a port conflict issue while trying to run the Docker container.

### Action

#### Application Creation
- Open Visual Studio Code and create a new Node.js application.
- Initialize a Node.js project using `npm init`.
- Write a simple "Hello, Docker World!" application in `app.js`.

#### Dockerization
- Create a Dockerfile specifying the Node.js base image, setting up the working directory, installing dependencies, and defining the command to run the application.
- Build the Docker image using `docker build`.
- Run the Docker container using `docker run`.

#### Port Conflict Issue
- Encounter a port conflict issue due to port 3000 being already in use.
- Use `lsof -i :3000` to identify the process using the port.
- Stop the conflicting process using `kill -9 <PID>`.
- If you're unable to free up port 3000, you can choose a different port when running the Docker container. Update the docker run command accordingly:docker run -p <host_port>:3000 node-docker-app
- Retry running the Docker container.

### Result
Successfully create a simple Node.js application, Dockerize it, and resolve the port conflict issue.

## SWOT Analysis

### Strengths
- Quick and straightforward setup using Visual Studio Code for Node.js development.
- Docker allows for easy containerization and portability of the application.
- Identification and resolution of the port conflict issue demonstrate troubleshooting skills.

### Weaknesses
- Potential dependency on external services or processes using the same port, leading to conflicts.
- Limited coverage of error handling and potential issues in the application.

### Opportunities
- Opportunities to extend the application by adding more features or integrating with other technologies.
- Learning opportunities to explore advanced Docker configurations and practices.

### Threats
- Possible conflicts with other applications or services using the same resources (ports, dependencies).
- Future changes in Node.js or Docker ecosystems that may require updates to the application or Docker configuration.

## Getting Started

Follow these steps to set up and run the Dockerized Node.js application.

...

## Cleanup

If you want to stop and remove the Docker container, use the following commands:

docker ps              # Identify the container ID or name
docker stop <container_id_or_name>
docker rm <container_id_or_name>

...

