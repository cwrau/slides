# Common Issues & Troubleshooting

<div class="grid grid-cols-2 gap-4 text-sm">
<div>

## Common Issues

<v-clicks>

1. **Cluster Creation Fails**
   - Check provider credentials
   - Verify resource quotas
   - Review CAPI controller logs

2. **Node Bootstrap Issues**
   - Examine cloud-init logs
   - Check network connectivity
   - Verify security group rules

3. **Control Plane Problems**
   - Check etcd health
   - Verify load balancer config
   - Review cert expiration

</v-clicks>

</div>
<div>

## Debugging Tools

<v-clicks>

1. **Useful Commands**
   ```bash
   k9s
   > describe $resource
   > view logs of controllers
   ```

2. **Health Checks**
   - Provider controller status
   - Machine controller status
   - Bootstrap provider status

</v-clicks>

</div>
</div> 