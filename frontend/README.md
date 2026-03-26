# 💼 Online Job Portal - Frontend

The **Online Job Portal** is a full-stack web application built using **React**, **Spring Boot**, and **MySQL**, designed to simplify the job search and hiring process. It allows users to register, authenticate, and manage job postings dynamically while maintaining strong security through JWT authentication. The platform supports real-time SMS notifications for job applications and provides separate dashboards for different user roles — Admin, Employer, and Candidate.

---

## 🚀 Features

* 🧑‍💼 **User Management** – Register new users, authenticate securely, and manage job postings.
* 🔒 **Role-Based Authentication** – Implemented with **Spring Security** and **JWT**, ensuring access control for Admin, Employer, and Candidate roles.
* 🧾 **Job Posting System** – Employers can post, update, and delete job listings; candidates can view and apply for jobs.
* 💬 **SMS Notifications** – Integrated **Fast2SMS API** to notify users upon successful job applications.
* ⚙️ **Error Handling & Validation** – Client-side and server-side validation using **React Hook Form** and **Spring Validation**.
* 📱 **Responsive UI** – Built with **React** and **Tailwind CSS** for an elegant, mobile-friendly experience.
* 💾 **Secure Data Handling** – Passwords encrypted using **BCrypt**, and APIs are stateless for scalability.

---

## 🧰 Tech Stack

### 🖥️ Frontend

* React
* React Hook Form
* React Router DOM
* Tailwind CSS
* Axios

### ⚙️ Backend

* Spring Boot
* Spring MVC
* Spring Data JPA
* Spring Security (JWT)
* RESTful API
* Fast2SMS API
* MySQL

---

## 🗂️ Folder Structure

```
online-job-portal/
├─ frontend/
│  ├─ src/
│  │  ├─ components/
│  │  ├─ pages/
│  │  ├─ services/
│  │  ├─ App.jsx
│  │  └─ main.jsx
│  ├─ package.json
│  ├─ vite.config.js
│  └─ .gitignore
│
└─ backend/
   ├─ src/
   │  ├─ main/
   │  │  ├─ java/com/jobportal/
   │  │  │  ├─ controller/
   │  │  │  ├─ service/
   │  │  │  ├─ repository/
   │  │  │  └─ model/
   │  │  └─ resources/
   │  │      └─ application.properties
   ├─ pom.xml
   └─ .gitignore
```

---

## ⚙️ Setup and Installation (Frontend + Backend)

### 🔹 Prerequisites

Make sure the following are installed:

* Node.js (v16+)
* npm (v8+)
* Java 17 or later
* MySQL Server
* IDE (IntelliJ IDEA / Eclipse / VS Code)
* Postman (for API testing)

---

## 🖥️ Frontend Setup (React)

1️⃣ **Clone the repository**

```bash
git clone https://github.com/yourusername/online-job-portal.git
```

2️⃣ **Move to frontend folder**

```bash
cd online-job-portal/frontend
```

3️⃣ **Install dependencies**

```bash
npm install
```

4️⃣ **Run the frontend server**

```bash
npm run dev
```

The frontend will start on
👉 **[http://localhost:5173](http://localhost:5173)**

---

## ⚙️ Backend Setup (Spring Boot)

1️⃣ **Open Backend Project**
Open the `backend` folder in **IntelliJ IDEA** or **Eclipse**.

2️⃣ **Configure Database**
In `src/main/resources/application.properties`, update with your MySQL credentials:

```properties
# ===============================
# DATABASE CONFIGURATION
# ===============================
spring.datasource.url=jdbc:mysql://localhost:3306/job_portal
spring.datasource.username=root
spring.datasource.password=yourpassword

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

# ===============================
# JWT CONFIGURATION
# ===============================
jwt.secret=your_secret_key

# ===============================
# SERVER CONFIGURATION
# ===============================
server.port=8080
```

3️⃣ **Run the Application**
Run the main class:
`src/main/java/com/jobportal/JobPortalApplication.java`

Your backend will start on
👉 **[http://localhost:8080](http://localhost:8080)**

---

## 🔗 Connecting Frontend and Backend

In your React project (inside `src/services/api.js` or wherever you configure Axios):

```javascript
const BASE_URL = "http://localhost:8080/api";
```

All requests like registration, login, and job posting will go through this base URL.

Example:

```javascript
axios.post(`${BASE_URL}/auth/register`, userData);
```

---

## 🧠 API Endpoints

| Method | Endpoint             | Description                  |
| ------ | -------------------- | ---------------------------- |
| `POST` | `/api/auth/register` | Register new user            |
| `POST` | `/api/auth/login`    | Authenticate and receive JWT |
| `GET`  | `/api/jobs`          | Fetch all job posts          |
| `POST` | `/api/jobs`          | Create new job post          |
| `POST` | `/api/apply/{jobId}` | Apply for a job              |
| `GET`  | `/api/users/{id}`    | Fetch user profile           |

Use **Postman** to test these APIs. Make sure JWT is passed in headers:

```
Authorization: Bearer <your-token>
```

---

## 🔒 Security and Authentication

* Implemented **JWT (JSON Web Token)** for secure user authentication.
* **Spring Security** ensures only authorized roles can access endpoints.
* Passwords are hashed with **BCrypt**.
* Stateless authentication for scalability and API independence.

---

## 📲 SMS Notification Integration

Integrated **Fast2SMS API** to send SMS notifications when a user successfully applies for a job.

**Example SMS:**

> “Hello Aniket! Your application for *React Developer* has been submitted successfully.”

---

## 🧪 Testing

All APIs tested using **Postman**:

* Registration and login validation
* Job posting and update
* JWT-based authorization
* Exception handling

---

## 🧾 Error Handling

* **Frontend:** Validations using `React Hook Form` to prevent invalid submissions.
* **Backend:** Custom exception handlers using `@ControllerAdvice` in Spring Boot.
* Unified error responses ensure smooth client-server communication.

---

## 🌐 Deployment

### Frontend:

* Can be deployed on **Vercel**, **Netlify**, or **GitHub Pages**

### Backend:

* Deploy on **Render**, **Railway**, or **Heroku**
* Host database on **MySQL Cloud (e.g., PlanetScale / AWS RDS)**

---

## 📸 Screenshots (Add Later)

You can add screenshots once ready. Example format:

```markdown
![Login Page](screenshots/login.png)
![Dashboard](screenshots/dashboard.png)
```

---

## 🧑‍💻 Author

**👤 Aniket Soni**
💼 Java Full Stack Developer
📧 Email: [[your-email@example.com](mailto:your-email@example.com)]
🔗 LinkedIn: [your-linkedin-profile]
🐙 GitHub: [https://github.com/yourusername](https://github.com/yourusername)

---

## ⭐ Support and Feedback

If you found this project helpful, please give it a **⭐ Star** on GitHub.
Your support motivates me to build more amazing full-stack applications! 🚀
