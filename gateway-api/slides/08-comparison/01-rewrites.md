```yaml
layout: two-cols-header
layoutClass: gap-4
```
# URL Rewrite Comparison

::left::

<v-click>

- ### Gateway API
  ```yaml
  apiVersion: gateway.networking.k8s.io/v1
  kind: HTTPRoute
  metadata:
    name: rewrite-example
  spec:
    rules:
    - filters:
      - type: URLRewrite
        urlRewrite:
          path:
            type: ReplacePrefixMatch
            replacePrefixMatch: /v2
  ```

</v-click>

::right::

<v-click>

- ### Ingress
  ```yaml
  apiVersion: networking.k8s.io/v1
  kind: Ingress
  metadata:
    name: rewrite-example
    annotations:
      nginx.ingress.kubernetes.io/rewrite-target: /v2/$2
  spec:
    rules:
    - http:
        paths:
        - path: /v1(/|$)(.*)
          pathType: Prefix
  ```

</v-click> 