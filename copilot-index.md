# copilot-index.md

## Overview
This project is a Spring Boot Java 21+ API prototype for Cognito-based authentication. It demonstrates clean architecture, DTO usage, and structured logging, and is ready for secure and public endpoints.

## Tech Stack
- Java 21
- Spring Boot
- SLF4J + Logback (logging)
- JUnit 5, Mockito, AssertJ (testing)
- Flyway (DB versioning, planned)

## Entry Points
- Main: `CognitoauthApplication.java`
- API: `/api/public/hello`, `/api/secure/hello`

## Modules/Folders
- `controller/` – REST API endpoints (public and secure)
- `service/` – Business logic
- `dto/` – Data Transfer Objects for API communication
- `resources/` – Configuration, static assets
- `test/` – Unit and integration tests

## Key Relationships & End-to-End Flows
- Controller → Service → (Repository planned for DB)
- DTOs used for all API responses
- Logging includes userId, requestId, operation

## Critical APIs & Integration Points
- `GET /api/public/hello` – Unsecured hello endpoint
- `GET /api/secure/hello` – Secured hello endpoint (auth to be added)

## Naming Conventions
- Controllers: `*Controller.java`
- Services: `*Service.java`
- DTOs: `*Dto.java`
- Tests: `*Tests.java`

## Test Coverage Map
- Service and controller tests planned (see `/test`)

## Auth/Security Approach
- Public endpoints require no auth
- Secure endpoints will require Cognito JWT validation (to be implemented)

## Update Policy
- Update this index after any significant architectural or API change.
