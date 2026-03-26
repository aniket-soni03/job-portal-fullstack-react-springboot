# 🧾 Job Portal — Backend

## 📌 Description
Backend service for the job portal built using Spring Boot providing secure REST APIs for authentication, job management, and role-based access control.

## 🚀 Tech Stack
- Spring Boot
- Spring Security (JWT)
- Spring Data JPA
- MySQL
- REST APIs
- Maven

## ✨ Features
- JWT-based authentication and authorization
- Role-based access control (Employer/Employee)
- Create, update, delete, and view job postings
- Job search with pagination and filtering
- RESTful API design for frontend integration
- Exception handling for stable API responses
- SMS notification using Fast2SMS API

## 🔧 API Overview
- POST /api/auth/register → Register new user
- POST /api/auth/login → Authenticate user and return JWT
- GET /api/jobs → Fetch all jobs
- GET /api/jobs/{id} → Get job by ID
- POST /api/jobs → Create job
- PUT /api/jobs/{id} → Update job
- DELETE /api/jobs/{id} → Delete job

## 🔒 Authentication
- JWT-based authentication using Spring Security
- Token-based authorization for protected endpoints

## ⚙️ Run Locally

```bash
cd backend
mvn spring-boot:run

⚙️ Configuration

Update application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/job_portal
spring.datasource.username=your_username
spring.datasource.password=your_password
jwt.secret=yourSecretKey
fast2sms.apiKey=yourFast2SMSKey