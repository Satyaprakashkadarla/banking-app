# Banking Application

A RESTful Banking Application built using **Spring Boot**, **Spring Data JPA (Hibernate)**, and **MySQL**. This project demonstrates how to develop secure and scalable banking APIs for account management, deposits, withdrawals, and account operations.

## Features

* Create a new bank account
* Get account details by ID
* Deposit money into an account
* Withdraw money from an account
* Retrieve all bank accounts
* Delete a bank account
* RESTful API architecture
* MySQL database integration
* Spring Data JPA (Hibernate) for ORM

## Tech Stack

* Java 21
* Spring Boot 3.x
* Spring Data JPA (Hibernate)
* MySQL
* Maven
* Lombok
* IntelliJ IDEA
* Postman

## Project Structure

```text
src
└── main
    ├── java
    │   └── net.javaguides.banking_app
    │       ├── controller
    │       ├── dto
    │       ├── entity
    │       ├── mapper
    │       ├── repository
    │       ├── service
    │       │   └── impl
    │       └── BankingAppApplication.java
    │
    └── resources
        └── application.properties
```

## Database Configuration

Update `application.properties` with your MySQL credentials:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/banking_app
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

## API Endpoints

### Create Account

```http
POST /api/accounts
```

Request Body:

```json
{
  "accountHolderName": "John Doe",
  "balance": 1000
}
```

### Get Account By ID

```http
GET /api/accounts/{id}
```

### Deposit Amount

```http
PUT /api/accounts/{id}/deposit
```

Request Body:

```json
{
  "amount": 500
}
```

### Withdraw Amount

```http
PUT /api/accounts/{id}/withdraw
```

Request Body:

```json
{
  "amount": 200
}
```

### Get All Accounts

```http
GET /api/accounts
```

### Delete Account

```http
DELETE /api/accounts/{id}
```

## Running the Application

Clone the repository:

```bash
git clone https://github.com/your-username/banking-app.git
```

Navigate to the project:

```bash
cd banking-app
```

Run the application:

```bash
./mvnw spring-boot:run
```

or

```bash
mvn spring-boot:run
```

The application will start on:

```text
http://localhost:8080
```

## Testing APIs

Use Postman to test all REST endpoints.

Example:

```http
http://localhost:8080/api/accounts
```

## Learning Outcomes

This project demonstrates:

* Spring Boot REST API Development
* Layered Architecture
* DTO Pattern
* Entity Mapping with JPA
* Repository Pattern
* Service Layer Implementation
* MySQL Integration
* CRUD Operations
* Banking Transactions (Deposit & Withdrawal)

## Future Enhancements

* Account Transfer Feature
* Transaction History
* Exception Handling
* Validation using Bean Validation
* Swagger/OpenAPI Documentation
* Spring Security & JWT Authentication
* Docker Deployment

## Reference

This project is inspired by the Java Guides tutorial:

"Spring Boot Project | Banking Application using Spring Boot, Spring Data JPA (Hibernate), & MySQL"

## Author

Satya Prakash

Java Full Stack Developer passionate about building scalable backend applications using Spring Boot and modern Java technologies.
