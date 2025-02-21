# Hands on: Deployments

Create a new deployment using the `kubectl create deployment` command:
`kubectl create deployment my-deploy --image=nginx:1.24`

List all deployments:
`kubectl get deployments`

List all replicasets:
`kubectl get replicasets`

List all pods:
`kubectl get pods`

Look at the details of a pod from the deployment (replace `my-deploy-` with the actual pod name):
`kubectl describe pod my-deploy-`

Look at the details of a replicaset from the deployment (replace `my-deploy-` with the actual replicaset name):
`kubectl describe replicaset my-deploy-`

Scale the deployment to 3 replicas:
`kubectl scale --replicas=3 deploy/my-deploy`

List all deployments:
`kubectl get deployments`

List all pods:
`kubectl get pods`

Delete a pod from the deployment (replace `my-deploy-` with the actual pod name):
`kubectl delete pod my-deploy-`

List all pods again:
`kubectl get pods`

Look at the history of the deployment:
`kubectl rollout history deployment my-deploy`

Update the deployment to use a different image:
`kubectl set image deployment my-deploy nginx=nginx:1.25`

Revisit the history of the deployment:
`kubectl rollout history deployment my-deploy`

Show the details of the deployment at a specific revision:
`kubectl rollout history deployments my-deploy --revision=1`

Rollback the deployment to the previous version:
`kubectl rollout undo deployment my-deploy --to-revision=1`

Revisit the history of the deployment:
`kubectl rollout history deployment my-deploy`
