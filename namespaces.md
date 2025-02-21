# Hands on: Namespaces

List all namespaces:
`kubectl get namespace`

Create a new namespace using the `kubectl create namespace` command:
`kubectl create namespace test`

Run a new pod in the new namespace using the `kubectl run` command:
`kubectl run test-app -–image=nginx -–namespace=test`

List all pods:
`kubectl get pods`

List all pods in the new namespace:
`kubectl get pods –-namespace=test`

List all pods in all namespaces:
`kubectl get pods -A`

Change the current namespace:
`kubectl config set-context --current --namespace=<namespace-name>`

Delete the new namespace:
`kubectl delete namespace test`

List all pods in all namespaces:
`kubectl get pods -A`
