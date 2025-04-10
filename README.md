# Quiz App - Spring Boot Microservice Architecture

This is a **Quiz Application** built using **Spring Boot**, designed with a modular **microservices architecture**. It includes services for managing questions and quizzes, and demonstrates core concepts such as service discovery, API Gateway routing, and client-side load balancing.

---

## Architecture Overview

- **Question Service** – Handles all operations related to quiz questions.
- **Quiz Service** – Manages quizzes, quiz creation, and result calculation.
- **API Gateway** – Acts as the single entry point to the system, routing requests to respective services.
- **Service Discovery (Eureka)** – Registers services and enables dynamic lookup.
- **Load Balancer** – Distributes traffic among service instances to ensure reliability and scalability.

---

## Technologies Used

- Java 17+
- Spring Boot
- Spring Web, Spring Data JPA
- Spring Cloud Gateway
- Spring Cloud Eureka
- PostgreSQL
- Maven

---

## Key Features

- RESTful APIs to create and manage quizzes
- Random question selection based on category
- Submit answers and calculate scores
- Microservices registered with Eureka
- Routing through Spring Cloud Gateway
- Load balancing enabled for scalable service calls

---

## API Gateway and Load Balancing

### API Gateway

All client requests pass through **Spring Cloud Gateway**, which forwards the request to appropriate backend services. This simplifies the client-side logic and centralizes authentication, logging, and routing.

### Load Balancing

With **Spring Cloud LoadBalancer**, the system distributes requests across multiple instances of a service registered with **Eureka**. This improves performance and prevents overload on a single service instance.

---

## Running the Application

1. Clone the repository:

```bash
git clone https://github.com/renuvelhal/Quiz-App-SpringBoot-Microservice.git
```

2. Start Eureka Server

3. Start Question and Quiz Services

4. Start API Gateway

5. Access API endpoints via:

```
http://localhost:8080/question-service/question/all
http://localhost:8080/quiz-service/quiz/create
```

---

## Project Structure

```
quiz-app/
├── api-gateway/
├── quiz-service/
├── question-service/
└── eureka-server/
```
