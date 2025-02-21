# Hands on: Labels

Look at the details of a pod from the deployment (replace `my-deploy-` with the actual pod name):
`kubectl describe pod my-deploy-`

Look at the details of a replicaset from the deployment (replace `my-deploy-` with the actual replicaset name):
`kubectl describe replicaset my-deploy-`

Create a new pod with labels using the `kubectl run` command:
`kubectl run labeled-pod --image=nginx --restart=Never --labels=tier=backend,env=dev`

Look at the details of the pod:
`kubectl describe pod labeled-pod | grep -C 2 Labels:`

Add a label to the pod:
`kubectl label pod labeled-pod region=eu`

Review the labels of the pod:
`kubectl get pod labeled-pod --show-labels`

Change a label on the pod:
`kubectl label pod labeled-pod region=us --overwrite`

Review the labels of the pod:
`kubectl get pod labeled-pod --show-labels`

Remove a label from the pod:
`kubectl label pod labeled-pod region-`

Review the labels of the pod:
`kubectl get pod labeled-pod --show-labels`
