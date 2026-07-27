# Deploying Multi-Container Applications using Docker Compose

## Problem Statement Overview
Starting and managing multi-container application stacks individually creates complex startup procedures, difficult inter-service dependency management, and inconsistent development environments. Docker Compose solves these issues by allowing developers to define, configure, and run an entire multi-container application stack using a single YAML configuration file.

## Solution Approach
I deployed a multi-container voting application stack using Docker Compose:
1. **Service Containerization:** Prepared individual `Dockerfile` configurations for each microservice (`vote`, `result`, `worker`).
2. **Compose Architecture Definition:** Authored a unified `docker-compose.yml` defining service specifications, container names, port mappings, networks, and service dependencies.
3. **Stack Deployment:** Deployed and built the full application stack simultaneously using Docker Compose commands.
4. **Verification & Management:** Tested service-to-service communication, validated frontend interface access in the browser, and managed stack operations via `docker compose ps` and `docker compose logs`.

## Dependencies and Tools
* Ubuntu VM / Local Development Environment
* Docker Engine & Docker CLI
* Docker Compose
* Multi-container application source code (`vote`, `result`, `worker`)

## Execution Steps
1. **Build and Launch Application Stack:**
   ```bash
   docker compose up -d --build
