# Hands on: Set up your local Kind Cluster

```bash
choco install kind

kind create cluster
kind get clusters

kubectl cluster-info --context kind-kind

kubectl get all
```

## Alternative methods

Using `winget` instead of `choco`:
`winget install Kubernetes.kind`

Alternatively get latest release binary from:
https://github.com/kubernetes-sigs/kind/releases
rename to `kind.exe` add file to your path variable.