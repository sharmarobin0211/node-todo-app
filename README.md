# 🚀 Serverless Dockerized App Deployment on AWS

This project automates the deployment of a containerized application using **AWS services** in a serverless architecture. It pulls code from GitHub, builds and stores Docker images, and deploys them using Amazon ECS (Fargate). Logs are stored and monitored via Amazon CloudWatch.

---

## 🧱 Architecture Overview

### ✅ Services Used:
- **GitHub** – Source code repository
- **Amazon EC2** – Builds Docker image from source
- **Amazon ECR** – Stores Docker images
- **Amazon ECS (Fargate)** – Runs containers serverlessly
- **Amazon CloudWatch** – Centralized logging and monitoring

---
## 📁 Project Structure

.
├── Dockerfile # Docker build instructions
├── app/ # Application code
├── scripts/
│ └── deploy.sh # Shell script for build and deployment
├── ecs-task-definition.json # ECS Task definition (Fargate)
└── README.md # Project documentation

---

## ⚙️ Setup & Deployment

### 1. 📦 Clone the Repository

git clone https://github.com/sharmarobin0211/nodo-todo-app

  2. 🔑 Configure AWS Credentials
   
Make sure your EC2 instance has the appropriate IAM role or manually configure AWS CLI:
aws configure

  3. 🐳 Build and Push Docker Image

Docker image is built from Dockerfile

Image is pushed to ECR

ECS task and service are updated


📊 Monitoring
Application logs are automatically streamed to Amazon CloudWatch Logs.

Monitor ECS service and tasks via the AWS Console or CLI.

📌 Prerequisites
An ECR repository created in your AWS account

An ECS cluster (Fargate) with task and service roles configured

IAM Role with permissions: ECR, ECS, CloudWatchLogs, EC2.

