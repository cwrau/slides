---
layout: two-cols-header
---

# Reconciliation Process

::left::

```mermaid
sequenceDiagram
    participant User
    participant API Server
    participant Controller
    participant Infrastructure
    
    User->>API Server: Apply YAML
    API Server->>Controller: Watch Event
    Controller->>Infrastructure: Reconcile
    Infrastructure-->>Controller: Status Update
    Controller-->>API Server: Update Status
    API Server-->>User: Updated Resource
```

::right::

<v-clicks>

1. **Watch Phase**
   - Controllers watch Custom Resources
   - Events trigger reconciliation
   - Webhooks validate changes

2. **Reconciliation Phase**
   - Compare desired vs actual state
   - Plan necessary changes
   - Execute in order

</v-clicks>