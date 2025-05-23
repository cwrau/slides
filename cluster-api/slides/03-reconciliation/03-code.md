# Controller Implementation

<style>
  .slidev-layout {
    font-size: 0.9em;
  }
</style>

```go {all|6-12|14-20|all}
func (r *MachineReconciler) Reconcile(ctx context.Context, req ctrl.Request) (ctrl.Result, error) {
    machine := &clusterv1.Machine{}
    if err := r.Get(ctx, req.NamespacedName, machine); err != nil {
        return ctrl.Result{}, client.IgnoreNotFound(err)
    }
    // Reconciliation logic here
}

// Example reconciliation steps
steps := []func(context.Context, *clusterv1.Machine) error{
    r.reconcileBootstrap,
    r.reconcileInfrastructure,
    r.reconcileNodeRef,
    r.reconcilePhase,
}
```

<v-click>

Key aspects:
- Controller struct holds clients
- Reconcile function is the entry point
- Steps are executed in order
- Error handling at each step

</v-click>