# Hands on: Selectors

Create three pods with different labels using the `kubectl run` command:
```bash
kubectl run frontend --image=nginx --labels=env=prod,team=shiny
kubectl run backend --image=nginx --labels=env=prod,team=legacy,app=v1.2.4
kubectl run database --image=nginx --labels=env=prod,team=storage
```

List all pods with their labels:
`kubectl get pods --show-labels`

List all pods with the `env=prod` label:
`kubectl get pods -l env=prod --show-labels`
