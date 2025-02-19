# Hands on: Environment Variables

kubectl run env-test –image=nginx --env “foo=bar”

kubectl exec envar-demo -- printenv
