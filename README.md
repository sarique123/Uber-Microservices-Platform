# 🚗 Uber Ride Booking Platform (Microservices Architecture)

This project is a **backend system for an Uber-like ride booking platform**, designed with a scalable **Microservices Architecture** using **Spring Boot**, **Spring Cloud**, and distributed technologies.

---

## 🗂️ Microservices Overview

| Microservice      | Description                                                                                  | Repository Link                                                                 |
|-------------------|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| **AuthService**    | Manages user registration, login, and token-based authentication using JWT & Spring Security | [GitHub](https://github.com/sarique123/UberProject-AuthService)                 |
| **BookingService** | Handles ride booking lifecycle: request, assignment, and completion                          | [GitHub](https://github.com/sarique123/UberBookingService)                      |
| **ReviewService**  | Manages user feedback and ride ratings                                                       | [GitHub](https://github.com/sarique123/UberProject-ReviewService)               |
| **LocationService**| Manages driver geolocation data using Redis GeoSpatial                                        | [GitHub](https://github.com/sarique123/UberProject-LocationService)             |
| **SocketServer**   | Enables real-time rider-driver communication via WebSockets (STOMP Protocol)                  | [GitHub](https://github.com/sarique123/SocketServer-With-Spring-Boot)           |
| **EntityService**  | Defines shared data models/entities used across services for consistency                     | [GitHub](https://github.com/sarique123/UberProject-EntityService)               |
| **EurekaServer**   | Implements service discovery and dynamic service registration using Netflix Eureka            | [GitHub](https://github.com/sarique123/Uber-ServiceDiscovery-EurekaServer)      |

---

## 🏗️ Architecture Overview
A scalable microservices architecture where services communicate via REST APIs and WebSockets.
Service Discovery is managed by Eureka, and Redis GeoSpatial is used for real-time location queries.

*(Optional: Add architecture diagram here if available)*

---

## 🚀 Technologies Used
- Spring Boot, Spring Cloud (Netflix Eureka)
- JWT Authentication (Spring Security + BCrypt)
- Redis GeoSpatial for location tracking
- MySQL for persistent storage
- WebSocket with STOMP Protocol for real-time updates

---

## 📦 How to Run (Optional Section)
```bash
# Clone individual services:
git clone https://github.com/sarique123/UberProject-AuthService
git clone https://github.com/sarique123/UberBookingService
git clone https://github.com/sarique123/UberProject-ReviewService
git clone https://github.com/sarique123/UberProject-LocationService
git clone https://github.com/sarique123/SocketServer-With-Spring-Boot
git clone https://github.com/sarique123/UberProject-EntityService
git clone https://github.com/sarique123/Uber-ServiceDiscovery-EurekaServer

# Start Eureka Server first
cd Uber-ServiceDiscovery-EurekaServer
mvn spring-boot:run

# Then start other services:
cd UberProject-AuthService
mvn spring-boot:run

cd UberBookingService
mvn spring-boot:run

# ...repeat for all services
