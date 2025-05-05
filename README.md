# holbertonschool-softy-pinko-docker

## Project Overview

This project demonstrates the use of Docker to containerize and deploy a full-stack application. The application consists of a front-end static content server, a back-end API server, and a reverse proxy server. The infrastructure is designed to be scalable and efficient, utilizing Docker Compose for orchestration and Nginx for load balancing.

## Curriculum Context

- **Curriculum**: [C#25] Foundations v2 - Part 3
- **Project Badge**: Docker (Novice)
- **Author**: Derek Webb
- **Weight**: 1
- **Manual QA Review**: Required

## Description

Docker is a platform that allows applications to be packaged into portable, self-contained environments called containers. Containers include all necessary dependencies, libraries, and configurations, ensuring consistent behavior across different environments. This project focuses on creating a Dockerized infrastructure with the following components:

1. **Reverse Proxy**: Routes traffic to the appropriate service (front-end or back-end).
2. **Load Balancer**: Distributes API requests across multiple back-end servers using the Round Robin algorithm.
3. **Front-End Server**: Serves static content using Nginx.
4. **Back-End API Server**: Provides dynamic data using Flask.

## High-Level Design

The architecture includes:
- A reverse proxy server that acts as the entry point.
- A load balancer to distribute traffic between two API servers.
- A front-end server for static content.

### Round Robin Load Balancing
Round Robin is a simple algorithm that distributes requests evenly across servers. For example, with servers A, B, and C:
- Request 1 → Server A
- Request 2 → Server B
- Request 3 → Server C
- Request 4 → Server A (cycle repeats)

## Prerequisites

- Install Docker Desktop: [Docker Installation Guide](https://www.docker.com/)
- Familiarize yourself with Docker concepts: [Docker Tutorial](https://docs.docker.com/get-started/)

## Tasks Overview

### Task 0: Create Your First Docker Image
- Create a Dockerfile based on Ubuntu.
- Update and upgrade APT packages.
- Print "Hello, World!" when the container runs.

### Task 1: Back-End API Server
- Install Python3, pip3, and Flask in the Dockerfile.
- Create a Flask app with a single endpoint (`/api/hello`) that returns "Hello, World!".

### Task 2: Front-End Static Server
- Use Nginx to serve static files.
- Clone the front-end repository and configure Nginx to serve it on port 9000.

### Task 3: Connect Front-End and Back-End
- Use Flask-CORS to enable cross-origin requests.
- Update the front-end to fetch data dynamically from the back-end API.

### Task 4: Simplify with Docker Compose
- Create a `docker-compose.yml` file to manage all services (front-end, back-end).
- Use `docker-compose up` to spin up the entire application.

### Task 5: Add a Proxy Server
- Add an Nginx proxy server to route traffic to the front-end and back-end.
- Update the front-end to make API calls through the proxy.

### Task 6: Scale Horizontally
- Use Docker Compose to scale the back-end API servers.
- Configure Nginx to load balance requests across multiple API servers.

## Useful Resources

- [Docker Cheatsheet](https://dockerlabs.collabnix.com/docker/cheatsheet/)
- [Proxy vs Reverse Proxy](https://www.nginx.com/resources/glossary/reverse-proxy-vs-proxy-server/)
- [Flask Documentation](https://flask.palletsprojects.com/)

## Repository Structure

```
holbertonschool-softy-pinko-docker/
├── task0/
├── task1/
├── task2/
├── task3/
├── task4/
├── task5/
└── task6/
```

## Author

Derek Webb
