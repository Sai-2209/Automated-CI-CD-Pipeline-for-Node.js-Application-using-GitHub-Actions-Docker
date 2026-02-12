🚀 Automated CI/CD Pipeline for Node.js Application using GitHub Actions & Docker
📌 Project Overview

This project demonstrates the implementation of a CI/CD (Continuous Integration and Continuous Deployment) pipeline for a Node.js web application using GitHub Actions and Docker.

The pipeline automatically:

Installs dependencies

Builds the application

Creates a Docker image

Pushes the Docker image to DockerHub

This automation ensures faster, reliable, and consistent deployments with minimal manual intervention.

🎯 Objective

The primary objective of this task is to:

Understand CI/CD fundamentals

Implement GitHub Actions workflows

Containerize an application using Docker

Automate Docker image build and push process

Secure credentials using GitHub Secrets

🛠️ Technologies Used

Node.js

Express.js

Docker

DockerHub

GitHub

GitHub Actions (CI/CD)

🏗️ Project Architecture
Developer Pushes Code
        ↓
GitHub Repository
        ↓
GitHub Actions Workflow Triggered
        ↓
Install Dependencies
        ↓
Build Docker Image
        ↓
Login to DockerHub
        ↓
Push Image to DockerHub

📂 Project Structure
nodejs-demo-app/
│
├── app.js
├── package.json
├── Dockerfile
└── .github/
    └── workflows/
        └── main.yml

🟢 Application Description

The application is a simple Express.js server that runs on port 3000 and returns a confirmation message to verify successful deployment.

🐳 Docker Implementation

The application is containerized using Docker.

Dockerfile Explanation:

Uses official Node.js 18 image

Sets working directory

Copies package.json

Installs dependencies

Copies application code

Exposes port 3000

Runs the application

This ensures consistency across environments.

⚙️ CI/CD Workflow Explanation

The GitHub Actions workflow:

Trigger:

Runs automatically on push to the main branch.

Workflow Steps:

Checkout repository code

Setup Node.js environment

Install dependencies

Run tests (placeholder)

Login to DockerHub using encrypted secrets

Build Docker image

Push image to DockerHub

🔐 Security Implementation

Sensitive credentials like DockerHub username and password are stored securely using:

GitHub → Settings → Secrets → Actions

Accessed in workflow using:

${{ secrets.DOCKER_USERNAME }}
${{ secrets.DOCKER_PASSWORD }}


This ensures that credentials are not exposed in logs or source code.

🚦 How to Run Locally (Optional)
1️⃣ Install dependencies
npm install

2️⃣ Start application
node app.js


Open browser:

http://localhost:3000

🐳 Run Using Docker
Build image:
docker build -t yourusername/nodejs-demo-app .

Run container:
docker run -p 3000:3000 yourusername/nodejs-demo-app

📦 DockerHub Deployment

After successful GitHub Actions execution:

The Docker image is automatically pushed to DockerHub repository:

https://hub.docker.com/r/yourusername/nodejs-demo-app

📈 Benefits of This CI/CD Pipeline

Automated builds

Reduced manual errors

Faster deployments

Secure credential management

Scalable containerized architecture

Industry-standard DevOps practice

🔍 Key DevOps Concepts Demonstrated

Continuous Integration

Continuous Deployment

Infrastructure Automation

Containerization

Secrets Management

Pipeline as Code (YAML)

💡 Future Improvements

Add automated testing using Jest

Implement multi-stage Docker builds

Add version tagging for Docker images

Deploy to cloud (AWS, Azure, GCP)

Add Slack/Email notifications on failure

Implement rollback mechanism

🎓 Learning Outcome

Through this project, I gained hands-on experience in:

Designing CI/CD workflows

Writing GitHub Actions YAML files

Building and pushing Docker images
