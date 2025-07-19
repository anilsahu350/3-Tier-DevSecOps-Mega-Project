# 🚀 3-Tier DevSecOps Mega Project

A complete DevSecOps pipeline for a Node.js-based 3-tier web app (React frontend, Express backend, MySQL DB), built with Docker, Jenkins, Trivy, GitLeaks, and SonarQube.

---

## 🧰 Tech Stack

- **Frontend**: React + Nginx
- **Backend**: Node.js (Express)
- **Database**: MySQL
- **CI/CD**: Jenkins + Docker Compose
- **Security**: GitLeaks, Trivy
- **Code Quality**: SonarQube

---

## 🔧 Prerequisites

Install on Jenkins host:

- Docker + Docker Compose
- Node.js (Jenkins tool name: `nodejs23`)
- SonarScanner (`sonar-scanner`)
- GitLeaks, Trivy
- SonarQube (Jenkins name: `sonar`)
- Docker Hub credentials in Jenkins as `docker-cred`

---

## 🛠️ Jenkins Pipeline Stages

1. **Checkout** from GitHub branch `docker-build-deploy`
2. **JS Compilation** checks (client + backend)
3. **Secret Scanning** via GitLeaks
4. **Code Quality** with SonarQube
5. **Trivy Security Scan** (FS & Docker Images)
6. **Docker Build + Push** to Docker Hub
7. **Deploy** with Docker Compose

---

## 🐳 Docker Compose

Run locally:

```bash
docker-compose up -d
