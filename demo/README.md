# 🚀 Spring Boot AWS & Docker Deployment Pipeline

A production-ready Spring Boot microservice integrated with cloud-native AWS services (RDS PostgreSQL and S3 Storage), containerized with Docker, and deployed on an AWS EC2 instance with an automated GitHub Actions CI/CD pipeline.

---

## 🏗️ Architecture & Tech Stack

```text
[ Client / Postman ] 
        │
        ▼
   [ AWS EC2 ] ──▶ [ Docker Container (Spring Boot REST API) ]
                               │                 │
                               ▼                 ▼
                       [ AWS RDS ]           [ AWS S3 ]
                     (PostgreSQL DB)      (File/Media Storage)

                     Backend: Java 17, Spring Boot 3, Spring Data JPA, RESTful API

Database: PostgreSQL on AWS RDS

Cloud Storage: Amazon S3 for file uploads

Containerization: Docker & Docker Hub

Cloud Infrastructure: AWS EC2 (Ubuntu Server)

CI/CD: GitHub Actions (Automated build, dockerize, and deploy workflow)

🛠️ Key Features
REST API Endpoints: Complete CRUD operations with Spring Boot.

Data Persistence: Relational data mapping using JPA Hibernate connected to AWS RDS PostgreSQL.

Object Storage: Media/file handling seamlessly linked to Amazon S3.

Containerization: Clean Dockerfile packaging the app into a reproducible lightweight container.

CI/CD Automation: Automated workflow triggering on every git push origin main to build the JAR, push to Docker Hub, and redeploy on AWS EC2.

🚀 Deployment Screenshots
1. Docker Container Running Live on AWS EC2
⚙️ How to Run Locally
Prerequisites
JDK 17+

Maven

Docker Desktop