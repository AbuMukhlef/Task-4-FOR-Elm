# Employee Management System V4

## Project Description
The Employee Management System is a REST API application built with Spring Boot and JPA/Hibernate for managing employee data. This system allows users to perform CRUD operations (Create, Read, Update, Delete) on employee records.

## Version 4 Updates
In this fourth version of the Employee Management System, the following enhancements have been implemented:

- **ORM Integration**: Replaced direct database operations with JPA/Hibernate ORM for more efficient data management
- **Spring Boot Framework**: Upgraded to use Spring Boot 3.4.3 for improved performance and security
- **EntityManager**: Implemented EntityManager for database operations instead of direct JDBC
- **Repository Pattern**: Enhanced the repository layer with proper separation of concerns
- **PostgreSQL Support**: Added PostgreSQL database support for robust data storage
- **RESTful API Design**: Improved API design with proper HTTP status codes and response handling
- **Transaction Management**: Added transaction support for database operations

## Technical Stack
- Java 23
- Spring Boot 3.4.3
- Spring Data JPA
- Hibernate ORM
- PostgreSQL Database
- RESTful API

## Testing with Postman

### Setup
1. Ensure PostgreSQL is running and properly configured in your application.properties
2. Start the Spring Boot application
3. Open Postman

### Get All Employees
- Method: GET
- URL: http://localhost:8080/absher/api/v4/employees

### Get Employee by ID
- Method: GET
- URL: http://localhost:8080/absher/api/v4/employees/1

### Create New Employee
- Method: POST
- URL: http://localhost:8080/absher/api/v4/employees
- Headers: Content-Type: application/json
- Body:
```json
{
  "name": "John Doe",
  "gender": "Male",
  "dob": "1990-01-01",
  "phoneNumber": "1234567890",
  "hobbies": ["Reading", "Hiking", "Coding"]
}
```

### Update Employee
- Method: PUT
- URL: http://localhost:8080/absher/api/v4/employees/1
- Headers: Content-Type: application/json
- Body:
```json
{
  "name": "John Doe Updated",
  "gender": "Male",
  "dob": "1990-01-01",
  "phoneNumber": "9876543210",
  "hobbies": ["Reading", "Swimming", "Coding"]
}
```

### Delete Employee
- Method: DELETE
- URL: http://localhost:8080/absher/api/v4/employees/1

## Data Model
The Employee entity includes the following fields:
- id (int): Unique identifier
- name (String): Employee name
- gender (String): Employee gender
- dob (String): Date of birth
- phoneNumber (String): Contact number
- hobbies (List<String>): Employee hobbies

## Notes
- Make sure to configure your PostgreSQL connection in the application.properties file
- The API returns appropriate HTTP status codes: 200 OK, 201 Created, 204 No Content, 404 Not Found
- Error handling is implemented to provide meaningful error messages