# Hands on: Resource Requests and Limits

Create new namespace:
`kubectl create namespace resource-test`

Create a resource quota for the new namespace:
`kubectl apply -f ./resources/resource-quota.yaml`

Explore the quota:
`kubectl describe resourcequota resource-quota --namespace=resource-test`

Add a pod without specifying resource requests and limits:
`kubectl apply -f ./resources/pod-no-resources.yaml --namespace=resource-test`

Add a pod with resource requests and limits:
`kubectl apply -f ./resources/pod-with-resources.yaml --namespace=resource-test`

Explore the quota:
`kubectl describe resourcequota resource-quota --namespace=resource-test`

Create more pods to reach the quota:
`kubectl apply -f ./resources/pod-with-resources1.yaml --namespace=resource-test`
`kubectl apply -f ./resources/pod-with-resources2.yaml --namespace=resource-test`