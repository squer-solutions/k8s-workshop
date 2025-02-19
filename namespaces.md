# Hands on: Namespaces

kubectl get namespace

kubectl create namespace test

kubectl run test-app -–image=nginx -–namespace=test


kubectl get pods

kubectl get pods –-namespace=test

kubectl get pods -A

kubectl config set-context --current --namespace=<namespace-name>

kubectl delete namespace test

kubectl get pods -A
