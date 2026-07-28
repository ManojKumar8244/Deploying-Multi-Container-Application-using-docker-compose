# Deploying Multi-Container Applications using Docker Compose

## 📌 Project Overview

This project demonstrates how to deploy and manage a **multi-container voting application** using **Docker Compose**. The application follows a microservices architecture consisting of three independent services: **Vote**, **Worker**, and **Result**. Each service is containerized using its own Dockerfile, while Docker Compose orchestrates the entire application stack by managing container creation, networking, dependencies, and lifecycle through a single `docker-compose.yml` file.

---

## 🎯 Objectives

- Containerize multiple application components using Docker.
- Deploy a complete multi-container application using Docker Compose.
- Manage application services from a single Compose configuration.
- Enable communication between application containers.
- Simplify application deployment and management.
- Understand Docker Compose networking and orchestration.

---

## 🏗️ Architecture

The application consists of the following services:

- **Vote Service** – Python-based frontend where users cast their votes.
- **Worker Service** – .NET Core background service that processes votes.
- **Result Service** – Node.js application that displays live voting results.
- **Docker Compose** – Orchestrates all services and their dependencies.
- **Docker Network** – Enables communication between containers.

---

## 🛠️ Technologies Used

- Docker
- Docker Compose
- Docker CLI
- Python
- Node.js
- .NET Core
- HTML
- CSS
- YAML
- Ubuntu / Linux

---

## 📂 Project Structure

```text
docker-compose-voting-app/
│
├── Screenshots/
│   ├── Screenshot of Docker compose service list.png
│   ├── Screenshot of application working through browser.png
│   └── Screenshot of running containers.png
│
├── result/
│   ├── tests/
│   ├── views/
│   ├── Dockerfile
│   ├── docker-compose.test.yml
│   ├── package.json
│   ├── package-lock.json
│   ├── server.js
│   ├── app.js
│   └── ...
│
├── vote/
│   ├── static/
│   ├── templates/
│   ├── Dockerfile
│   ├── app.py
│   ├── requirements.txt
│   └── ...
│
├── worker/
│   ├── Dockerfile
│   ├── Program.cs
│   └── Worker.csproj
│
├── Architecture.png
├── docker-compose.yml
└── README.md
```

---

## 🚀 Deployment Steps

### 1. Clone the Repository

```bash
git clone <repository-url>
cd docker-compose-voting-app
```

---

### 2. Build and Start the Application Stack

```bash
docker compose up -d --build
```

---

### 3. Verify Running Services

```bash
docker compose ps
```

---

### 4. Verify Running Containers

```bash
docker ps
```

---

### 5. View Application Logs

View logs for all services:

```bash
docker compose logs
```

View logs for individual services:

```bash
docker compose logs vote
docker compose logs worker
docker compose logs result
```

---

### 6. Verify Docker Images

```bash
docker images
```

---

### 7. Verify Docker Network

```bash
docker network ls
```

Inspect the application network:

```bash
docker network inspect <network-name>
```

---

### 8. Access the Application

Open the application in your browser using the configured ports.

Example:

```text
http://localhost:8080
```

or

```text
http://localhost:<configured-port>
```

---

### 9. Stop the Application

```bash
docker compose down
```

To remove associated volumes:

```bash
docker compose down -v
```

---

## 🔍 Verification Commands

```bash
docker compose ps

docker compose logs

docker ps

docker images

docker network ls

docker network inspect <network-name>

docker volume ls
```

---

## 📊 Key Features

- Multi-container application deployment
- Independent microservices architecture
- Docker Compose orchestration
- Automatic service networking
- Centralized configuration using `docker-compose.yml`
- Easy container lifecycle management
- Service dependency management
- Simplified deployment with a single command

---

## 📚 Learning Outcomes

Through this project, I gained hands-on experience with:

- Docker Compose
- Multi-container application deployment
- Docker networking
- Docker image creation
- Docker volumes
- Service orchestration
- Container lifecycle management
- Microservices architecture

---

## ✅ Project Outcome

Successfully deployed a multi-container voting application using Docker Compose. Each application component was containerized independently and orchestrated using a single `docker-compose.yml` file. Docker Compose simplified service deployment, networking, dependency management, and lifecycle operations, providing an efficient and scalable solution for running a microservices-based application.

---

## 👨‍💻 Author

**Manoj Kumar Nagamulla**

- GitHub: https://github.com/ManojKumar8244
