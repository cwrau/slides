# Core Concepts

## Gateway API Building Blocks

<v-click>

- ### GatewayClass
  - Defines the type of Gateway implementation
  - Similar to StorageClass concept
  - Infrastructure provider specific

</v-click>

<v-click>

- ### Gateway
  - Represents a network endpoint
  - Configures load balancer, proxy, etc.
  - Defines listeners and routes

</v-click>

<v-click>

- ### Route Resources
  - HTTPRoute, GRPCRoute, TCPRoute
  - Define routing rules
  - Attach to Gateway resources 

</v-click>