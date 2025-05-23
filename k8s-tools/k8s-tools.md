# Kubernetes Tools

[By Chris Werner Rau](https://cwrau.io)



## Is Awesome!



## But

Kinda awkward to work with



### Tools

That's why there are a multitude of tools to help you!



## CLI


#### [K9s](https://github.com/derailed/k9s)

Hands down the best tool for a quick and deep overview of your cluster

Even simple administration


#### [kube-ops-view](https://github.com/hjacobs/kube-ops-view)

Funky multi cluster overview 


#### [heluxup](https://github.com/ekeih/heluxup)

Checks for updates for [helm-operator](https://github.com/fluxcd/helm-operator) HelmReleases


#### [telepresence](https://github.com/telepresenceio/telepresence)

Lifts your local development into the cluster


## BROWSER


#### [kube-web-view](https://github.com/hjacobs/kube-web-view)

Multi cluster search/overview


## HTML


#### [kube-resource-report](https://github.com/hjacobs/kube-resource-report)

Cost report

Only really for aws/gcp, but still a good overview



## In-Cluster


### Operators


#### [vertical-pod-autoscaler](https://github.com/kubernetes/autoscaler/tree/master/vertical-pod-autoscaler)

Automagically (😉) sets the right resource requests and limits

Configurable, of course


#### [goldilocks](https://github.com/FairwindsOps/goldilocks)

Auto-configures vpa and provides dashboard


#### [downscaler](https://github.com/hjacobs/kube-downscaler)

Time based scaling of your resources


#### [janitor](https://github.com/hjacobs/kube-janitor)

Cleans up resources after a defined duration or at a point in time

(Good for demo systems / CI/CD magic)


#### [flux](https://github.com/fluxcd/flux)

Implements GitOps!!!! 👊(o(*ﾟ▽ﾟ*)o)🥳


#### [helm-operator](https://github.com/fluxcd/helm-operator)

Provides and implements a `HelmRelease`-Resource


### [k-rail](https://github.com/cruise-automation/k-rail)

Admission webhook for security



## Plugins


### Helm


#### [diff](https://github.com/databus23/helm-diff)

Provides a diff for the upgrade


#### [whatup](https://github.com/bacongobbler/helm-whatup)

Checks for updates of helm releases

(Only local repo though)


### Kubectl


#### [krew](https://github.com/kubernetes-sigs/krew)

Kubectl plugin manager


#### [access-matrix](https://github.com/corneliusweig/rakkess)

Little overview of your access to the cluster


#### [konfig](https://github.com/corneliusweig/konfig)

Helps merging kube configs


#### [debug](https://github.com/aylei/kubectl-debug)

Awesome for debugging containers without shell

``k debug -n resume cwr-b9547b7cf-tgpdv --image=alpine -c caddy -a --port-forward  ash``



## Shell Aliases
