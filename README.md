# 🧾 Job Portal — Full Stack

## 📌 Description
Full-stack job portal built with React and Spring Boot featuring JWT-based authentication, role-based access control, and job management system.

## 🚀 Tech Stack
- React.js
- Spring Boot
- Spring Security (JWT)
- MySQL
- REST APIs

## ✨ Features
- Role-based authentication (Employer/Employee)
- JWT-based secure login system
- Job posting, updating, and deletion
- Job application system for users
- Job search with filters (category, type, salary)
- Responsive UI with real-time form validation

## 🏗️ Architecture
- Frontend: React application for UI, forms, and routing
- Backend: Spring Boot REST APIs with authentication and business logic
- Database: MySQL for persistent storage

## 🔧 API / Backend
- Spring Boot REST APIs
- JWT Authentication & Authorization
- MySQL integration using Spring Data JPA
- SMS integration using Fast2SMS API

## ⚙️ Configuration

## Update your application.properties:
```bash
spring.datasource.url=jdbc:mysql://localhost:3306/your_database
spring.datasource.username=your_username
spring.datasource.password=your_password

jwt.secret=your_secret_key 
```

## ⚙️ Run Locally

## Backend
```bash
cd backend
mvn spring-boot:run
```

## Frontend
```bash
cd frontend
npm install
npm run dev
```