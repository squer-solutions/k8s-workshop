# Hands on: Working with Kubectl

Display all available contexts:

`kubectl config get-contexts`

Display the current-context:

`kubectl config current-context`

General commands:

`kubectl [command] [TYPE] [NAME] [flags]`

Using `kubectl explain` to get information about a resource definition:

`kubectl explain TYPE [--recursive=false] [flags]`

```bash
kubectl explain pod

kubectl explain pod.spec

kubectl explain pod.spec -–recursive
```

Display all available resources including abbreviations:

`kubectl api-resources`
