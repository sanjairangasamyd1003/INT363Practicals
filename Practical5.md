# INT363: CLOUD MICROSERVICES
# Practical 5 — Automatic Startup of Dependent Services

## Aim
To configure Docker Compose so that the backend service starts after the database service and only when the database is ready.

## Scenario

The backend application depends on a MySQL database.

```text
User → Backend → Database
