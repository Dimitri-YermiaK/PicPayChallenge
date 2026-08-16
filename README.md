# PicPay Backend Challenge

REST API for financial transfers between users, built with Java and Spring Boot.

## About the Project

This project is a solution to the [PicPay Junior Backend Challenge](https://github.com/PicPay/picpay-desafio-backend), developed with Java and Spring Boot.

The main goal is to implement a financial transfer system between users, including balance validation, external authorization, and transaction notifications.

## Table of Contents

- [Architecture](#architecture)
- [Project Structure](#project-structure)
- [Technologies](#technologies)
- [How to Run](#how-to-run)
- [API Endpoint](#api-endpoint)

## Architecture

The project follows a layered architecture with clear separation of responsibilities:

- **Controller:** Exposes the REST endpoints and handles incoming HTTP requests.
- **Service:** Contains the core business logic, including transfer validation, authorization, and notification.
- **Repository:** Responsible for data persistence and database access.
- **Domain:** Defines the core entities (User, Transaction) and their business rules.

## Project Structure

```
src/main/java/
├── controller/          # REST endpoints
├── service/             # Business logic and rules
├── repository/          # Data access layer
├── domain/              # Core entities (User, Transaction)
└── infra/               # External service integrations
```

## Technologies

- **Language:** Java
- **Framework:** Spring Boot / Spring Web / Spring Data JPA
- **Database:** H2 (in-memory)
- **Dependency Management:** Maven
- **Additional:** Lombok

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/Dimitri-YermiaK/PicPayChallenge.git
```

2. Navigate to the project directory:

```bash
cd PicPayChallenge
```

3. Run the application with Maven:

```bash
./mvnw spring-boot:run
```

On Windows:

```bash
mvnw.cmd spring-boot:run
```

The API will be available at:

```
http://localhost:8080
```

## API Endpoint

### Create Transfer

```
POST /transfer
```

Request body:

```json
{
  "value": 100.00,
  "payer": 1,
  "payee": 2
}
```

Successful response:

```
200 OK
```
