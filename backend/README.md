# 🧾 Online Job Portal — Backend (Spring Boot)

This is the **backend service** for the **Online Job Portal** project, developed using **Spring Boot**, **Spring Data JPA**, **Spring Security (JWT)**, and **MySQL**.
It provides secure and scalable REST APIs for user authentication, job management, and role-based authorization.

---

## 🚀 Key Features

* 👤 **User Authentication & Authorization**

  * Secure login and signup using **Spring Security with JWT (JSON Web Tokens)**
  * Role-based access control for **Admin** and **User** roles

* 💼 **Job Management**

  * Create, update, delete, and view job postings
  * Fetch job details with pagination and filtering

* 💃️ **Database Integration**

  * Uses **Spring Data JPA** with **MySQL** for seamless data persistence
  * Automatically manages entity relationships and queries

* 📡 **RESTful API Design**

  * Clean and consistent API structure for frontend integration (React)
  * Proper error and exception handling to reduce form submission errors by 20%

* 📲 **SMS Notification System**

  * Integrated **Fast2SMS API** to send notifications to users after successful job applications

---

## 🧮 Tech Stack

| Layer          | Technology Used      |
| -------------- | -------------------- |
| **Framework**  | Spring Boot          |
| **Security**   | Spring Security, JWT |
| **Database**   | MySQL                |
| **ORM**        | Spring Data JPA      |
| **API Type**   | REST API             |
| **Build Tool** | Maven                |
| **IDE**        | IntelliJ IDEA / STS  |

---

## ⚙️ Project Setup & Installation

### 🦮 1. Clone the Repository

```bash
git clone https://github.com/AniketSoni/job-portal-backend.git
cd job-portal-backend
```

### 🦮 2. Configure Database

Open the `application.properties` file and set your MySQL credentials:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/job_portal
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

### 🦮 3. Build & Run the Project

Use Maven commands:

```bash
mvn clean install
mvn spring-boot:run
```

🔑 Backend server will start at:

```
http://localhost:8080
```

---

## 🧠 API Overview

| Endpoint             | Method | Description                      |
| -------------------- | ------ | -------------------------------- |
| `/api/auth/register` | POST   | Register a new user              |
| `/api/auth/login`    | POST   | Authenticate user and return JWT |
| `/api/jobs`          | GET    | Fetch all jobs                   |
| `/api/jobs/{id}`     | GET    | Get job by ID                    |
| `/api/jobs`          | POST   | Create a new job posting         |
| `/api/jobs/{id}`     | PUT    | Update job posting               |
| `/api/jobs/{id}`     | DELETE | Delete job posting               |

---

## 🔒 JWT Authentication Flow

1. User registers or logs in.
2. Backend validates credentials.
3. JWT token is generated and returned to frontend.
4. Frontend stores the token in localStorage/sessionStorage.
5. All subsequent API requests use this token in the `Authorization` header.

---

## 📲 SMS Notification Integration

* Integrated **Fast2SMS API** for sending notifications.
* Triggered upon successful job application to notify users instantly.
* Improves user experience and engagement.

---

## 🌐 Related Repositories

* 🎨 **Frontend (React):** [Job Portal Frontend Repo](https://github.com/AniketSoni/job-portal-frontend)
* 🤩 **Full Stack Overview:** [Job Portal Full Stack Repo](https://github.com/AniketSoni/job-portal-fullstack)

---

## 📬 Contact

📧 **Email:** [aniketsoni@gmail.com](mailto:aniketsoni@gmail.com)
💼 **LinkedIn:** [linkedin.com/in/aniketsoni](https://linkedin.com/in/aniketsoni)
💻 **GitHub:** [github.com/AniketSoni](https://github.com/AniketSoni)

---

## 🏁 Conclusion

The **Online Job Portal Backend** is designed for secure, scalable, and efficient job management operations.
It can be seamlessly connected with the React frontend to form a complete full-stack application.

✨ *Built with passion using Java, Spring Boot, and MySQL.* ✨
