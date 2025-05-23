# Core Concepts

<div class="grid grid-cols-2 gap-4">

<div>

<v-click>

1. **Cluster** 
   - Represents a Kubernetes cluster
   - Defines cluster-wide settings
   - References infrastructure and control plane

</v-click>

<v-click>

2. **Machine** 
   - A node in the cluster
   - Maps to a single node
   - Contains provider-specific details

</v-click>

</div>

<div>

<v-click>

3. **MachineDeployment**
   - Manages a set of Machines
   - Similar to Kubernetes Deployments
   - Handles rolling updates

</v-click>

<v-click>

4. **MachineSet**
   - Ensures a specified number of Machine replicas
   - Similar to Kubernetes ReplicaSets
   - Managed by MachineDeployments

</v-click>

</div>

</div>