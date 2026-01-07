# Laravel Dockerized Application – OS Assignment 2

A fully dockerized Laravel web application built as part of the **Operating Systems – Practical Assignment 2**.  
This project demonstrates how modern web applications can be deployed using **Docker**, **Docker Compose**, and a **multi-container architecture**.

The application is containerized using PHP-FPM, Nginx, and a database service, following best practices for container-based development environments.

---

## 📌 Project Overview

This project focuses on applying core Operating Systems concepts such as:
- Process isolation
- Resource abstraction
- Service orchestration
- Inter-process communication  

All of these concepts are implemented practically using Docker containers.

---

## 🛠 Technologies Used

- **Laravel** (PHP Framework)
- **Docker**
- **Docker Compose**
- **PHP 8.3 (FPM)**
- **Nginx**
- **SQLite / MySQL (container-ready)**
- **Git & GitHub**
- **WSL2 (Linux environment on Windows)**

---

## 🧱 System Architecture

The application is built using a **multi-container architecture**:

| Service | Description |
|------|-----------|
| app | Laravel application running on PHP-FPM |
| web | Nginx web server |
| db | Database service (SQLite by default, MySQL ready) |

Each service runs in its own isolated container and communicates through a shared Docker network.

---

## 📂 Project Structure

os-assignment2-laravel-docker/
│
├── task-project/ # Laravel application
││ ├── app/
││ ├── public/
││ ├── database/
││ ├── Dockerfile
││ └── artisan
│
├── nginx/
││ └── default.conf # Nginx configuration
│
├── docs/
││ ├── screenshots/ # Required screenshots for submission
││ └── notes.md # Technical notes and reflections
│
├── docker-compose.yml
├── README.md
└── .dockerignore
---

## 🐳 Docker Implementation

### Dockerfile
The Dockerfile is responsible for:
- Installing PHP and required extensions
- Installing Composer
- Installing Laravel dependencies
- Preparing the application for execution

### docker-compose.yml
Docker Compose orchestrates all services:
- Builds the Laravel image
- Starts Nginx and database services
- Manages volumes and networking
- Exposes the application on port **8080**

---

## ▶️ How to Run the Project

### Prerequisites
- Docker Desktop
- Docker Compose
- Git

### Steps

```bash
git clone https://github.com/amir-alaqad-code/os-assignment2-laravel-docker.git
cd os-assignment2-laravel-docker
docker compose up -d --build
Generate application key:docker compose exec app php artisan key:generate


Run database migrations:
docker compose exec app php artisan migrate

Open the application:
http://localhost:8080

```
📸 Screenshots

All required screenshots are stored inside:

docs/screenshots/


They include:

Docker images list

Running containers

Application running in browser

GitHub repository and commits

These screenshots are also included in the submitted PDF file.


🎯 Assignment Requirements Checklist
| Requirement                       | Status      |
| --------------------------------- | ----------- |
| Dockerfile                        | ✅ Completed |
| docker-compose.yml                | ✅ Completed |
| Multi-container setup             | ✅ Completed |
| Application running inside Docker | ✅ Completed |
| Docker image built                | ✅ Completed |
| Containers running                | ✅ Completed |
| GitHub repository                 | ✅ Completed |
| Documentation                     | ✅ Completed |
⭐ Bonus Features Implemented

Multi-container architecture

Nginx + PHP-FPM production setup

Persistent storage using volumes

Clean Docker image build process

Full documentation and screenshots

📚 Learning Outcomes

Through this project, the following skills were developed:

Understanding container-based OS abstraction

Managing isolated execution environments

Networking between distributed services

Practical DevOps and deployment skills

Debugging real-world Docker issues

👤 Author

Name: Amir Alaqad
Course: Operating Systems
Assignment: Practical Assignment 2
Eng: Yousef M. Y. Al Sabbah

