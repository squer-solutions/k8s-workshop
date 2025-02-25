# Create deployment

`kubectl create deployment nginx --image=nginx --port 8080`

`kubectl get deployments`
`kubectl get replicasets`
`kubectl get pods`

`kubectl scale deployment nginx --replicas=3`

# alternative solution
`kubectl edit deployment nginx` # change replicas to 3

# get a pod and delete it
`kubectl delete pod $pod`
`kubectl get pods`

# update image 
`kubectl set image deployment/nginx nginx=bitnami/nginx`

# see rollout history
`kubectl rollout history deployment/nginx`
`kubectl rollout pause deployment/nginx`
`kubectl rollout resume deployment/nginx`
`kubectl rollout undo deployment/nginx`
`kubectl rolout status deployment/nginx`
`kubectl rollout restart deployment/nginx`
