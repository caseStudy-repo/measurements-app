[![Case Study](https://img.shields.io/endpoint?url=https://cloud.cypress.io/badge/detailed/vrsv3n/main&style=flat&logo=cypress)](https://cloud.cypress.io/projects/vrsv3n/runs)

# Measurements

This repository contains a case study app for a Master's thesis. The project demonstrates a full-stack implementation with a **Quarkus backend** and a **React frontend**, along with a complete **CI/CD pipeline**.

## Features
The project includes:
- **Quarkus backend**
- **React frontend**
- **CI/CD automation**, including:
  - Build process
  - Unit test automation
  - Quality gate enforcement
  - Functional test automation
  - Containerized deployment to a cloud environment

## Scope (Backend + Frontend + CLI)
The application provides the following functionalities:
- Stores **Products** (id, name, min allowed temperature, max allowed temperature) in a database with **CRUD** operations available via REST endpoints.
- Accepts **Measurements** (product, temperature, measurement type) via REST endpoints.
- Evaluates **measurements** and marks them as **OK** (inside the allowed temperature range) or **NOT OK**.
- Provides a **measurements history** for the last 10 days via a REST endpoint.

## Running the Backend
To run the backend, you can either:
- **Build and run manually**:
  ```sh
  mvn clean package
  java -jar target/your-backend.jar
  ```
- **Use Docker Compose**:
  ```sh
  docker-compose build
  docker-compose up
  ```

After starting the backend, you can access the Swagger UI at:
[http://127.0.0.1:8280/api/v1/swagger-ui/](http://127.0.0.1:8280/api/v1/swagger-ui/)

For more details, check the `_backend_` folder.

## Running the Frontend
To run the frontend, use:
- **Node.js (npm)**:
  ```sh
  npm install
  npm run start
  ```
- **Docker**:
  ```sh
  docker run -d -p 3000:80 <image_name>
  ```

For more details, check the `_frontend_` folder.

---

This case study is an essential part of my **Master’s thesis research**, demonstrating the integration of backend, frontend, and automated deployment for a real-world application.
