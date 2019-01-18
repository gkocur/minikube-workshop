# Linux

## Using snap
```bash
sudo snap install helm --classic
```

## Using binary package:
1. Download latest release: https://github.com/helm/helm/releases
2. Unpack it (tar -zxvf helm-v2.0.0-linux-amd64.tgz)
3. Find the helm binary in the unpacked directory, and move it to its desired destination (mv linux-amd64/helm /usr/local/bin/helm)

# Mac OS

```bash
brew install kubernetes-helm
```

# Check if it's installed properly
```bash
helm help
```
