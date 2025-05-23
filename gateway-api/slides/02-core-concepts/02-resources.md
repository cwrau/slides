```yaml
layout: two-cols-header
layoutClass: gap-4
```

# Gateway API Resources

## Key Resource Types

::left::

<v-click>

### GatewayClass
```yaml
apiVersion: gateway.networking.k8s.io/v1beta1
kind: GatewayClass
metadata:
  name: traefik
spec:
  controllerName: traefik.io/gateway-controller
```

</v-click>

<v-click>

### Gateway
```yaml
apiVersion: gateway.networking.k8s.io/v1beta1
kind: Gateway
metadata:
  name: my-gateway
spec:
  gatewayClassName: traefik
  listeners:
    - name: http
      port: 80
      protocol: HTTP
```

</v-click>

::right::

<v-click>

### HTTPRoute
```yaml
apiVersion: gateway.networking.k8s.io/v1beta1
kind: HTTPRoute
metadata:
  name: http-app-route
spec:
  parentRefs:
    - name: my-gateway
  rules:
    - matches:
      - path:
          type: PathPrefix
          value: /app
      backendRefs:
      - name: app-service
        port: 8080
```

</v-click>
