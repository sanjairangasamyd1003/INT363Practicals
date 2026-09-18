# INT363: CLOUD MICROSERVICES
# Practical 3 — Docker Compose

## Aim
To define, configure, and run multiple Docker containers as a single application using Docker Compose.

## Important Commands

```bash
docker compose up
docker compose up -d
docker compose stop
docker compose down
docker compose ps
docker compose logs
docker compose logs backend
```

## Docker vs Docker Compose

| Docker | Docker Compose |
|---|---|
| Manages containers and images | Manages multiple related containers |
| docker run | docker compose up |
| Individual container operations | Multi-container application stacks |

## Key Points
1. Docker Compose is designed for multi-container applications.
2. Services are defined in a YAML configuration file.
3. docker compose up starts the defined services.
4. docker compose up -d starts services in detached mode.
5. docker compose ps checks service status.
6. docker compose logs helps troubleshoot services.
7. docker compose stop stops services.
8. docker compose down stops and removes services and network.
