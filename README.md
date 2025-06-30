# Employee Transport & Food Management System

This is a Spring Boot-based RESTful API that manages employees and their associated resources, such as food, private transport, and public transport.

## 📦 Features

- CRUD operations for:
  - Employees
  - Food items associated with an employee
  - Private Transport associated with an employee
  - Public Transport records
- Validation of ownership (e.g., verifying if a `Food` or `Transport` belongs to an `Employee`)
- Custom exception handling
- DTO-based clean mapping using `Mapper` utility

---

## 🛠️ Tech Stack

- Java 17+
- Spring Boot
- Spring Data JPA
- Hibernate
- PostgreSQL / MySQL (configurable)
- Lombok
- MapStruct (optional for Mapper)
- Swagger/OpenAPI (for API docs)


---

## ⚙️ API Endpoints (Examples)

### 🔹 Employee
- `GET /api/employees/{id}` – Get employee by ID
- `POST /api/employees` – Create employee

### 🔹 Food
- `GET /api/employees/{employeeId}/food/{foodId}` – Get a food item belonging to an employee
- `POST /api/employees/{employeeId}/food` – Add food to an employee

### 🔹 Private Transport
- `GET /api/employees/{employeeId}/private-transport/{transportId}` – Get a Private Transport belonging to an employee
- `POST /api/employees/{employeeId}/private-transport`– Add Private Transport to Employee

### 🔹 Public Transport
- `GET /api/employee/{employeeId}/public-transport/{publicTransportId}`– Get a Public Transport belonging to an employee
- `POST /api/employee/{employeeId}/public-transport` – Add Public Transport to Employee

---

## ❗ Exception Handling

- `ResourceNotFoundException` for missing or unauthorized resources
- General `RuntimeException` for ownership mismatch

---

## 🚀 Running the Application
Use Maven Wrapper or your IDE:

```bash
./mvnw spring-boot:run
```
The app will be available at: http://localhost:8080

Swagger UI (if enabled) at: http://localhost:8080/swagger-ui/index.html

## 🚧 Future Enhancements
 - Add authentication/authorization (e.g., JWT)
 - Pagination & sorting support for list APIs
 - Dockerize the application
 - Add caching for commonly accessed data
 - Extend API documentation with Swagger/OpenAPI 3.0

 ### 🤝 Contributing
- Contributions are welcome! Please fork the repository and open a pull request or file an issue.
