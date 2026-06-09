# keycloak

Install keycloak:
```
helm upgrade -i keycloak \
  oci://registry-1.docker.io/cloudpirates/keycloak \
  --namespace keycloak \
  --create-namespace \
  --set keycloak.adminPassword=admin \
  --set keycloak.hostname=https://keycloak.k8s.shubhamtatvamasi.com \
  --set keycloak.proxyHeaders=xforwarded \
  --set ingress.enabled=true \
  --set ingress.className=traefik \
  --set "ingress.hosts[0].host=keycloak.k8s.shubhamtatvamasi.com" \
  --set "ingress.hosts[0].paths[0].path=/" \
  --set "ingress.hosts[0].paths[0].pathType=Prefix" \
  --set "ingress.tls[0].hosts[0]=keycloak.k8s.shubhamtatvamasi.com" \
  --set "ingress.tls[0].secretName=keycloak-tls"
```
