```yaml
layout: two-cols-header
layoutClass: gap-4
```

# Gateway API Troubleshooting

## Common Issues

::left::

<v-click>

- ### Configuration
  - Invalid Gateway class
  - Missing ReferenceGrants
  - TLS certificate issues
  - Route conflicts

</v-click>

<v-click>

- ### Troubleshooting
  - Check Gateway status
  - Verify route attachments
  - Review controller logs
  - Test connectivity

</v-click>

# Debugging Steps

::right::

<v-click>

- ### Check Resources
  ```bash
  kubectl get gateway,httproute -A
  kubectl describe gateway my-gateway
  kubectl describe httproute my-route
  ```

</v-click>

<v-click>

- ### Controller Logs
  ```bash
  kubectl logs -n gateway-system \
    -l app=gateway-controller
  kubectl get events --field-selector \
    type=Warning
  ```

</v-click>