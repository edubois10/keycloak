# keycloak
```
openssl req -subj '/CN=test.keycloak.org/O=Test Keycloak./C=US' -newkey rsa:2048 -nodes -keyout key.pem -x509 -days 365 -out certificate.pem
```
If no sealsecret exist
```
oc create secret tls example-tls-secret --cert certificate.pem --key key.pem -n keycloak
secret/example-tls-secret created
```
Seal the secret
```
```

```
oc create secret generic keycloak-db-secret \
  --from-literal=username= \
  --from-literal=password= -n keycloak
```

Seal the Secret