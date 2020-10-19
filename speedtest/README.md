# DEVELOPMENT
## TESTING INSTALL LOCALLY VIA DRY-RUN:
```
helm install \
  speedtest \
  --dry-run \
  --debug \
  . \
  --set ingressroute.enabled=True \
  --set ingressroute.hosts=speedtest.medogz.com \
  --set ingressroute.tls=true \
  --set ingressroute.tls=tls-traefikv2
```
