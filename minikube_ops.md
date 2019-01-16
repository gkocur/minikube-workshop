Let's copy paste help: ;)

# Starting
To start with default virtualization and cpu/memory setting:
```bash
minikube start
```
To set cpu/memory
```bash
minikube start --cpus 4 --memory 4096
```
## Linux
To start on linux system with kvm hypervisor:
```bash
minikube start --vm-driver kvm2
```
It's possible to run on host system directly with `--vm-driver none`.
## Mac OS
To start on OSX with `hyperkit` driver:
```bash
minikube start --vm-driver hyperkit
```
# Status
TO check if minikube is running:
```bash
minikube status
```

# Get IP
To get the IP of VM:
```bash
minikube ip
```

# Dashboard
To run k8s dashboard:
```bash
minikube dashboard
```

# SSH to virtual machine
To ssh into vm with k8s:
```bash
minikube ssh
```

# Use as docker environment
To use docker daemon running on minikube (for example to build image, run container itp.):
```bash
eval $(minikube docker-env)
```
or on fish:
```bash
eval (monikube docker-env)
```
It will automatically recognize your shell and use commands specific to it (well, it's supposed to do it ;)

# Stopping
To stop running minikue vm:
```bash
minikube stop
```
# Deleting
Kill'em all:
```bash
minikube delete
```
