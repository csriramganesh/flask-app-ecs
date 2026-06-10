# Flask Application Dockerization Project

## Project Overview

This project demonstrates how to containerize a Python Flask application using Docker. The application was deployed and tested on an Ubuntu EC2 instance, showcasing both single-stage and multi-stage Docker builds along with Docker Compose.

## Technologies Used

* Python
* Flask
* Docker
* Docker Compose
* Ubuntu EC2

---

## Project Objectives

* Create a custom Dockerfile for a Flask application
* Build and run Docker containers
* Understand Docker image layers and caching
* Implement a multi-stage Docker build
* Compare image sizes between single-stage and multi-stage builds
* Manage containers using Docker Compose

---

## Project Structure

```text
flask-app-ecs/
├── app.py
├── run.py
├── requirements.txt
├── Dockerfile
├── Dockerfile-multi
├── docker-compose.yml
└── screenshots/
```

---

## Single Stage Dockerfile

Created a Dockerfile using the official Python Slim image.

Key steps:

* Used Python 3.14 Slim as the base image
* Set the working directory
* Installed application dependencies
* Copied application source code
* Exposed port 80
* Started the Flask application

---

## Multi-Stage Dockerfile

Created a multi-stage Docker build to separate dependency installation from the runtime environment.

Benefits:

* Cleaner image structure
* Better build organization
* Improved Dockerfile practices
* Foundation for production-grade containerization

---

## Docker Compose

Created a Docker Compose configuration to simplify container deployment and management.

Features:

* Single command deployment
* Container lifecycle management
* Consistent runtime configuration

---

## Screenshots

### 1. Dockerfile Created

![Dockerfile Created](screenshots/01_Dockerfile_created.png)

### 2. Docker Image Built

![Docker Image Built](screenshots/02_Docker_image_built.png)

### 3. Docker Image Verified

![Docker Image Verified](screenshots/03_Docker_image_verified.png)

### 4. Container Running

![Container Running](screenshots/04_container_running.png)

### 5. Application Running in Browser

![Application Running](screenshots/05_application_running_in_browser.png)

### 6. Multi-Stage Dockerfile Created

![Multi Stage Dockerfile](screenshots/06_dockerfile_multi_created.png)

### 7. Multi-Stage Image Built

![Multi Stage Image Built](screenshots/08_multistage_image_built.png.png)

### 8. Image Size Comparison

![Image Size Comparison](screenshots/09_image_size_comparison.png.png)

### 9. Multi-Stage Container Running

![Multi Stage Container Running](screenshots/10_multistage_container_running.png)

### 10. Docker Compose Configuration

![Docker Compose Created](screenshots/11_docker_compose_created.png)

### 11. Docker Compose Deployment

![Docker Compose Up](screenshots/12_docker_compose_up_and_docker_compose_ps.png)

---

## Commands Used

### Build Single Stage Image

```bash
docker build -t flask-app:v1 .
```

### Run Container

```bash
docker run -d --name flask-app -p 80:80 flask-app:v1
```

### Build Multi-Stage Image

```bash
docker build -f Dockerfile.multi -t flask-app:multi .
```

### Run Multi-Stage Container

```bash
docker run -d --name flask-app-multi -p 80:80 flask-app:multi
```

### Deploy Using Docker Compose

```bash
docker compose up -d
```

### Stop Docker Compose Services

```bash
docker compose down
```

---

## Learning Outcomes

Through this project, I learned:

* Docker image creation
* Container lifecycle management
* Dockerfile best practices
* Multi-stage Docker builds
* Image optimization concepts
* Docker Compose fundamentals
* Running containerized applications on Linux servers

---

## Author

Sriram Ganesh

GitHub: https://github.com/csriramganesh

