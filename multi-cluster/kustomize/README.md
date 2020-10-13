# Helm Example

This example will deploy the [Kubernetes sample guestbook](https://github.com/kubernetes/examples/tree/master/guestbook/) application
using kustomize. The app will be deployed into the `fleet-mc-kustomize-example` namespace.

The application will be customized as follows per environment:

* Test clusters: Disable Redis replication
* Prod clusters: Scale the front deployment to 3 and enable replication

```yaml
kind: GitRepo
apiVersion: fleet.cattle.io/v1alpha1
metadata:
  name: kustomize
  namespace: fleet-local
spec:
  repo: https://github.com/rancher/fleet-examples/
  bundleDirs:
  - kustomize
  targetCustomization:
  - name: test
    clusterSelector:
      matchLabels:
        env: test

  - name: prod
    clusterSelector:
      matchLabels:
        env: prod
```
