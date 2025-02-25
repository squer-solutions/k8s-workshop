# create a service account pod-viewer
`kubectl create serviceaccount pod-viewer`

# create a role pod-reader
`kubectl create role pod-viewer-role --resource pods --verb get,list,watch`

# create a rolebinding pod-viewer-binding
`kubectl create rolebinding pod-viewer-binding --role=pod-viewer-role --serviceaccount=default:pod-viewer`

# create a pod pod-viewer
`kubectl run pod-viewer --image=bitnami/kubectl --rm -it -- sh`
