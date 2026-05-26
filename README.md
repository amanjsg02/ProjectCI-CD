# Flask CI/CD Pipeline using Docker & GitHub Actions

##  Project Overview

This project demonstrates a complete **DevOps CI/CD pipeline** for a Flask web application using **GitHub Actions and Docker**.  
It automates the process of testing, building, and deploying the application as a Docker container.

The pipeline ensures that every code change is validated and packaged in a reproducible environment.

---

##  DevOps Workflow

###  Continuous Integration (CI)

On every push to the `main` branch:

- GitHub Actions triggers the workflow
- Sets up Ubuntu environment
- Configures Python 3.11 using setup-python
- Installs dependencies from `requirements.txt`
- Runs automated tests using `pytest`
- Validates code before build stage

---

###  Continuous Delivery (CD)

After successful CI:

- Docker image is built using Dockerfile
- Flask application is containerized
- Image is tagged with Docker Hub username/repository
- Docker image is pushed to Docker Hub using GitHub Secrets

---

##  Tech Stack

- Python 3.11
- Flask
- Docker
- GitHub Actions
- pytest
- Docker Hub

---

##  Security Implementation

- GitHub Secrets used for secure credentials storage:
  - DOCKER_USERNAME
  - DOCKER_PASSWORD (Access Token)
- No sensitive data exposed in source code

---

##  Flask Application

A simple Flask web application exposing a single endpoint:
