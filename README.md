# 🐳 Full-Stack Containerized Application Orchestration

[![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)
[![Docker Compose](https://img.shields.io/badge/Compose-2496ED?logo=docker&logoColor=white)](https://docs.docker.com/compose/)
![Status](https://img.shields.io/badge/Status-Complete-green)

## 📌 Project Overview
This project demonstrates the containerization and orchestration of a three-tier full-stack application. It showcases the ability to manage complex service dependencies, inter-container networking, and persistent storage using **Docker** and **Docker Compose**.

## 🏗️ System Architecture
The application is architected into three distinct microservices that operate within a private virtual bridge network:

1.  **Frontend (Nginx):** Serves the static assets and acts as a reverse proxy.
2.  **Backend (API):** Processes business logic and connects to the database.
3.  **Database (Persistence):** A managed database instance using Docker Volumes for data safety.

---

## 🛠️ Key Technical Features
*   **Multi-Stage Docker Builds:** Optimized Dockerfiles to ensure small, secure, and production-ready images.
*   **Service Orchestration:** Automated the lifecycle of the entire stack via `docker-compose`.
*   **Isolated Networking:** Implemented a dedicated bridge network to ensure services communicate securely using internal DNS.
*   **Volume Persistence:** Configured persistent storage to prevent data loss during container restarts or upgrades.
*   **Environment Segregation:** Used `.env` files to keep sensitive credentials out of the source code.

---

## 📂 Project Structure
```text
.
├── frontend/             # Web interface source & Dockerfile
├── backend/              # API logic & Dockerfile
├── database/             # DB configurations & init scripts
├── .env.example          # Template for sensitive credentials
└── docker-compose.yml    # Master orchestration file
