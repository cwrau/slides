# Kubernetes Tooling

[By Chris Werner Rau](https://cwrau.io)




#### [ExternalDNS](https://github.com/kubernetes-sigs/external-dns)

Exposes kubernetes services and ingresses with DNS entries



#### [traefik](https://github.com/traefik/traefik)

Cloud native reverse proxy and kubernetes ingress provider



#### [cert-manager](https://github.com/jetstack/cert-manager)

cert-manager automates the issuance of certificates using http and / or dns based challenges.



#### [Jaeger](https://github.com/jaegertracing/jaeger)

Jaeger provides cross application tracing capabilities



#### [Kubernetes Metrics Server](https://github.com/kubernetes-sigs/metrics-server)

Exposes metrics in the kubernetes apiserver, which then can be used for hpa and / or vpa



#### [Prometheus](https://github.com/prometheus/prometheus)

Time series database used for metrics



#### [Loki](https://github.com/grafana/loki/)

Central logging storage for kubernetes, can be queried by Grafana



#### [Grafana](https://github.com/grafana/grafana)

Displays metrics from various sources for analysis and dashboards



#### [Flux](https://github.com/fluxcd/flux)

flux implements a gitops based workflow



#### [Reflector](https://github.com/emberstack/kubernetes-reflector)

Automates the replication of secrets, configmaps and certificates



#### [Helm Operator](https://github.com/fluxcd/helm-operator)

helm-operator provides a CRD to install helm releases into your kubernetes cluster



#### [Kubernetes Janitor](https://github.com/hjacobs/kube-janitor)

Automates the deletion of resources based on a ttl or deadline



#### Backups

Haven't found a satisfying solution yet.

- Velero is too much, badly documented for automated usage
    - good for end users, bad for administrators
    - mostly documented using the CLI
    - cannot only backup data
    - can only restore data when also restoring pods
- Stash has various problems but a smaller feature set
    - no CLI
        - bad for users, ok for administrators
    - relatively well documented
