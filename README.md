# 🚀 CI/CD Pipeline for Node.js Application

![Node.js](https://img.shields.io/badge/Node.js-18-green)
![Docker](https://img.shields.io/badge/Docker-Containerized-blue)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-orange)
![Status](https://img.shields.io/badge/Build-Automated-brightgreen)

---

## 📌 Overview

This project demonstrates the implementation of a **CI/CD pipeline** using **GitHub Actions** to automate the build and deployment process of a Node.js web application.

The workflow automatically:

- ✅ Installs dependencies  
- ✅ Builds the application  
- ✅ Creates a Docker image  
- ✅ Pushes the Docker image to DockerHub  

This project showcases practical DevOps automation using industry-standard tools.

---

## 🛠️ Tech Stack

- **Node.js**
- **Express.js**
- **Docker**
- **DockerHub**
- **GitHub Actions**

---

## 📂 Project Structure

```bash
nodejs-demo-app/
│
├── app.js
├── package.json
├── Dockerfile
└── .github/
    └── workflows/
        └── main.yml
```

---

## ⚙️ CI/CD Workflow

### 🔄 Trigger
The workflow runs automatically on:

```yaml
push:
  branches:
    - main
```

### 🔁 Pipeline Steps

1. Checkout repository
2. Setup Node.js environment
3. Install dependencies
4. Run tests (placeholder)
5. Login to DockerHub (via GitHub Secrets)
6. Build Docker image
7. Push image to DockerHub

---

## 🐳 Docker Configuration

The application is containerized using Docker.

### Build Image
```bash
docker build -t <your-docker-username>/nodejs-demo-app .
```

### Run Container
```bash
docker run -p 3000:3000 <your-docker-username>/nodejs-demo-app
```

---

## 🔐 Secrets Management

Sensitive credentials are securely stored using:

**GitHub → Settings → Secrets → Actions**

Used in workflow as:

```yaml
${{ secrets.DOCKER_USERNAME }}
${{ secrets.DOCKER_PASSWORD }}
```

This ensures secure authentication without exposing credentials.

---

## 🚦 Run Locally (Optional)

### Install Dependencies
```bash
npm install
```

### Start Server
```bash
node app.js
```

Visit:
```
http://localhost:3000
```

---

## 📦 Deployment Flow

```
Code Push → GitHub Actions Triggered → Build → Docker Image Created → Push to DockerHub
```

---

## 📈 Key DevOps Concepts Demonstrated

- Continuous Integration (CI)
- Continuous Deployment (CD)
- Infrastructure as Code
- Containerization
- Secure Secrets Management
- Workflow Automation

---

## 🔮 Future Improvements

- Add automated testing (Jest)
- Implement multi-stage Docker builds
- Add version tagging for Docker images
- Deploy to cloud platforms (AWS/Azure/GCP)
- Add failure notifications

---

## 🎯 Learning Outcome

Through this project, I gained hands-on experience in:

- Designing CI/CD pipelines
- Writing GitHub Actions workflows
- Containerizing applications with Docker
- Automating deployment processes
- Securing credentials in CI/CD environments

---

