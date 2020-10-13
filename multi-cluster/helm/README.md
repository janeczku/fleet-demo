# Helm Example

This example will deploy the [Kubernetes sample guestbook](https://github.com/kubernetes/examples/tree/master/guestbook/) application as
packaged as a Helm chart.
The app will be deployed into the `fleet-mc-helm-example` namespace.

The application will be customized as follows per environment:

* Test clusters: No Redis replication
* Prod clusters: Enable redis replication and scale the frontend deployment to 3

```yaml
kind: GitRepo
apiVersion: fleet.cattle.io/v1alpha1
metadata:
  name: helm
  namespace: fleet-local
spec:
  repo: https://github.com/janeczku/fleet-demo/
  paths:
  - multi-cluster/helm
  targetCustomizations:
  - name: test
    clusterSelector:
      matchLabels:
        env: test

  - name: prod
    clusterSelector:
      matchLabels:
        env: prod
```
