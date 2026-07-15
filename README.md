# 🛍️ Product Management REST API

A RESTful backend application built using **Spring Boot**, **Spring Data JPA**, and **MySQL** to perform CRUD (Create, Read, Update, Delete) operations on product data. This project demonstrates REST API development, database integration, validation, and exception handling.

---

## 📌 Features

- ➕ Add a new product
- 📋 View all products
- 🔍 View a product by ID
- ✏️ Update product details
- ❌ Delete a product
- ✅ Input validation
- ⚠️ Global exception handling
- 🗄️ MySQL database integration
- 📡 RESTful API design
- 🧪 Tested using Postman

---

## 🛠️ Technologies Used

- Java 17
- Spring Boot
- Spring Data JPA (Hibernate)
- MySQL
- Maven
- Postman
- Spring Validation

---

## 📂 Project Structure

```text
ProductManagement
│
├── src/main/java/com/example/demo
│   ├── controller
│   │      ProductController.java
│   │
│   ├── service
│   │      ProductService.java
│   │
│   ├── repository
│   │      ProductRepository.java
│   │
│   ├── model
│   │      Product.java
│   │
│   ├── exception
│   │      ResourceNotFoundException.java
│   │      GlobalExceptionHandler.java
│   │
│   └── ProductManagementApplication.java
│
├── src/main/resources
│      application.properties
│
└── pom.xml
```

---

## 🗃️ Database

**Database Name**

```sql
product
```

Spring Boot automatically creates the **products** table using Hibernate.

---

## 🔗 REST API Endpoints

| Method       |      Endpoint      |     Description       |
|--------------|--------------------|-----------------------|
| POST         | `/api/products`    | Add a new product     |
| GET          | `/api/products`    | Get all products      |
| GET          | `/api/products/{id}| Get product by ID     |
| PUT          | `/api/products/{id}| Update product        |
| DELETE       | `/api/products/{id}| Delete product        |

---

## 📥 Sample Request (POST)

**POST**

```http
POST /api/products
```

```json
{
    "productName": "Laptop",
    "category": "Electronics",
    "brand": "Dell",
    "price": 65000,
    "quantity": 10,
    "description": "Dell Inspiron 15"
}
```

---

## 📤 Sample Response

```json
{
    "id": 1,
    "productName": "Laptop",
    "category": "Electronics",
    "brand": "Dell",
    "price": 65000.0,
    "quantity": 10,
    "description": "Dell Inspiron 15"
}
```

---

## ✅ HTTP Status Codes
 
| Status Code     |        Description           |
|---------------- |----------------------------- |
| 200 OK          |       Request Successful     |
| 201 Created     | Product Created Successfully |
| 400 Bad Request |       Validation Failed      |
| 404 Not Found   |       Product Not Found      |

---

## ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/sonypasupuleti31/Product-Management-REST-API-SpringBoot
```

### 2. Open the Project

Import the project into **Spring Tool Suite (STS)** or **IntelliJ IDEA**.

### 3. Create MySQL Database

```sql
CREATE DATABASE product;
```

### 4. Configure Database

Update **application.properties** with your MySQL username and password.

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/product
spring.datasource.username=root
spring.datasource.password=your_password
```

### 5. Run the Application

Run:

```
ProductManagementApplication.java
```

The application starts on:

```
http://localhost:8080
```

---

## 🧪 Testing

All endpoints were tested successfully using **Postman**.

Example URL:

```
http://localhost:8080/api/products
```

---

## 📖 Learning Outcomes

Through this project, I learned:

- Building REST APIs using Spring Boot
- Implementing CRUD operations
- Integrating Spring Boot with MySQL
- Using Spring Data JPA (Hibernate)
- Request validation using Jakarta Validation
- Exception handling with `@RestControllerAdvice`
- Testing REST APIs using Postman
- Returning proper HTTP status codes
- Following layered architecture (Controller → Service → Repository)

---

## 👩‍💻 Author

**Sony Pasupuleti**

Aspiring Java Full Stack Developer | Spring Boot | MySQL | REST API Development

---

## ⭐ Future Enhancements

- Product search by name
- Pagination and sorting
- Swagger/OpenAPI documentation
- Spring Security with JWT Authentication
- Docker containerization
- Unit testing with JUnit & Mockito
- Role-based access control

---
