# Hands on: Deployments

kubectl create deployment my-deploy --image=nginx:1.24

kubectl get deployments

kubectl get replicasets

kubectl get pods

kubectl describe pod my-deploy…

kubectl describe replicaset my-deploy…

kubectl scale --replicas=3 deploy/my-deploy

kubectl get deployments

kubectl get pods

kubectl delete pod my-deploy…

kubectl get pods

kubectl rollout history deployment my-deploy

kubectl set image deployment my-deploy nginx=nginx:1.25

kubectl rollout history deployments my-deploy --revision=1

kubectl rollout undo deployment my-deploy --to-revision=1

kubectl rollout history deployment my-deploy
