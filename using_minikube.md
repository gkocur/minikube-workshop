# Let's check what we have here:
```bash
kubectl get pods
kubectl get services
kubectl get deployments
kubectl get configmaps
kubectl get secrets
```

# Let's run something:
## Using cli:
```bash
kubectl run nginx --image=nginx --replicas=2
```

Exercise:
Check what is running now using cli and dashboard ;)
We have 1 deployment with 2 pods. No services, so we can't interact with it.

```bash
kubectl expose deployment nginx --type=NodePort --port 80 --name=nginx
```

Now we can access the service:
`curl -v $(minikube ip):<port>`

Let's clear the cluster:
```bash
kubectl delete deployment nginx
kubectl delete service nginx
```

## Using manifest files
```bash
kubectl create -f k8s/nginx/deployment.yaml
kubectl create -f k8s/nginx/service.yaml
```
Let's play with it...

... and clean it up:
```bash
kubectl delete -f k8s/nginx/deployment.yaml
kubectl delete -f k8s/nginx/service.yaml
```