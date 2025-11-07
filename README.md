Project Overview

This project is a full-stack E-commerce Application built using Spring Boot for the backend. It provides a robust and scalable platform that manages products, users, orders, and payments efficiently. The goal of this project is to demonstrate the core functionalities of an online shopping system with secure APIs and modular architecture.

Features

User registration and authentication (JWT-based)

Role-based access control (Admin & Customer)

Product management (Add, update, delete, view)

Category and sub-category handling

Shopping cart functionality

Order placement and tracking

Payment gateway integration (mock or real)

RESTful APIs for frontend integration

Exception handling and validation

Secure backend with Spring Security

Technologies Used
Backend

Spring Boot – Core backend framework

Spring MVC – REST API development

Spring Data JPA (Hibernate) – ORM and database handling

Spring Security & JWT – Authentication and authorization

MySQL / PostgreSQL – Relational database

Lombok – Simplifies boilerplate code

Maven – Dependency management and build tool

Frontend (optional integration)

React / Angular – For user interface

Axios / Fetch API – For backend communication

Tools & Environment

Postman / Swagger UI – API testing and documentation

IntelliJ IDEA / VS Code / Eclipse – Development IDE

Git & GitHub – Version control and collaboration

Project Structure
Ecommerce-Spring-Boot/
│
├── src/main/java/com/example/ecommerce/
│   ├── controller/         # REST controllers
│   ├── model/              # Entity classes
│   ├── repository/         # Data access layer
│   ├── service/            # Business logic layer
│   ├── config/             # Security and application configuration
│   └── EcommerceApplication.java  # Main entry point
│
├── src/main/resources/
│   ├── application.properties     # Database and app configurations
│   └── data.sql / schema.sql      # Initial database setup (optional)
│
└── pom.xml                       # Maven dependencies

API Endpoints
Authentication
Method	Endpoint	Description
POST	/api/auth/register	Register a new user
POST	/api/auth/login	User login and JWT generation
Products
Method	Endpoint	Description
GET	/api/products	Get all products
GET	/api/products/{id}	Get product by ID
POST	/api/products	Add new product (Admin)
PUT	/api/products/{id}	Update product details
DELETE	/api/products/{id}	Delete a product
Orders
Method	Endpoint	Description
POST	/api/orders	Create new order
GET	/api/orders/{userId}	View orders by user
How to Run the Project

Clone the Repository

git clone https://github.com/your-username/Ecommerce-Spring-Boot.git
cd Ecommerce-Spring-Boot


Configure Database
Update application.properties with your database credentials:

spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce_db
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update


Build and Run

mvn clean install
mvn spring-boot:run


Access the Application

API Base URL: http://localhost:8080/api/

Swagger UI (if enabled): http://localhost:8080/swagger-ui.html

Future Enhancements

Add product reviews and ratings

Integrate real payment gateway (Stripe / Razorpay)

Implement inventory management

Add admin dashboard (React / Angular)

Introduce microservices architecture for scalability

License

This project is open-source and available for educational and personal use.
