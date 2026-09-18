# INT363: CLOUD MICROSERVICES
# Practical 7 — Scaling Microservices for High Traffic

## Aim
To demonstrate horizontal scaling of backend microservices using Docker Compose.

## Scenario

An online learning platform receives a sudden increase in traffic during exams.

If only one backend container is running, it may become overloaded.

Problems include:
- Slow response time
- Timeout errors
- Poor user experience
- Service unavailability
- Increased server pressure

## Scaling

Scaling means increasing application capacity so it can handle more users or work.

### Vertical Scaling
Increasing CPU, memory, or other resources of one machine or container.

### Horizontal Scaling
Increasing the number of service instances.

Example:

```text
One backend container
        ↓
Three backend containers
