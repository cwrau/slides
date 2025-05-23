# Infrastructure Providers

<div class="grid grid-cols-2 gap-4">

<v-clicks>

<v-click>

<div>

## Provider Responsibilities

- VM/Instance provisioning
- Network configuration
- Security group management
- Load balancer setup
- Storage provisioning

</div>

</v-click>

</v-clicks>

<v-clicks>

<v-click>

<div>

## Implementation Requirements

- Must implement provider-specific CRDs
- Handle infrastructure lifecycle
- Provide status updates
- Implement finalizers

</div>

</v-click>

</v-clicks>

</div>

<v-clicks>

## Example: OpenStack Provider

```yaml
apiVersion: infrastructure.cluster.x-k8s.io/v1beta1
kind: OpenstackMachineTemplate
spec:
  template:
    spec:
      flavor: standard.2.1905
      identityRef:
        name: openstack-credentials
        cloudName: openstack
```

</v-clicks>