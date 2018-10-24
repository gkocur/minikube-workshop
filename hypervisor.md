# Installing kvm on Linux

Details: https://github.com/kubernetes/minikube/blob/master/docs/drivers.md

## Ubuntu/Debian
```bash
sudo apt install libvirt-clients libvirt-daemon-system qemu-kvm
```
## Centos/RHEL
```bash
sudo yum install libvirt-daemon-kvm qemu-kvm
```

# Installing kvm2 driver
```bash
curl -Lo docker-machine-driver-kvm2 https://storage.googleapis.com/minikube/releases/latest/docker-machine-driver-kvm2 \
&& chmod +x docker-machine-driver-kvm2 \
&& sudo cp docker-machine-driver-kvm2 /usr/local/bin/ \
&& rm docker-machine-driver-kvm2
```

# Installing hyperkit on Mac OS

## Homebrew
```bash
brew install docker-machine-driver-hyperkit
```
## Manually
```bash
curl -Lo docker-machine-driver-hyperkit https://storage.googleapis.com/minikube/releases/latest/docker-machine-driver-hyperkit \
&& chmod +x docker-machine-driver-hyperkit \
&& sudo cp docker-machine-driver-hyperkit /usr/local/bin/ \
&& rm docker-machine-driver-hyperkit \
&& sudo chown root:wheel /usr/local/bin/docker-machine-driver-hyperkit \
&& sudo chmod u+s /usr/local/bin/docker-machine-driver-hyperkit
```

If you encountered errors like Could not find hyperkit executable, you might need to install Docker for Mac