# Spring Boot Application

This is a Spring Boot application built with Java 17. The project includes a Dockerfile for containerization and deployment to a Kubernetes cluster using a `deployment.yaml` file. The application can be run in a Kubernetes cluster using Helm.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Building the Docker Image](#building-the-docker-image)
- [Deploying to Kubernetes](#deploying-to-kubernetes)
- [Running with Helm](#running-with-helm)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

- Java 17
- Maven
- Docker
- Kubernetes
- Helm

## Getting Started

Clone the repository:

```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
```

## Building the Docker Image

- Build the project using Maven and Docker: The Dockerfile is a multi-stage build that first uses a Maven image to build the project, and then an OpenJDK 17 image to run it.
- Build the Docker image: docker build -t yourusername/your-app:latest .

## Deploying to Kubernetes

kubectl apply -f deployment.yaml

## Running with Helm

helm install your-app ./your-app-chart

## Project Structure

```java
kube/
├── blueprints/
│   └── app-deployment.yaml
├── src/
│   ├── main/
│   │   ├── java/
│   │   └── resources/
│   └── test/
│       ├── java/
│       └── resources/
├── Dockerfile
├── pom.xml
└── README.md
```

## Contributing

We welcome contributions! Please see CONTRIBUTING.md for more details.
