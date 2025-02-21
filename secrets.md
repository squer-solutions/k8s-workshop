# Hands on: Secrets

Create a new Secret using a literal value:
`kubectl create secret generic db-creds --from-literal=pwd=s3cre!`

Create a new Secret using an `.env` file:
`kubectl create secret generic db-creds --from-env-file=secret.env`

Create a new Secret using an SSH key:
`kubectl create secret generic ssh-key --from-file=id_rsa=~/.ssh/id_rsa`

Encoding a literal value in base64 (compare that with the first secret):
`echo -n 's3cre!' | base64`
