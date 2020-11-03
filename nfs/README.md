## Deployment Instructions
```
kubectl create ns nfs
```
```
kubectl create -f rbac.yaml -f class.yaml -f deployment.yaml
```