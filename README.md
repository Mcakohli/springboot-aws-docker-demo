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
Backend: Java 17, Spring Boot 3, Spring Data JPA, RESTful API
Database: PostgreSQL on AWS RDS
Cloud Storage: Amazon S3 for file uploads
Containerization: Docker & Docker Hub
Cloud Infrastructure: AWS EC2 (Ubuntu Server)
CI/CD: GitHub Actions (Automated build, dockerize, and deploy workflow)

Key Features

REST API Endpoints: Complete CRUD operations with Spring Boot.
Data Persistence: Relational data mapping using JPA Hibernate connected to AWS RDS PostgreSQL.
Object Storage: Media/file handling seamlessly linked to Amazon S3.
Containerization: Clean Dockerfile packaging the app into a reproducible lightweight container.
CI/CD Automation: Automated workflow triggering on every git push origin main to build the JAR, push to Docker Hub, and redeploy on AWS EC2.

## 🚀 Deployment Screenshots

### 1. Spring Boot Maven Build Success
![Maven Build Success](https://raw.githubusercontent.com/Mcakohli/springboot-aws-docker-demo/main/docs/screenshots/05-maven-build-success.png)

### 2. AWS Infrastructure (RDS Database & S3 Storage)
| AWS RDS PostgreSQL | Amazon S3 Storage Bucket |
| :---: | :---: |
| ![AWS RDS](https://raw.githubusercontent.com/Mcakohli/springboot-aws-docker-demo/main/docs/screenshots/02-rds-database.png) | ![Amazon S3](https://raw.githubusercontent.com/Mcakohli/springboot-aws-docker-demo/main/docs/screenshots/01-s3-bucket.png) |

### 3. Docker Image Build & Registry Push
| Docker Image Push | Docker Hub Registry |
| :---: | :---: |
| ![Docker Push](https://raw.githubusercontent.com/Mcakohli/springboot-aws-docker-demo/main/docs/screenshots/dcoker%20push.png) | ![Docker Hub](https://raw.githubusercontent.com/Mcakohli/springboot-aws-docker-demo/main/docs/screenshots/04-docker-hub-push.png) |

### 4. AWS EC2 Container Deployment & Live Application
| AWS EC2 Instance | Live Application Deployment |
| :---: | :---: |
| ![AWS EC2 Instance](https://raw.githubusercontent.com/Mcakohli/springboot-aws-docker-demo/main/docs/screenshots/03-ec2-instance.png) | ![EC2 Live Deployment](https://raw.githubusercontent.com/Mcakohli/springboot-aws-docker-demo/main/docs/screenshots/06-ec2-deployment-live.png) |

### 5. Application Code & Structure
| Spring Boot AWS Config | Project Structure | S3 Config Code |
| :---: | :---: | :---: |
| ![Spring Boot AWS](https://raw.githubusercontent.com/Mcakohli/springboot-aws-docker-demo/main/docs/screenshots/springboot%20aws.png) | ![Project Structure](https://raw.githubusercontent.com/Mcakohli/springboot-aws-docker-demo/main/docs/screenshots/02-project-structure.png) | ![S3 Config Code](https://raw.githubusercontent.com/Mcakohli/springboot-aws-docker-demo/main/docs/screenshots/03-s3-config-code.png) |

3. Docker Image Build & Push to Docker Hub
4. AWS EC2 Container Deployment & Live Application
⚙️ How to Run Locally
Prerequisites

JDK 17+
Maven
Docker Desktop

1. Clone the Repository
git clone https://github.com/Mcakohli/springboot-aws-docker-demo.git
cd springboot-aws-docker-demo

2. Configure Environment Variables
Set up your database connection and AWS credentials in src/main/resources/application.yml or via environment variables:
spring:
  datasource:
    url: jdbc:postgresql://your-rds-endpoint.amazonaws.com:5432/postgres
    username: your_db_username
    password: your_db_password

aws:
  s3:
    bucket: your-s3-bucket-name

3. Build & Run via Docker
# Build Docker image
docker build -t springboot-aws-demo .

# Run Container
docker run -p 8080:8080 --name springboot-app springboot-aws-demo
Access the API locally at: http://localhost:8080

👨‍💻 Author
Rahul Kohli — GitHub Profile
