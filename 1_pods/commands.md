# Create the pod 
`kubectl run nginx --image bitnami/nginx:latest`

# See the logs of this pod
`kubectl logs nginx`

# Describe the pod
`kubectl describe pod nginx`

# Get the definition of the pod
`kubectl get pod nginx -o yaml`

# Open a shell in the pod:
`kubectl exec -it nginx -- sh`

# List all pods:
`kubectl get pods`

# Delete the pod:
`kubectl delete pod nginx`

# List all pods again for verification:
`kubectl get pods`

# Hint to get definition
`kubectl run nginx --image bitnami/nginx:latest --dry-run=client -o yaml`
---

# DIY exercise
`kubectl run hello-world --image hello-world`
`kubectl get pods`