# multi_node_cluster

勉強会用に作成したkindを使用したK8sリポジトリ

## 手順

### インストール準備

```
brew install kubectl
brew install kind
brew install argoproj/tap/kubectl-argo-rollouts
```

### kindのクラスター作成

```
kind create cluster --config kind-cluster-config.yaml --name argorollout-cluster
```

### Argo Rolloutのインストール

```
kubectl create namespace argo-rollouts
kubectl apply -n argo-rollouts -f https://github.com/argoproj/argo-rollouts/releases/latest/download/install.yaml
```

### nginx達のapply

```
kubectl apply -k ./
```

## ダッシュボード確認

## nginx確認

## 新しいrolloutデプロイ

## active, previewの確認

## プロモート

## active確認

なんかactiveとpreviewがどっちも一緒のイメージになっちゃう
zenn描かなきゃ
```brew install argocd```

```kubectl apply -f rollout/nginx-rollout.yaml```

```brew install argoproj/tap/kubectl-argo-rollouts```

```kubectl apply -k ./```

```kubectl argo rollouts dashboard```

## Tips

nginx-active: <http://localhost:30080>
nginx-preview: <http://localhost:30100>

## 参考

- <https://github.com/argoproj/argo-cd>
- <https://argo-cd.readthedocs.io/en/stable/getting_started/#1-install-argo-cd>
