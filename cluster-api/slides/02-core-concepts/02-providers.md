# Core Components

<div class="grid grid-cols-2 gap-4">
<div>

## Provider Types

<v-clicks>

- **Infrastructure Provider**
  - Creates and manages infrastructure
  - VM instances, networking, security
  - Provider-specific implementation

- **Bootstrap Provider**
  - Generates node bootstrap data
  - kubeadm configuration
  - Cloud-init scripts

</v-clicks>

</div>
<div>

## Control Plane

<v-clicks>

- **Control Plane Provider**
  - Manages control plane nodes
  - (Handles etcd management)
  - Coordinates upgrades

- **KubeadmControlPlane**
  - Default implementation
  - Uses kubeadm for bootstrapping
  - Manages HA control plane

</v-clicks>

</div>
</div>