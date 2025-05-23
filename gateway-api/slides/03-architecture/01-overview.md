# Gateway API Architecture

## High-Level Overview

```mermaid {scale: 0.8}
graph TD
    A[Gateway API Resources] --> B[Gateway Controllers]
    B --> C[Infrastructure]
    D[Route Resources] --> B
    E[Service Resources] --> B
    B --> F[Load Balancers]
    B --> G[Proxies]
    B --> H[Service Mesh]
```

<style>
.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
  margin-top: 1rem;
}
</style>

<div class="grid-container">

<div>
<v-click>

### Resource Layer
- Kubernetes Custom Resources
- Declarative configuration
- Role-based access control

</v-click>
</div>

<div>
<v-click>

### Controller Layer
- Multiple implementations
- Infrastructure specific
- Policy enforcement

</v-click>
</div>

<div>
<v-click>

### Infrastructure Layer
- Load balancers
- Proxies
- Service mesh components

</v-click>
</div>

</div>