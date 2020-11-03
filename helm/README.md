### Helm Commands

```
kubectl -n kube-system create serviceaccount tiller
```

```
kubectl create clusterrolebinding tiller --clusterrole cluster-admin --serviceaccount=kube-system:tiller
```

```
helm2 init --service-account tiller
```
For Helm 2
```
helm2 repo add stable https://charts.helm.sh/stable
```
For Helm 3
```
helm repo add stable https://charts.helm.sh/stable
```
```
helm2 inspect values stable/prometheus > /tmp/prometheus.values
```
Find server section under type and add the following 
```
    ## List of IP addresses at which the Prometheus server service is available
    ## Ref: https://kubernetes.io/docs/user-guide/services/#external-ips
    ##
    externalIPs: []

    loadBalancerIP: ""
    loadBalancerSourceRanges: []
    servicePort: 80
    sessionAffinity: None
    nodePort: 32322
    type: NodePort
```
Install prometheus
```
helm2 install stable/prometheus --name prometheus --values /tmp/prometheus.values --namespace prometheus
```
```
helm2 inspect values stable/grafana > /tmp/grafana.values
```
Find service: just below deployment annotations and chage the following
```
service:
   type: NodePort
   nodePort: 32323
   port: 80
   annotations: {}
   labels: {}
```
update the admin password as seen below
```
adminUser: admin
adminPassword: updatethispassword
```
Enable persistence
```
persistence:
   enabled: true
```
Install Grafana
```
helm2 install stable/grafana --name grafana --values /tmp/grafana.values --namespace grafana
```
To remove helm installs (helm2 remove [install name] --purge)

eg.
```
helm2 delete grafana --purge
```