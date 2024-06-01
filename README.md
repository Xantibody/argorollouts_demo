# multi_node_cluster

勉強会用に作成したkindを使用したK8sリポジトリ

```kind create cluster --config kind-config.yaml```

```
kubectl create namespace argo-rollouts
kubectl apply -n argo-rollouts -f https://github.com/argoproj/argo-rollouts/releases/latest/download/install.yaml
```

## 参考

- <https://github.com/argoproj/argo-cd>
- <https://argo-cd.readthedocs.io/en/stable/getting_started/#1-install-argo-cd>
