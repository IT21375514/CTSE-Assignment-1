# CTSE Assignment 1 - User Authentication Microservice

This project is a containerized Node.js Express microservice deployed on Azure Web App, with CI/CD enabled using GitHub Actions.

## 👥 Group Members

- **Sanjayan. C** – IT21375514  
- **Balakrishnan K. D** – IT21194894  
- **Shandeep. J** – IT21375682  

## 🔧 Features
- User registration and login with JWT
- User management
- MongoDB Atlas integration
- Dockerized and deployed via Azure Web App
- CI/CD with GitHub Actions and Snyk vulnerability scanning

## 🚀 Deployment Overview

The service is deployed on **Azure Web App for Containers**, with the container image pulled directly from **Docker Hub**. Deployment is automated via a GitHub Actions workflow, which builds the Docker image, runs security scans, pushes it to Docker Hub, and deploys it to Azure using a publish profile.

## 🛡️ GitHub Repository Secrets

The CI/CD pipeline uses sensitive credentials for deployment and scanning. These must be added as **GitHub Repository Secrets** under:

**Repository → Settings → Secrets and variables → Actions**

| Secret Name              | Description                                       |
|--------------------------|---------------------------------------------------|
| `DOCKER_USERNAME`        | Your Docker Hub username                          |
| `DOCKER_PASSWORD`        | Docker Hub access token (used instead of password)|
| `AZURE_PUBLISH_PROFILE`  | Azure Web App publish profile (Base64 XML format) |
| `SNYK_TOKEN`             | Token from Snyk for running vulnerability scans   |

## 🛠️ Setup

1. Clone the repo  
2. Run `npm install`  
3. Set environment variables in `.env`  
4. Run with `npm start`  
5. Set up Azure Web App for Containers  
6. Configure environment variables in Azure  
7. Connect Snyk to the repository    
8. Add GitHub repository secrets