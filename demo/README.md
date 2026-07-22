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
                                                               ```





