# INT363: CLOUD MICROSERVICES
# Practical 8 — Implementing an API Gateway

## Aim

To implement an API Gateway using Nginx and Docker Compose for routing requests to multiple backend microservices.

## Architecture

Client → API Gateway → User Service
                     → Order Service

## Project Structure

```text
api-gateway-demo/
├── docker-compose.yml
├── nginx/
│   └── default.conf
├── userservice/
│   ├── Dockerfile
│   ├── package.json
│   └── server.js
└── orderservice/
    ├── Dockerfile
    ├── package.json
    └── server.js
