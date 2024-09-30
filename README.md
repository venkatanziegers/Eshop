# E-Commerce Project Overview

## Project Overview
This repository implements an e-commerce microservices project using .NET tools, focusing on **Catalog, Basket, Discount,** and **Ordering** microservices. It employs both **NoSQL (Redis)** and **Relational databases (PostgreSQL, SQL Server)**, communicating through **RabbitMQ** for event-driven architecture, and utilizes **YARP API Gateway** for routing.

## Features Implemented

### Catalog Microservice
- Built using **ASP.NET Core Minimal APIs** and **.NET 8** features.
- Implemented **Vertical Slice Architecture** and **CQRS** using **MediatR**.
- Utilized **Marten** for document database management on **PostgreSQL**.

### Basket Microservice
- Developed an **ASP.NET 8 Web API** following REST principles.
- Used **Redis** for distributed caching.
- Integrated with **Discount gRPC Service** for price calculations.

### Discount Microservice
- Created a high-performance **gRPC server**.
- Used **Entity Framework Core** with **SQLite** for data access.

### Ordering Microservice
- Implemented **DDD, CQRS,** and **Clean Architecture**.
- Configured to consume events from **RabbitMQ** for order processing.

### YARP API Gateway
- Developed API gateway for routing and managing requests to microservices.
- Implemented rate limiting for API usage.

## Running the Project

### Prerequisites
- **Visual Studio 2022**
- **.NET Core 8** or later
- **Docker Desktop**

### Steps to Run
1. Clone the repository.
2. Configure Docker settings (minimum memory: **4 GB**, CPU: **2**).
3. Navigate to the root directory of the solution and run:
   ```bash
   docker-compose -f docker-compose.yml -f docker-compose.override.yml up -d
