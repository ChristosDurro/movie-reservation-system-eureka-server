# Eureka Server

## Overview
The **Eureka Server** is a critical component of the Movie Reservation System, responsible for service discovery. It enables microservices to register themselves and discover other services dynamically, ensuring seamless communication between them.

## Features
- Centralized service registry for microservices.
- Enables dynamic service discovery and load balancing.
- Facilitates fault tolerance by detecting unavailable services.

## Technologies Used
- **Spring Boot** – Core framework for building the microservice.
- **Spring Cloud Netflix Eureka** – Service registry and discovery.

## Service Registration
Once started, microservices within the system register themselves with Eureka Server using their service names. Example registration in `application.properties`:

```properties
spring.application.name=movie-service
eureka.client.service-url.defaultZone=http://localhost:8761/eureka/
```

## Installation & Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/ChristosDurro/movie-reservation-system-eureka-server.git
   ```
2. Navigate to the project folder:
   ```bash
   cd movie-reservation-system-eureka-server
   ```
3. Configure the `application.properties` file:
   ```properties
   spring.application.name=eureka-server
   server.port=8761
   eureka.client.register-with-eureka=false
   eureka.client.fetch-registry=false
   ```
4. Build and run the service:
   ```bash
   mvn spring-boot:run
   ```

---

This service is part of the **Movie Reservation System**, designed to showcase a microservices-based architecture with Spring Boot.

