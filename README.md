# keycloak

Install keycloak:
```
helm upgrade -i keycloak \
  oci://registry-1.docker.io/cloudpirates/keycloak \
  --namespace keycloak \
  --create-namespace
```
