# Example: Creating a Workload Cluster

```yaml {all|6-8|9-12|13-|all}
apiVersion: cluster.x-k8s.io/v1beta1
kind: Cluster
metadata:
  name: example-cluster
spec:
  clusterNetwork:
    pods:
      cidrBlocks: ["192.168.0.0/16"]
  controlPlaneRef:
    kind: KubeadmControlPlane
    apiVersion: controlplane.cluster.x-k8s.io/v1beta1
    name: example-control-plane
  infrastructureRef:
    kind: OpenStackCluster
    apiVersion: infrastructure.cluster.x-k8s.io/v1beta1
    name: example-cluster
```

---

# Example: Control Plane Setup

```yaml {all|6|7|8-}
apiVersion: controlplane.cluster.x-k8s.io/v1beta1
kind: KubeadmControlPlane
metadata:
  name: example-control-plane
spec:
  replicas: 3
  version: v1.26.1
  machineTemplate:
    infrastructureRef:
      kind: OpenStackMachineTemplate
      apiVersion: infrastructure.cluster.x-k8s.io/v1beta1
      name: example-control-plane
```

---

# Example: OpenStackCluster Setup

```yaml {all|7|8|all}
apiVersion: infrastructure.cluster.x-k8s.io/v1beta1
kind: OpenStackCluster
metadata:
  name: example-cluster
spec:
  identityRef:
    cloudName: openstack-cloud
    name: openstack-credentials
```
