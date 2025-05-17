
# Spring PetClinic Sample Application [![Build Status](https://github.com/spring-projects/spring-petclinic/actions/workflows/maven-build.yml/badge.svg)](https://github.com/spring-projects/spring-petclinic/actions/workflows/maven-build.yml)[![Build Status](https://github.com/spring-projects/spring-petclinic/actions/workflows/gradle-build.yml/badge.svg)](https://github.com/spring-projects/spring-petclinic/actions/workflows/gradle-build.yml)
# Prod-SpringBoot-Pet-App 🚀  
[![Azure DevOps CI/CD](https://img.shields.io/badge/Azure%20DevOps-CI%2FCD-blue?logo=azure-devops)](https://azure.microsoft.com/en-us/services/devops/)
[![Java](https://img.shields.io/badge/Java-17-red?logo=java)](https://www.oracle.com/java/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-green?logo=spring-boot)](https://spring.io/projects/spring-boot)
[![Docker](https://img.shields.io/badge/Docker-Containerized-blue?logo=docker)](https://www.docker.com/)
[![Maven](https://img.shields.io/badge/Maven-Build-orange?logo=apache-maven)](https://maven.apache.org/)
[![SonarQube](https://img.shields.io/badge/SonarQube-Code%20Quality-brightgreen?logo=sonarqube)](https://www.sonarsource.com/)
[![JFrog Artifactory](https://img.shields.io/badge/Artifacts-JFrog-yellowgreen?logo=jfrog)](https://jfrog.com/)
[![Trivy Scan](https://img.shields.io/badge/Security-Trivy-critical?logo=aqua)](https://aquasecurity.github.io/trivy/)
[![Deployed to Azure](https://img.shields.io/badge/Deployed-Azure%20Container%20Instance-0078D4?logo=microsoft-azure)](https://azure.microsoft.com/en-us/services/container-instances/)

# DevSecOps CI/CD Pipeline with Azure DevOps 🚀

This repository demonstrates a complete **CI/CD pipeline** implementation using **Azure DevOps**, covering phases from code integration to secure deployment, aligned with DevSecOps best practices.

> 🛠️ Forked & built upon the original work by [mentor name or repo if you want to credit], but executed, customized, and deployed fully by me.

---

## 📌 Project Goals

- Automate code build, test, and deployment pipelines.
- Perform **Static Application Security Testing (SAST)** and **Dynamic Application Security Testing (DAST)**.
- Integrate **SonarQube**, **JFrog Artifactory**, **Azure Blob Storage**, **Docker Hub**, and **Azure Container Registry (ACR)**.
- Deploy across multiple environments: **Staging**, **Production**, and **Azure Container Instance (ACI)**.

---

## 🔄 CI/CD Pipeline Overview

### 1. **Continuous Integration (CI)**

- ✅ Code Commit & Merge (GitHub → Azure Repos)
- ✅ **SAST** via SonarQube
- ✅ Build with Maven (skipping tests where needed)
- ✅ Docker image creation
- ✅ Artifact upload to:
  - Azure Blob Storage
  - AWS S3
  - JFrog Artifactory

### 2. **Continuous Delivery (CD)**

- ✅ Automated deployments to **Development** and **Staging**
- ✅ Manual approvals where required
- ✅ Integration testing environment readiness

### 3. **Continuous Deployment (CD)**

- ✅ Production push (manual approval step)
- ✅ Azure Container Instance (ACI) Deployment
- ✅ Verification via Route 53 subdomains (e.g., `staging.cloudvishwakarma.in`)

---

## 🔧 Tools & Technologies

| Purpose                | Tool/Service           |
|------------------------|------------------------|
| Version Control        | GitHub + Azure Repos   |
| CI/CD                  | Azure DevOps Pipelines |
| Build Tool             | Maven                  |
| Containerization       | Docker                 |
| Code Quality           | SonarQube              |
| Security Scanning      | Trivy, OWASP ZAP       |
| Artifact Repository    | JFrog + Azure Blob + AWS S3 |
| Cloud Platforms        | AWS + Azure            |
| DNS Routing            | AWS Route53            |

---

## 🗃️ Branching Strategy

- `main`: Production-ready code
- `dev`: Active development branch
- `feature/*`: Feature-specific development
- `hotfix/*`: Production hotfixes

---

## 🚀 Deployment Environments

| Environment | Platform   | IP/URL                            |
|-------------|------------|-----------------------------------|
| Staging     | AWS EC2    | `staging.cloudvishwakarma.in`     |
| Production  | AWS EC2    | `prod.cloudvishwakarma.in`        |
| ACI         | Azure ACI  | `http://<ACI-FQDN>:8080`          |

---

## ✅ Pipeline Execution Summary

- [x] Azure DevOps Agent Setup on Ubuntu VM (AWS)
- [x] Created and tested self-hosted agent pool
- [x] PAT generation and agent registration
- [x] CI: Build, Dockerize, and publish artifacts
- [x] CD: Deploy to multiple environments
- [x] SAST with SonarQube
- [x] DAST with ZAP scan
- [x] Trivy image vulnerability scanning
- [x] Multi-registry support: ACR + Docker Hub

---

## 📂 Folder Structure



## Understanding the Spring Petclinic application with a few diagrams

<img width="1042" alt="petclinic-screenshot" src="https://cloud.githubusercontent.com/assets/838318/19727082/2aee6d6c-9b8e-11e6-81fe-e889a5ddfded.png">

