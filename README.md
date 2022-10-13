# OpenSearch Day 2 lifecycle management with KubeDB

KubeDB OpsRequest is an enterprise grade feature for databases. Get a free 30 day KubeDB Enterprise Edition trial licence from [AppsCode License server](https://license-issuer.appscode.com/?p=kubedb-enterprise). Now, install KubeDB with the license.

```
$ helm repo add appscode https://charts.appscode.com/stable/
$ helm repo update
$ helm install kubedb appscode/kubedb \
  --version v2022.08.08 \
  --namespace kubedb --create-namespace \
  --set kubedb-provisioner.enabled=true \
  --set kubedb-ops-manager.enabled=true \
  --set kubedb-dashboard.enabled=true \
  --set-file global.license=/path/to/the/license.txt
```

To provision an OpenSearch Topology cluster:
```bash
$ kubectl apply -f os_topology.yaml
```

To provision an OpenSearch-Dashboards for the cluster:
```bash
$ kubectl apply -f os_dashboard.yaml
```

To horizontally upgrade your cluster:
```bash
$ kubectl apply -f os_horizontal_scaling.yaml
```

To vertically upgrade your cluster:
```bash
$ kubectl apply -f os_vertical_scaling.yaml
```

To view all the supported OpenSearch versions by KubeDB:
```bash
$ kubectl get esversion | grep opensearch
```

To Upgrade your cluster version:
```bash
$ kubectl apply -f os_upgrade.yaml
```

To restart your cluster:
```bash
$ kubectl apply -f os_restart.yaml
```

For hands on demo, take a deep dive into the full webinar below:

[![OpenSearch OpsReq](https://img.youtube.com/vi/gSoWaVV4iQo/0.jpg)](https://www.youtube.com/watch?v=gSoWaVV4iQo)



