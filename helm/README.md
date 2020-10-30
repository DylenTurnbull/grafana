### Helm Commands

```
kubectl -n kube-system create serviceaccount tiller
```

```
kubectl create clusterrolebinding tiller --clusterrole cluster-admin --serviceaccount=kube-system:tiller
```

```
helm init --service-account tiller
```
For Helm 2
```
helm2 repo add stable https://charts.helm.sh/stable
```
For Helm 3
```
helm repo add stable https://charts.helm.sh/stable
```