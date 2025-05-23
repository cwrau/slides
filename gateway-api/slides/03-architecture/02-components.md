```yaml
layout: two-cols-header
layoutClass: gap-4
```

# Gateway API Components

::left::

<v-click>

### Gateway Controllers
- Traefik Gateway Controller
- Cilium Gateway Controller
- Istio Gateway Controller
- Contour Gateway Controller

</v-click>

<v-click>

### Route Controllers
- HTTP Route Controller
- GRPC Route Controller
- TCP Route Controller
- TLS Route Controller

</v-click>

::right::

<v-click>

### Policy Controllers
- BackendTLSPolicy
- ClientCertificatePolicy
- RateLimitPolicy

</v-click>

<v-click>

### Component Interaction
```mermaid {scale: 0.4}
sequenceDiagram
    participant IP as Infrastructure Provider
    participant CO as Cluster Operator
    participant D as Developer
    participant C as Controller
    participant I as Infrastructure

    IP->>C: Create GatewayClass
    CO->>C: Create Gateway
    D->>C: Create Route
    C->>I: Configure Infrastructure
    I-->>C: Status Update
    C-->>IP: Update GatewayClass Status
    C-->>CO: Update Gateway Status
    C-->>D: Update Route Status
```
</v-click>
