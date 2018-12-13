# Getting started

Creating a cluster admin role for your user 

```
kubectl create clusterrolebinding cluster-adm \
--clusterrole=cluster-admin \
--user=$(cat ~/.oci/config | grep user | cut -c 6-)
```

Installing the dashboard 

```
kubectl apply -f \
https://raw.githubusercontent.com/kubernetes/dashboard/master/src/deploy/recommended/kubernetes-dashboard.yaml
```

Log into the dashboard

```
http://localhost:8001/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/
```
