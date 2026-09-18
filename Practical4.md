# INT363: CLOUD MICROSERVICES
# Practical 4 — Migrating from Monolithic to Microservices

## Aim
To convert a monolithic application into a microservices architecture using Docker Compose.

## Architecture

User → Frontend → Backend → Database

## Project Structure

```text
ecommerce-microservices/
├── docker-compose.yml
├── frontend/
│   ├── Dockerfile
│   └── index.html
└── backend/
    ├── Dockerfile
    ├── package.json
    └── server.js
