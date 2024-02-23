## k8s-training
k8sに慣れるために、nginx + Goアプリケーションをk8sにデプロイしてみる

## アーキテクチャ
TODO

## 環境
minikube version: v1.32.0

## クラスタにデプロイ
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
│   ├── conf/
│   ├── static_content/
│   └── Dockerfile
├── default.conf
├── docker-compose.yml
├── nginx-echo-server.yml
└── README.md

```