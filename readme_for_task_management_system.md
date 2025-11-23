# Smart Task Management System
A full-stack **Java Spring Boot + MySQL** application with **JWT Authentication, Role-Based Access, CRUD, Logging, Global Exception Handling, and Pagination/Sorting**.

This project is designed to backend development.

---

# 🚀 Features
- User Registration & Login (JWT Based)
- Role-Based Authorization (ADMIN / USER)
- Create, Update, Delete Tasks
- Assign Tasks to Users
- Pagination & Sorting
- Global Exception Handling
- Logging using SLF4J
- Clean 3-Layer Architecture (Controller → Service → Repository)
- MySQL Database

---

# 🏗️ Tech Stack
**Backend:** Java 17+, Spring Boot, Spring Security, JWT, JPA/Hibernate

**Database:** MySQL

**Build Tool:** Maven

**Tools:** Postman, GitHub, IntelliJ/Eclipse

---

# 📁 Project Structure
```
src/main/java/com/taskmanagement
│
├── controller
├── service
│   ├── impl
├── repository
├── entity
├── security
│   ├── filters
│   ├── config
├── exception
└── payload
```

---

# ⚙️ Setup Instructions

## 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/task-management-system.git
cd task-management-system
```

## 2. Configure the database (MySQL)
Create the database:
```sql
CREATE DATABASE task_management;
```

Update `src/main/resources/application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/task_management
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD
```

## 3. Run the project
Using Maven:
```bash
mvn spring-boot:run
```

Or using Java:
```bash
java -jar target/task-management-system.jar
```

---

# 🔐 Authentication Flow (JWT)
- User registers using `/auth/register`
- User logs in using `/auth/login`
- API returns JWT Token
- Client stores token
- User calls all protected APIs by passing token in header:
```
Authorization: Bearer <TOKEN>
```

---

# 📌 API Endpoints

## Authentication
| Method | Endpoint          | Description |
|--------|-------------------|-------------|
| POST   | /auth/register    | Register user |
| POST   | /auth/login       | Login & get token |

## Task Management
| Method | Endpoint          | Description |
|--------|-------------------|-------------|
| POST   | /tasks            | Create task |
| GET    | /tasks            | List tasks with pagination |
| PUT    | /tasks/{id}       | Update task |
| DELETE | /tasks/{id}       | Delete task |

---

# 🧪 Testing with Postman
Add this header for all task APIs:
```
Authorization: Bearer <your_token>
```

---

# 📝 Logging
SLF4J logs request processing, errors, and database operations.

---

# 🚀 Deployment (Optional)
### Build JAR
```bash
mvn clean package
```
### Run
```bash
java -jar target/task-management-system.jar
```

---

# ⭐ How to Push This Project to GitHub (All Commands)

## 1. Initialize Git
```bash
git init
```

## 2. Add all files
```bash
git add .
```

## 3. Commit
```bash
git commit -m "Initial commit - Task Management System"
```

## 4. Create GitHub Repo
Go to GitHub → New Repository → Name: `task-management-system`

## 5. Add Remote
```bash
git remote add origin https://github.com/YOUR_USERNAME/task-management-system.git
```

## 6. Push to GitHub
```bash
git branch -M main
git push -u origin main
```

---

# 🎯 Final Notes
This project is designed exactly like real-world enterprise systems and is perfect for:
- Interviews
- Resume / GitHub Portfolio
- Learning Spring Boot end-to-end

