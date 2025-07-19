🎓 Student Management API 
This project is a RESTful API built with Spring Boot that provides functionality to create, read, update, and delete (CRUD) student information.

## 🚀 Technologies

- Java 17+
- Spring Boot
- Spring Data JPA
- PostgreSQL
- Hibernate Validator

## 📁 Project Structure

com.project
├── domain // Entity classes
├── dto // Data Transfer Objects
├── enums // Enum types (Gender, Faculty)
├── mapper // Entity ↔ DTO mappers
├── repository // JpaRepository interfaces
├── resource // RestController endpoints
└── service // Business logic services

💻 API Endpoints  
| Method | Endpoint          | Description              |
| ------ | ----------------- | ------------------------ |
| POST   | /api/student      | Create a new student     |
| GET    | /api/student/{id} | Get student by ID        |
| GET    | /api/students     | Retrieve all students    |
| PUT    | /api/student/{id} | Update student fully     |
| PATCH  | /api/student/{id} | Update student partially |
| DELETE | /api/student/{id} | Delete student           |

⚙️ Database Configuration
application.yml:
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/student
    username: mohirdev
    password: 123
  jpa:
    hibernate:
      ddl-auto: update
    properties:
      hibernate:
        dialect: org.hibernate.dialect.PostgreSQLDialect
    show-sql: true

📝 Validations
- First name & last name: letters and spaces only
- Email: must be in valid format
- Phone number: e.g. +998901234567
- Date of birth: must be in the past
- Gender & Faculty: ENUM values


📄 License
This project is created for educational purposes. Feel free to use it as you wish.
