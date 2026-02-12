# 🚀 CI/CD Pipeline using Jenkins & Docker

## 📌 Project Overview

This project demonstrates a complete CI/CD pipeline that automates the build and deployment of a Dockerized static web application using Jenkins.

Whenever code is pushed to GitHub, Jenkins automatically:

1. Checks out the latest source code
2. Builds a Docker image
3. Stops the existing container (if running)
4. Deploys a new container with updated changes

This eliminates manual deployment and ensures faster and reliable delivery.

---

## 🎯 Objective

To implement an automated Continuous Integration and Continuous Deployment (CI/CD) workflow using:

- GitHub as Source Code Management
- Jenkins for Automation
- Docker for Containerization
- Nginx for Web Server
- Windows-based Jenkins Agent
- WSL Ubuntu for development

---

## 🏗️ Architecture Workflow

Developer → GitHub → Jenkins → Docker Build → Docker Container → Browser

---

## 🛠️ Tools & Technologies Used

- Git & GitHub
- Jenkins (Pipeline)
- Docker
- Nginx
- HTML
- Windows 11
- WSL Ubuntu

---

## 📂 Project Structure

unlox-ci-cd/
│
├── index.html
├── Dockerfile
├── Jenkinsfile
├── README.md
└── screenshots/


---

## ⚙️ Pipeline Stages

### 1️⃣ Checkout Source Code
Jenkins automatically pulls the latest code from the GitHub repository.

### 2️⃣ Build Docker Image
docker build -t unlox-project .


### 3️⃣ Stop Old Container


docker stop unlox-cid
docker rm unlox-cid


### 4️⃣ Deploy New Container


docker run -d -p 8086:80 --name unlox-cid unlox-project


---

## 🌐 Application Access

After successful deployment, the application is accessible at:



http://localhost:8086


---

## 🔄 CI/CD Flow Explanation

1. Developer pushes changes to GitHub
2. Jenkins pipeline triggers build
3. Docker image is created
4. Existing container is removed
5. New container is deployed automatically

---

## 🚧 Challenges Faced & Solutions

| Issue | Solution |
|-------|----------|
| Git authentication error | Used Personal Access Token |
| Jenkins executor not available | Resolved disk space issue |
| Branch mismatch (main vs master) | Configured correct branch |
| Windows agent scripting issue | Used `bat` instead of `sh` |

---

## 📈 Future Enhancements

- Deploy to AWS EC2
- Add automated testing stage
- Push Docker image to Docker Hub
- Implement GitHub Webhooks for auto-trigger

---

## 👨‍💻 Author

Harish  
DevOps Enthusiast  
