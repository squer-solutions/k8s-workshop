# Hands on: Environment Variables

Create a new pod with environment variables using the `kubectl run` command:
`kubectl run env-test –image=nginx --env “foo=bar”`

Open a shell in the pod and print the environment variables:
`kubectl exec envar-demo -- printenv`
