# BookMyShow - DevOps Project

## Project Overview
This project demonstrates the deployment of a BookMyShow React application using DevOps tools and practices.

## Technologies Used
- AWS EC2
- Git and GitHub
- Jenkins
- Docker
- Docker Hub
- Kubernetes (K3s)
- Ansible
- Prometheus
- Grafana

## Project Architecture

Developer → GitHub → Jenkins → Docker Build → Docker Hub → Kubernetes (K3s) → BookMyShow Application

## Application Details
- Frontend: React.js
- Containerization: Docker
- Web Server: Nginx
- Container Orchestration: Kubernetes (K3s)
- Kubernetes Deployment: 2 replicas
- Kubernetes Service: NodePort 30080

## Kubernetes Resources
- Namespace: bookmyshow
- Deployment: bms-app
- Service: bms-service

## Docker Image
bhartibhute/bookmyshow:v1

## Deployment Process
1. Push application changes to GitHub.
2. Jenkins checks out the source code.
3. Jenkins installs application dependencies.
4. Jenkins builds the React application.
5. Jenkins builds the Docker image.
6. Jenkins pushes the image to Docker Hub.
7. Jenkins deploys the application to Kubernetes.

## Project Status
The repository and deployment configuration are being prepared. Infrastructure setup and pipeline execution are planned as the next steps.
