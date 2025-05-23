```yaml
layout: two-cols-header
layoutClass: gap-4
```

# Gateway API Shortcomings

## Current Limitations

- ### Infrastructure Coordination
  - TLS certificate management
  - Domain name coordination

::left::

- ### Developer Workflow

```yaml {all|6,7|none}{at:1}
apiVersion: gateway.networking.k8s.io/v1
kind: HTTPRoute
metadata:
  name: new-service
spec:
  hostnames:
    - "new-service.example.com" # Needs certificate
```
::right::

- ### Cluster Operator Tasks

```yaml {all|8|5}{at:1}
apiVersion: gateway.networking.k8s.io/v1
kind: Gateway
spec:
  listeners:
    - name: new-service-https # Must be unique per Gateway
      protocol: HTTPS
      # must be set for cert-manager
      hostname: "new-service.example.com"
      tls:
        certificateRefs:
          - name: new-service-tls
```
