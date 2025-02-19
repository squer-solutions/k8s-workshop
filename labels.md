# Hands on: Labels

kubectl describe pod my-deploy…

kubectl describe replicaset my-deploy…

kubectl run labeled-pod --image=nginx \
  --restart=Never --labels=tier=backend,env=dev

kubectl describe pod labeled-pod | grep -C 2 Labels:

kubectl label pod labeled-pod region=eu

kubectl get pod labeled-pod --show-labels

kubectl label pod labeled-pod region=us --overwrite

kubectl get pod labeled-pod --show-labels

kubectl label pod labeled-pod region-

kubectl get pod labeled-pod --show-labels
