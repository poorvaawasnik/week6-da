📝 Spring Boot Blog Management REST API
📌 Project Description

A RESTful backend application for managing blog content using Spring Boot and Spring Data JPA. The system supports user authentication, blog post creation, categories, comments, and role-based access control. It follows layered architecture, REST standards, and database best practices.

🚀 Features:--

✔ User registration & login
✔ Role-based access (ADMIN / AUTHOR / USER)
✔ Create, update, delete blog posts
✔ Category-wise blog management
✔ Comment system on blog posts
✔ Pagination & sorting
✔ Search blogs by title / category
✔ Exception handling & validation
✔ PostgreSQL + JPA integration

🛠 Technology Stack

Java 17

Spring Boot 3.x

Spring Data JPA (Hibernate)

PostgreSQL

Lombok

Maven

REST APIs

Swagger (optional)

🗄️ Database Schema
Tables
users
posts
categories
comments

Relationships

One User → Many Posts

One Post → Many Comments

One Category → Many Posts

📂 Project Structure
blog-management-api/
│── src/main/java/com/blogapi/
│   ├── BlogApiApplication.java
│   ├── controller/
│   │   ├── AuthController.java
│   │   ├── PostController.java
│   │   ├── CategoryController.java
│   │   └── CommentController.java
│   ├── service/
│   │   ├── PostService.java
│   │   ├── CategoryService.java
│   │   ├── UserService.java
│   │   └── CommentService.java
│   ├── repository/
│   │   ├── PostRepository.java
│   │   ├── CategoryRepository.java
│   │   ├── UserRepository.java
│   │   └── CommentRepository.java
│   ├── model/
│   │   ├── entity/
│   │   ├── dto/
│   │   └── enums/
│   ├── config/
│   └── exception/
│
│── src/main/resources/
│   ├── application.yml
│   └── data.sql
│
│── pom.xml
│── README.md

🔗 API Endpoints
Authentication
POST /api/auth/register
POST /api/auth/login

Blog Posts
GET    /api/posts
GET    /api/posts/{id}
POST   /api/posts
PUT    /api/posts/{id}
DELETE /api/posts/{id}

Categories
GET  /api/categories
POST /api/categories

Comments
POST /api/posts/{postId}/comments
GET  /api/posts/{postId}/comments

⚙️ application.yml (Sample)
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/blog_db
    username: postgres
    password: password
  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true

🎯 Learning Outcomes

REST API design with Spring Boot

Entity relationships using JPA

Pagination & sorting

Exception handling

Clean layered architecture
