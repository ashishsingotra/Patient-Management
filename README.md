# Patient Management System

This project is a microservices-based application for managing patient data, billing, and analytics. It is built using Spring Boot and Spring Cloud and utilizes various services for different functionalities.

## Services

The application is divided into the following microservices:

- **API Gateway:** The single entry point for all client requests, routing them to the appropriate service. It also handles cross-cutting concerns like security and logging.
- **Authentication Service:** Manages user authentication and authorization, providing JWT tokens for secure communication between services.
- **Patient Service:** Handles patient-related data, including creating, retrieving, and updating patient records.
- **Billing Service:** Manages billing and payment information for patient services.
- **Analytics Service:** Provides data analytics and reporting features.

## Infrastructure

The project uses the following infrastructure components:

- **Eureka Server:** For service discovery, allowing services to find and communicate with each other dynamically.
- **Spring Cloud Gateway:** The foundation for the API Gateway, providing routing and filtering capabilities.
- **Docker:** For containerizing the services, ensuring consistent environments for development and deployment.

## Getting Started

To get the project up and running, follow these steps:

1. **Prerequisites:**
   - Java 17 or higher
   - Maven 3.6 or higher
   - Docker

2. **Build the project:**
   ```bash
   mvn clean install
   ```

3. **Run the services:**
   - Use Docker Compose to start all the services:
     ```bash
     docker-compose up -d
     ```

## API Endpoints

Each service exposes a set of RESTful endpoints for interaction. Refer to the individual service documentation for detailed API specifications.

### Authentication Service

- `POST /auth/register`: Register a new user.
- `POST /auth/login`: Authenticate a user and receive a JWT token.

### Patient Service

- `GET /patients`: Retrieve a list of all patients.
- `GET /patients/{id}`: Get details of a specific patient.
- `POST /patients`: Create a new patient record.

## Testing

The project includes both unit and integration tests to ensure code quality and correctness.

- **Unit Tests:** Run using Maven:
  ```bash
  mvn test
  ```
- **Integration Tests:** Located in the `integration-tests` module, these tests verify the interaction between different services.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

