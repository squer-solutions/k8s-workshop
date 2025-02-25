# Hands on: Setting up a Kind Cluster with Ingress

Install NGINX Ingress controller to cluster: 
`kubectl apply \
    --filename https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml --wait`