# nfs-client-provisioner Deployment Instructions

This will deploy a very basic class and deployment to provide dynamic NFS persistent storage to your test cluster.

Create a namespace for nfs.

```
kubectl create ns nfs
```
Next deploy rbac changes a class and deployment manifest.

```
kubectl create -f rbac.yaml -f class.yaml -f deployment.yaml
```

That is all you need to do here. Now you will be able to add dynamic persistent storage to your deployments.