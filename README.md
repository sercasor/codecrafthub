CodeCraftHub Learning Management System

A simple REST API for tracking your learning goals and courses built with Java and Spring Boot.
Features

    Complete CRUD operations for course management
    JSON file-based storage (no database needed)
    RESTful API design
    Proper error handling

Installation

    Clone or download the project
    Install Java JDK 17 or higher
    Install Maven (if not already installed)

Running the Application

Navigate to the project directory and run:
bash

mvn spring-boot:run

Or build and run the JAR:
bash

mvn clean package
java -jar target/codecrafthub-1.0.0.jar

The API will be available at http://localhost:8080
API Endpoints
1. Add a Course

POST /api/courses

Request body:
json

{
"name": "Python Basics",
"description": "Learn Python fundamentals",
"target_date": "2025-12-31",
"status": "Not Started"
}

2. Get All Courses

GET /api/courses
3. Get Specific Course

GET /api/courses/{id}
4. Update Course

PUT /api/courses/{id}

Request body (all fields optional):
json

{
"status": "In Progress"
}

5. Delete Course

DELETE /api/courses/{id}
Testing

Use the provided curl commands or import the Postman collection to test all endpoints.
Troubleshooting

Problem: "JAVA_HOME not set"
Solution: Set JAVA_HOME environment variable to your JDK installation path

Problem: "Port already in use"
Solution: Stop other applications using port 8080 or change the port in application.properties
Project Structure
plaintext

codecrafthub/
├── src/
│   └── main/
│       ├── java/
│       │   └── com/codecrafthub/
│       │       ├── CodeCraftHubApplication.java
│       │       ├── controller/
│       │       ├── model/
│       │       └── service/
│       └── resources/
├── courses.json     # Data storage (auto-created)
└── pom.xml         # Dependencies
