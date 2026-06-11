# Dockerized Application with CI/CD Pipeline

## Project Overview

This project demonstrates a complete CI/CD (Continuous Integration and Continuous Deployment) pipeline for a Dockerized web application using GitHub Actions, Docker Hub, and AWS EC2.

The goal was to automate the deployment process so that every code change pushed to GitHub is automatically built, published, and deployed to a live AWS server without any manual intervention.

---

## Architecture

The deployment architecture consists of:

Developer → GitHub Repository → GitHub Actions → Docker Hub → AWS EC2 → Docker Container → NGINX → Live Website

A detailed architecture diagram is maintained separately within the repository.

---

## Technology Stack

* Docker
* Dockerfile
* Docker Compose
* GitHub Actions
* GitHub Secrets
* Docker Hub
* AWS EC2 (Ubuntu)
* NGINX
* Linux

---

## Project Structure

```text
project-2-docker-cicd/
│
├── app/
│   └── index.html
│
├── Dockerfile
├── docker-compose.yml
│
├── .github/
│   └── workflows/
│       └── deploy.yml
│
├── architecture-diagram-project2.png
└── README.md
```

---

## CI/CD Workflow

1. Developer pushes code to GitHub.
2. GitHub Actions workflow is triggered automatically.
3. Docker image is built using the Dockerfile.
4. The image is pushed to Docker Hub.
5. GitHub Actions connects to AWS EC2 using SSH.
6. The latest Docker image is pulled from Docker Hub.
7. Existing container is stopped and removed.
8. A new container is deployed automatically.
9. Changes become available on the live application.

---

## Security Implementation

Sensitive credentials are securely stored using GitHub Secrets.

### Secrets Used

* DOCKER_USERNAME
* DOCKER_PASSWORD
* EC2_HOST
* EC2_USER
* EC2_SSH_KEY

No credentials are exposed in the source code repository.

---

## Features

* Dockerized Web Application
* Automated CI/CD Pipeline
* GitHub Actions Integration
* Docker Hub Registry Integration
* AWS EC2 Deployment
* Automated Container Updates
* Secure Secret Management
* Zero Manual Deployment

---

## Deployment Validation

The CI/CD pipeline was successfully verified by modifying the application source code and pushing changes to GitHub.

The workflow automatically:

* Rebuilt the Docker image
* Pushed the updated image to Docker Hub
* Pulled the latest image on EC2
* Replaced the running container
* Updated the live website automatically

---

## Key Learnings

* Docker Image Creation and Management
* Containerized Application Deployment
* GitHub Actions Workflow Development
* CI/CD Pipeline Automation
* Secure Credential Management
* AWS EC2 Administration
* Linux Server Management
* NGINX Configuration

---

## Future Enhancements

* HTTPS with SSL Certificates
* Custom Domain Integration
* Infrastructure as Code using Terraform
* Monitoring with Prometheus and Grafana
* Kubernetes Deployment
* Multi-Container Architecture

---

