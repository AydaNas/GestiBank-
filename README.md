# GestiBank

Banking management web application built with an **Angular** frontend and a **Spring Boot** REST backend secured with **JWT**.

## Features

- JWT authentication and role-based access (Spring Security)
- Back office dashboard for administrators
- Client dashboard
- News (Actualités) management with full CRUD etc 

## Tech stack

| Layer    | Technologies                                  |
|----------|-----------------------------------------------|
| Frontend | Angular, TypeScript, SCSS                     |
| Backend  | Java, Spring Boot, Spring Security, Maven     |
| Database | <MySQL / PostgreSQL / H2>                     |
| DevOps   | Docker, Docker Compose, Jenkins (CI pipeline) |

## Project structure

GestiBank/
├── backend/    # Spring Boot REST API (Dockerfile, Jenkinsfile, docker-compose.yml)
└── frontend/   # Angular application

## Getting started

### Prerequisites

- Java 17+ (match your `pom.xml`), Node.js 18+ and npm
- <your database> running locally, or Docker

### 1. Backend

The JWT signing key is not stored in the repo, so set it as an environment variable:

bash
export JWT_SECRET=$(openssl rand -base64 64 | tr -d '\n')
cd backend
./mvnw spring-boot:run

Configure your database in `backend/src/main/resources/application.properties` (URL, username, password). The API runs on `http://localhost:8080` by default.

### 2. Frontend

bash
cd frontend
npm install
ng serve

Open `http://localhost:4200`.

### Run with Docker
bash
cd backend
export JWT_SECRET=$(openssl ra
nd -base64 64 | tr -d '\n')
docker compose up --build

## Roadmap / Future developments

### Frontend (Angular)
- [ ] Responsive design for mobile and tablet
- [ ] Charts for account balances and spending (Chart.js or ngx-charts)
- [ ] Multi-language support (French / English) with `ngx-translate`
- [ ] Dark mode
- [ ] Form validation improvements and better error messages
- [ ] Unit tests (Jasmine/Karma) and end-to-end tests (Cypress)

### Backend (Spring Boot)
- [ ] Refresh tokens and token revocation for JWT
- [ ] Role and permission management (admin, advisor, client)
- [ ] Transaction history with pagination and filtering
- [ ] API documentation with Swagger / OpenAPI
- [ ] Unit and integration tests (JUnit, Mockito, Testcontainers)
- [ ] Email notifications for transactions
- [ ] Database migrations with Flyway

### DevOps
- [ ] Complete the Jenkins CI/CD pipeline (build, test, Docker image push)
- [ ] Deploy to a cloud provider


## Author

**Aydan** — Master's student in Computer Science (Cloud and Data Infrastructure Computing), Université Grenoble Alpes.
[GitHub](https://github.com/AydaNas)
