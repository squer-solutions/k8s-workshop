# Hands on: Setting up a Kind Cluster with Ingress

Start a new Kind cluster:
`kind create cluster --config ./networking/kind.yaml`

Install the Ingress Controller:
`kubectl apply \
--filename https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml`

Create a demo deployment to showcase the Ingress:
`kubectl apply -f ./networking/ingress-demo.yaml`

Open in your browser:
`http://localhost:8080/foo`
`http://localhost:8080/bar`
