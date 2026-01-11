---
title: Docker Best Practices
description: Production-ready Docker containerization guidelines
globs: ["**/Dockerfile*", "**/docker-compose*.yml"]
source: https://docs.docker.com/develop/dev-best-practices/
references:
  - Multi-Stage Builds: https://12footsteps.medium.com/multistage-docker-builds-beyond-smaller-images-a-security-imperative-cd97ba51a7e8
  - Google Cloud Containerization: https://cloud.google.com/architecture/container-structure/docker-best-practices
---

# DOCKER PRODUCTION PATTERNS

## Layer Optimization
- **Multi-Stage Builds**: Separate build environment from runtime to reduce image size and attack surface.
- **Layer Caching**: Order `COPY` and `RUN` instructions to maximize caching of dependencies.
- **Minimal Base**: Prefer `alpine`, `debian-slim`, or `distroless` images.

## Security
- **Non-Root**: Never run containers as root. Create a dedicated user.
- **Secrets**: Never hardcode secrets in `Dockerfile` or `ENV`. Use volume-mounted secrets or environment variables at runtime.

## Health Checks
- **HEALTHCHECK**: Implement health checks in `Dockerfile` or `docker-compose.yml`.
- **Readiness vs Liveness**: Distinguish between process running and service ready to handle traffic.
