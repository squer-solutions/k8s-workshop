# Hands on: ConfigMaps

kubectl create configmap db-config --from-literal=db=staging

kubectl create configmap db-config --from-env-file=config.env

kubectl create configmap db-config --from-file=config.txt

kubectl create configmap db-config --from-file=app-config

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

kubectl exec configured-pod -- env
