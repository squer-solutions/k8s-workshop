# Hands on: Pods

Create a new pod using the `kubectl run` command:
`kubectl run nginx --image=nginx`

See the logs of this pod:
`kubectl logs nginx`

Open a shell in the pod:
`kubectl exec -it nginx -- sh`

List all pods:
`kubectl get pods`

Delete the pod:
`kubectl delete pod nginx`

List all pods again for verification:
`kubectl get pods`
