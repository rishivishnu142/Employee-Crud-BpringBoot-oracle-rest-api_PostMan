<div align="center">

# Employee CRUD REST API using Spring Boot, Oracle Database & Spring Data JPA

A production-ready RESTful Employee Management System developed using **Spring Boot**, **Spring Data JPA**, **Hibernate**, **Oracle Database**, and **Postman**. This project demonstrates enterprise-level backend development practices, including layered architecture, CRUD operations, data validation, RESTful API design, and Oracle database integration.

<p align="center">
  <img src="https://img.shields.io/badge/Java-17-orange?style=for-the-badge&logo=openjdk">
  <img src="https://img.shields.io/badge/Spring_Boot-4.1-green?style=for-the-badge&logo=springboot">
  <img src="https://img.shields.io/badge/Spring_Data_JPA-Repository-success?style=for-the-badge">
  <img src="https://img.shields.io/badge/Hibernate-ORM-brown?style=for-the-badge&logo=hibernate">
  <img src="https://img.shields.io/badge/Oracle-Database-red?style=for-the-badge&logo=oracle">
  <img src="https://img.shields.io/badge/Postman-API_Testing-orange?style=for-the-badge&logo=postman">
</p>

</div>

---

# Project Overview

This project is a RESTful Employee Management API built using Spring Boot and Oracle Database. It performs complete CRUD (Create, Read, Update, Delete) operations on employee records using Spring Data JPA and Hibernate.

The application follows a clean layered architecture that separates the Controller, Service, Repository, and Entity layers, making the code modular, maintainable, and scalable.

---

# Features

- Create Employee
- Retrieve All Employees
- Retrieve Employee by ID
- Update Employee
- Delete Employee
- Oracle Database Integration
- Spring Data JPA Repository
- Hibernate ORM
- RESTful Web Services
- Input Validation
- JSON Request & Response
- Maven Project Structure
- API Testing using Postman

---

# Technology Stack

| Technology | Description |
|------------|-------------|
| Java 17 | Programming Language |
| Spring Boot | Backend Framework |
| Spring Data JPA | Data Access Layer |
| Hibernate | ORM Framework |
| Oracle Database XE | Relational Database |
| Maven | Dependency Management |
| Eclipse IDE | Development Environment |
| Postman | REST API Testing |

---

# Project Architecture

```
                    Client / Postman
                           │
                     HTTP Request
                           │
                           ▼
                EmployeeController
                           │
                           ▼
                 EmployeeService
                           │
                           ▼
              EmployeeRepository
                           │
                           ▼
             Hibernate / Spring Data JPA
                           │
                           ▼
                   Oracle Database
```

---

# Project Structure

```
Employee-Crud-SpringBoot-Oracle

src
│
├── main
│   ├── java
│   │
│   └── com.employee.demo
│       │
│       ├── controller
│       │      EmployeeController.java
│       │
│       ├── entity
│       │      Employee.java
│       │
│       ├── repository
│       │      EmployeeRepository.java
│       │
│       ├── services
│       │      EmployeeService.java
│       │
│       └── EmployeeCrudOracleSpringApplication.java
│
└── resources
      application.properties
```

---

# REST API Endpoints

| HTTP Method | Endpoint | Description |
|--------------|---------------------------|-------------------------|
| GET | `/api/employees` | Retrieve all employees |
| GET | `/api/employees/{id}` | Retrieve employee by ID |
| POST | `/api/employees` | Create a new employee |
| PUT | `/api/employees/{id}` | Update an existing employee |
| DELETE | `/api/employees/{id}` | Delete employee |

---

# Sample Request

## Create Employee

```http
POST /api/employees
```

```json
{
    "name":"Rishikesh",
    "email":"rishi@gmail.com",
    "department":"IT",
    "salary":65000,
    "joinDate":"2026-07-14"
}
```

---

# Sample Response

```json
{
    "id":1,
    "name":"Rishikesh",
    "email":"rishi@gmail.com",
    "department":"IT",
    "salary":65000,
    "joinDate":"2026-07-14"
}
```

---

# Database Configuration

```properties
server.port=8099

spring.datasource.url=jdbc:oracle:thin:@//localhost:1521/XE
spring.datasource.username=system
spring.datasource.password=admin
spring.datasource.driver-class-name=oracle.jdbc.OracleDriver

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

---

# Running the Application

### Clone Repository

```bash
git clone https://github.com/rishivishnu142/Employee-Crud-BpringBoot-oracle-rest-api_PostMan.git
```

---

### Navigate to Project

```bash
cd Employee-Crud-BpringBoot-oracle-rest-api_PostMan
```

---

### Build Project

```bash
mvn clean install
```

---

### Run Spring Boot Application

```bash
mvn spring-boot:run
```

or run

```
EmployeeCrudOracleSpringApplication.java
```

from Eclipse or IntelliJ IDEA.

---

# API Base URL

```
http://localhost:8099/api
```

---

# Database Schema

**Employee**

| Column | Type |
|----------|------------|
| id | Long |
| name | String |
| email | String |
| department | String |
| salary | BigDecimal |
| joinDate | LocalDate |

---

# Validation Rules

The application validates:

- Employee Name must not be empty
- Email must not be empty
- Department must not be empty
- Salary must be greater than zero
- Join Date is mandatory

---

# Testing

The REST APIs have been tested using **Postman**.

Supported operations include:

- GET
- POST
- PUT
- DELETE

---

# Design Pattern

This project follows a layered architecture:

```
Controller
      │
      ▼
Service
      │
      ▼
Repository
      │
      ▼
Database
```

---

# Future Enhancements

- Spring Security
- JWT Authentication
- Swagger / OpenAPI Documentation
- Global Exception Handling
- Pagination & Sorting
- Search & Filter APIs
- Docker Deployment
- Unit Testing (JUnit & Mockito)
- Logging with SLF4J
- CI/CD Integration
- Role-Based Access Control (RBAC)

---

# Learning Outcomes

This project demonstrates practical knowledge of:

- Spring Boot
- Spring Data JPA
- Hibernate ORM
- Oracle Database Integration
- RESTful API Design
- CRUD Operations
- Dependency Injection
- Layered Architecture
- Maven Build Tool
- API Testing with Postman
- Input Validation
- Repository Pattern

---

# Author

**Rishikesh V**

GitHub: **https://github.com/rishivishnu142**

---

# License

This project is licensed under the **MIT License**.

Feel free to use, modify, and distribute this project for educational and learning purposes.

---

<div align="center">

### ⭐ If you found this project useful, please consider giving it a Star.

**Happy Coding! 🚀**

</div>
