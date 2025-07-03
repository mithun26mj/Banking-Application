# Simple Banking Application

This is a Spring Boot-based RESTful API project for a simple Banking Application. It allows you to create accounts, view account details, and perform deposit and withdrawal operations.

## Technologies Used
- Java 17
- Spring Boot
- Spring Data JPA (Hibernate)
- MySQL Database
- Lombok
- Maven

## Features
- Create a new bank account
- Retrieve account details by ID
- Deposit money into an account
- Withdraw money from an account

## Setup Instructions

### 1. Clone or Download the Project

```
git clone https://github.com/your-username/banking-app.git
cd banking-app
```

### 2. MySQL Configuration

Create a database in MySQL:

```sql
CREATE DATABASE banking_app;
```

Update the database configuration in `src/main/resources/application.properties`:

```
spring.datasource.url=jdbc:mysql://localhost:3306/banking_app
spring.datasource.username=root
spring.datasource.password=Mysql@123
spring.jpa.hibernate.ddl-auto=update
```

### 3. Build and Run the Project

You can build and run the project using your IDE or the command line:

```
mvn spring-boot:run
```

### 4. Test Endpoints

Use tools like Postman or curl to test the following endpoints:

- **Create Account**  
  `POST /api/accounts`  
  Body:
  ```json
  {
      "accountHolderName": "Ramesh",
      "balance": 1000.00
  }
  ```

- **Get Account by ID**  
  `GET /api/accounts/{id}`

- **Deposit Money**  
  `POST /api/accounts/{id}/deposit`  
  Body:
  ```json
  {
      "amount": 200.00
  }
  ```

- **Withdraw Money**  
  `POST /api/accounts/{id}/withdraw`  
  Body:
  ```json
  {
      "amount": 150.00
  }
  ```

## License

This project is licensed under the MIT License.
