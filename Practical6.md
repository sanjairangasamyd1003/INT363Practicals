# INT363: CLOUD MICROSERVICES
# Practical 6 — Managing Application Secrets

## Aim
To securely manage database passwords using Docker secrets and file-based secret injection.

## Problem

Hardcoding passwords in source code or Docker Compose files is unsafe.

Unsafe:

```yaml
environment:
  - DB_PASSWORD=rootpassword
