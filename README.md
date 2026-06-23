---
title: Customer Management API
sdk: docker
app_port: 7860
colorFrom: blue
colorTo: green
---

# Customer Management API

A simple FastAPI service that provides user registration, login with JWT, and CRUD operations for a customer database.  
The application runs inside a Docker container on Hugging Face Spaces and listens on **0.0.0.0:7860**.

## Features

- **User registration** (`/register`) and **login** (`/token`) with password hashing.
- JWT‑based authentication for protected endpoints.
- SQLite database (`customers.db`) automatically created on first run.
- CRUD endpoints for customers:
  - `POST /customers` – create a new customer
  - `GET /customers` – list all customers
  - `GET /customers/{id}` – retrieve a single customer
  - `PUT /customers/{id}` – update a customer
  - `DELETE /customers/{id}` – delete a customer

## Environment Variables

| Variable    | Description                                 | Default |
|------------|---------------------------------------------|---------|
| `SECRET_KEY` | Secret used to sign JWT tokens.            | `change-me` (should be overridden) |

## Running locally