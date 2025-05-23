# Bootstrap Providers

<div class="grid grid-cols-2 gap-4">

<v-clicks>

<v-click>

<div>

## Kubeadm Bootstrap Provider

- Default bootstrap provider
- Generates kubeadm configurations
- Handles node initialization
- Manages certificates and tokens

</div>

</v-click>

</v-clicks>

<v-clicks>

<v-click>

<div>

## Custom Bootstrap Providers

- Can implement alternative bootstrap methods
- Must generate valid node bootstrap data
- Responsible for initial node setup
- Can integrate with existing tools

</div>

</v-click>

</v-clicks>

</div>

<v-clicks>

## Example Configuration

```yaml
apiVersion: bootstrap.cluster.x-k8s.io/v1beta1
kind: KubeadmConfigTemplate
spec:
  template:
    spec:
      joinConfiguration:
        nodeRegistration:
          kubeletExtraArgs:
            cloud-provider: external
```

</v-clicks>