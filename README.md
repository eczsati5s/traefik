---
title: File
---

# Traefik & File

The file provider lets you define the dynamic configuration in a file.

## Configuration Examples

```yaml
# Dynamic configuration
tcp:
  routers:
    my-router:
      rule: "HostSNI(`example.com`)"
      service: my-service
      tls: {}

http:
  services:
    my-service:
      loadBalancer:
        servers:
          - url: "http://example.com"
```

## Reference

For the full documentation, see [File Provider](https://doc.traefik.io/traefik/providers/file/).