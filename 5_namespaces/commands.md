# Discover the default namespaces
`kubectl get namespaces`

# Create a new namespace
`kubectl create namespace my-namespace`

# Get all resources in a namespace
`kubectl get all --namespace ingress-nginx`
`kubectl get all -n ingress-nginx`

# Switch to a namespace
`kubectl config set-context --current --namespace=my-namespace`

# Delete a namespace
`kubectl delete namespace my-namespace`