# Create a pod with a custom label

`kubectl run label-pod --image=nginx --labels="app=web,env=dev"`

# Add a label to a pod
`kubectl label pod label-pod foo=bar`

# Remove a label from a pod
`kubectl label pod label-pod foo-`

# List all pods while showing labels 
`kubectl get pods --show-labels`