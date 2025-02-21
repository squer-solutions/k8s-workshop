# Hands on: ConfigMaps

Create a new ConfigMap using a literal value:
`kubectl create configmap db-config --from-literal=db=staging`

Create a new ConfigMap using an `.env` file:
`kubectl create configmap db-config --from-env-file=config.env`

Create a new ConfigMap using a text file:
`kubectl create configmap db-config --from-file=config.txt`

Create a new ConfigMap using a directory:
`kubectl create configmap db-config --from-file=app-config`

Example of using a ConfigMap as environment in a pod:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: configured-pod
spec:
  containers:
  - image: nginx:1.19.0
    name: app
    envFrom:
    - configMapRef:
        name: db-config
```

Create the pod using the configuration file and check the environment variables:
`kubectl exec configured-pod -- env`
