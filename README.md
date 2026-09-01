# Traefik

[![Build Status](https://github.com/traefik/traefik/workflows/Main/badge.svg)](https://github.com/traefik/traefik/actions)
[![Go Report Card](https://goreportcard.com/badge/github.com/traefik/traefik)](https://goreportcard.com/report/github.com/traefik/traefik)
[![Documentation](https://img.shields.io/badge/docs-v3.0-blue.svg)](https://doc.traefik.io/traefik/)

Traefik (pronounced *traffic*) is a modern HTTP reverse proxy and load balancer that makes deploying microservices easy.
Traefik integrates with your existing infrastructure components (Docker, Swarm, Kubernetes, Marathon, Consul, Etcd, Rancher, Amazon ECS, ...) and configures itself automatically and dynamically.

## Quick Start

Run Traefik using Docker:

```bash
docker run -d -p 8080:8080 -p 80:80 \
  -v /var/run/docker.sock:/var/run/docker.sock:ro \
  traefik:v3.0 --api.insecure=true --providers.docker
```

Access the dashboard at `http://localhost:8080/dashboard/`.

## Features

- Continuously updates its configuration (No restarts required)
- Supports multiple providers: Docker, Kubernetes, Consul, Etcd, etc.
- Automatic HTTPS via Let's Encrypt (ACME support)
- Webhooks and metrics (Prometheus, Datadog, StatsD)
- HTTP/2 and gRPC support

## Documentation

Comprehensive documentation is available at [doc.traefik.io/traefik/](https://doc.traefik.io/traefik/).

## License

Traefik is licensed under the [MIT License](LICENSE).