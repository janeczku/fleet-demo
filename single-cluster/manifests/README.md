# Manifests Example

This example will deploy a KVM virtual machine on a cluster node (Requires KubeVirt).

```yaml
kind: GitRepo
apiVersion: fleet.cattle.io/v1alpha1
metadata:
  name: manifests
  namespace: fleet-local
spec:
  repo: https://github.com/janeczku/fleet-demo/
  paths:
  - single-cluster/manifests
```
