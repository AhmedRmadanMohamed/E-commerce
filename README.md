<div align="center">

# 🛒 E-Commerce Backend

**A Spring Boot backend foundation for products, categories, carts, orders, reviews, users, brands, and configurable storefront data.**

![Java](https://img.shields.io/badge/Java-17-E76F00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-REST_API-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-Persistence-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-Hibernate-59666C?style=for-the-badge&logo=hibernate&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-Build-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)

</div>

---

## ✨ Overview

This repository is an evolving e-commerce backend built with Java and Spring Boot. It establishes a broad relational domain model and currently exposes storefront configuration and brand-focused endpoints through a layered controller, service, repository, DTO, and mapper design.

## 🧩 Domain Model

The current model includes:

- Products, categories, tags, and brands
- Carts and cart items
- Orders and order status
- Cards and payment-related data structures
- Users, credentials, authorities, and social profiles
- Reviews
- Storefront and application parameters
- E-commerce information and configuration

## 🚀 Implemented API Areas

| Method | Path | Purpose |
|---|---|---|
| `GET` | `/homePage/getDistinctNameParam` | List distinct application-parameter names |
| `GET` | `/homePage/getByParamName` | Retrieve parameters by name |
| `POST` | `/homePage/addParam` | Perform an application-parameter operation |
| `GET` | `/homePage/brands` | List brands |
| `GET` | `/homePage/BrandAndApplicationBarameters` | Retrieve brands with storefront parameters |

The repository also contains a global exception handler and a consistent response wrapper for API results.

## 🧱 Architecture

```text
REST Controller
      │
      ▼
Services ──► DTOs & Mappers
      │
      ▼
Spring Data Repositories
      │
      ▼
MySQL
```

## ⚙️ Getting Started

### Prerequisites

- JDK 17
- Maven or the included Maven Wrapper
- MySQL

### Configure

Provide local database settings in `src/main/resources/application.properties`:

```properties
spring.datasource.url=<your-jdbc-url>
spring.datasource.username=<your-username>
spring.datasource.password=<your-password>
```

Never commit real credentials. Prefer environment variables or environment-specific configuration for shared deployments.

### Run

Windows:

```powershell
.\mvnw.cmd spring-boot:run
```

Linux or macOS:

```bash
./mvnw spring-boot:run
```

### Test

```bash
./mvnw test
```

## 📌 Project Status

The domain model is broader than the current service and controller implementation. The repository should be treated as a backend foundation under active development, not as a complete production e-commerce platform.

## 🗺️ Roadmap

- Implement product, category, cart, order, review, and user use cases.
- Add request validation and transactional boundaries.
- Add authentication and role-based authorization.
- Expand unit and integration test coverage.
- Publish an OpenAPI contract and add automated builds.

---

<div align="center">

An extensible Spring Boot foundation for building a complete e-commerce backend.

</div>
