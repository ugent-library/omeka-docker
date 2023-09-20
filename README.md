# Omeka Docker

A simple bare-bones docker based development environment for Omeka.

## Setup

First, create a Docker image with a tuned PHP docker container:

```
docker build -t omeka/php:8.1.17 .
```

Then, point / map the docker volumes in `docker-compose.yml` to your local Omeka root path.

Finally, start the environment with Docker Compose:

```
docker compose up -d
```

Navigate to `omeka.box` to see your Omeka instance.

## Configuration

### php

Refer to `Dockerfile` to see the environment variables you can override in `docker-compose.yml`.

### Caddy

This setup uses Caddy as a webserver. Refer to the `docker-config/caddy/Caddyfile` for tuning.

