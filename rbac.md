# Hands on: Role Based Access Control

## ServiceAccounts

Get all ServiceAccounts in the cluster:
`kubectl get serviceaccounts`

Get the default ServiceAccount and explore the secret:
`kubectl get serviceaccount default -o yaml | grep -A 1 secrets:`

Get the secret of the default ServiceAccount (replace the secret name with the one from the previous command):
`kubectl get secret default-token- -o yaml`

Run a pod:
`kubectl run sa-test --image=nginx`

Explore the specs of this pod:
`kubectl get pod sa-test -o yaml`

Create a new ServiceAccount:
`kubectl create serviceaccount custom`

Create a new pod with the custom ServiceAccount:
`kubectl run sa-custom --image=nginx --serviceaccount=custom`

## Roles and RoleBindings

Create a new ServiceAccount:
`kubectl create serviceaccount rbac-test`

Create a new Role that allows to get pods:
`kubectl create role pod-reader --verb=get --resource=pods`

Bind the Role to the ServiceAccount:
`kubectl create rolebinding pod-reader-binding --role=pod-reader --serviceaccount=default:rbac-test`

Confirm that the Service account has the permission to get pods:
`kubectl auth can-i get pod --as=system:serviceaccount:default:rbac-test`

Check if the Service account has the permission to get deployments:
`kubectl auth can-i get deployment --as=system:serviceaccount:default:rbac-test`