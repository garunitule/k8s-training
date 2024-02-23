## k8s-training
k8sに慣れるために、nginx + Goアプリケーションをk8sにデプロイしてみる

## 事前準備
minikube version: v1.32.0

namespaceを作成
```
kubectl create namespace nginx
```

ConfigMapを作成
```
kubectl create configmap nginx-conf --from-file=default.conf -n nginx
```

クラスタにデプロイ
```
kubectl apply -f nginx-echo-server.yml
```

## ディレクトリ構成
```txt
.
├── nginx
│   ├── static_content/
│   └── Dockerfile
├── docker-compose.yml
└── README.md

```