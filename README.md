# 🚀 CI/CD EKS Deployment Pipeline

A complete DevOps project demonstrating Continuous Integration and Continuous Deployment (CI/CD) of containerized applications on Amazon EKS using GitHub Actions, Docker, Terraform, Kubernetes, and Amazon ECR.

---

## 📌 Overview

This project automates the entire application deployment lifecycle using GitHub Actions workflows.

The pipeline performs:

* Source Code Validation
* Automated Testing
* Docker Image Build
* Docker Image Push to Amazon ECR
* Infrastructure Provisioning using Terraform
* Kubernetes Deployment using Kustomize
* Continuous Deployment to Amazon EKS

---

## 🏗️ Architecture

```text
Developer
    │
    ▼
GitHub Repository
    │
    ▼
GitHub Actions
    │
    ▼
Docker Build
    │
    ▼
Amazon ECR
    │
    ▼
Terraform
    │
    ▼
Amazon EKS
    │
    ▼
Kubernetes Deployment
    │
    ▼
Application Access
```

---

## 📂 Repository Structure

```text
CI-CD_EKS_deployment_pipeline
│
├── workflows/
│   ├── ci.yml
│   ├── deployment.yml
│   └── cd-production.yml
│
├── app.py
├── index.js
├── calculator.js
├── calculator.test.js
├── package.json
├── requirements.txt
│
├── Dockerfile
├── Dockerfile-python
├── docker-compose.yml
├── nginx.conf
│
├── deploy.yaml
├── ingress.yaml
├── svc.yaml
├── kustomization.yaml
│
├── main.tf
├── variables.tf
├── outputs.tf
├── terraform.tf
├── ingress-nginx.tf
│
├── VERSION
└── README.md
```

---

## ⚙️ Prerequisites

Install the following tools before deployment:

* AWS CLI
* Docker
* Kubernetes CLI (kubectl)
* Terraform
* Git
* Node.js
* Python
* GitHub Actions

AWS Services:

* Amazon EKS
* Amazon ECR
* IAM
* VPC
* CloudWatch

---

## 🔄 CI/CD Workflow

### Continuous Integration

GitHub Actions performs:

* Source Checkout
* Dependency Installation
* Unit Testing
* Build Validation

### Docker Build

```bash
docker build -t application .
```

### Push Image to ECR

```bash
docker push <ecr-repository>
```

### Infrastructure Provisioning

```bash
terraform init
terraform plan
terraform apply
```

### Kubernetes Deployment

```bash
kubectl apply -k .
```

Resources Created:

* Deployment
* Service
* Ingress

---

## ☁️ Infrastructure Components

### Amazon EKS

Managed Kubernetes cluster for application deployment.

### Amazon ECR

Stores container images.

### Terraform

Automates infrastructure provisioning.

### IAM

Controls access permissions.

### CloudWatch

Provides monitoring and logging capabilities.

---

## 📦 Deployment Environments

### Development

```bash
kubectl apply -k dev
```

### Staging

```bash
kubectl apply -k staging
```

### Production

```bash
kubectl apply -k prod
```

---

## 🔒 Security Features

* GitHub Secrets for credential management
* IAM Role-Based Access Control
* Secure Container Deployment
* Infrastructure as Code
* Kubernetes Resource Isolation

---

## 📊 Monitoring

Monitoring and logging are enabled through:

* AWS CloudWatch
* GitHub Actions Logs
* Kubernetes Logs

---

## 🛠️ Technologies Used

| Technology     | Purpose                 |
| -------------- | ----------------------- |
| AWS EKS        | Container Orchestration |
| Amazon ECR     | Image Repository        |
| Docker         | Containerization        |
| Kubernetes     | Deployment Management   |
| Terraform      | Infrastructure as Code  |
| GitHub Actions | CI/CD Automation        |
| Nginx          | Reverse Proxy           |
| Node.js        | Application Runtime     |
| Python         | Backend Services        |

---

## 🎯 Key Learning Areas

* DevOps Automation
* CI/CD Pipeline Design
* Kubernetes Administration
* Docker Containerization
* AWS Cloud Services
* Infrastructure as Code
* GitOps Practices

---

## 👨‍💻 Author

**Libin Priyadarsan R**

DevOps & Cloud Enthusiast

Specializations:

* AWS Cloud
* Kubernetes
* Docker
* Terraform
* GitHub Actions
* CI/CD Automation

---

## ⭐ Project Status

Completed and maintained as a DevOps learning and deployment automation project.
