# Fleet Examples

## Single Cluster Examples

All examples will deploy content to the local cluster running the Fleet Manager.

| Example | Description |
|-------------|-------------|
| [manifests](single-cluster/manifests/) | An example using raw Kubernetes YAML and customizing it per target cluster |
| [helm](single-cluster/helm/) | An example using Helm and customizing it per target cluster |
| [kustomize](single-cluster/kustomize/) | An example using Kustomize and customizing it per target cluster |

## Multi-Cluster Examples

The examples below will deploy a single git repo to multiple clusters at once
and configure the app differently for each target.

| Example | Description |
|-------------|-------------|
| [manifests](multi-cluster/manifests/) | A full example of using raw Kubernetes YAML and customizing it per target cluster |
| [helm](multi-cluster/helm/) | A full example of using Helm and customizing it per target cluster |
| [helm-external](multi-cluster/helm-external/) | A full example of using a Helm chart that is downloaded from a third party source and customizing it per target cluster |
| [kustomize](multi-cluster/kustomize/) | A full example of using Kustomize and customizing it per target cluster |
