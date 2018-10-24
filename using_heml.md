# Installing helm on k8s cluster (tiller) and locally

By default minikube has RBAC enabled. You have to setup a service-account with role sufficient to create resources.
```bash
kubectl create -f k8s/helm/rbac.yaml
```
Install helm:
```bash
helm init --service-account tiller
```
# Using charts

Charts repository: https://github.com/helm/charts

Install a chart with default values:
```bash
helm install --name my stable/mysql
```

Install chart with custom values:
```bash
helm install --name my -f k8s/helm/mysql/values.yml   stable/mysql
```
helm install --name my -f k8s/helm/mysql/values.yml   stable/mysql

Delete chart permanently
```bash
helm delete my --purge
```
helm delete my --purge

