# Hands on: Secrets

kubectl create secret generic db-creds --from-literal=pwd=s3cre!

kubectl create secret generic db-creds --from-env-file=secret.env

kubectl create secret generic ssh-key --from-file=id_rsa=~/.ssh/id_rsa

echo -n 's3cre!' | base64
