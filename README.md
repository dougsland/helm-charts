# helm-charts
Just Another Helm Charts repo.

Supported charts:

| Chart     | Based on Image              |
|-----------|-----------------------------|
| speedtest | adolfintel/speedtest:latest |
| --        | --                          |
| --        | --                          |
| --        | --                          |

## Usage
```
$ helm repo add dougsland https://dougsland.github.io/helm-charts  
$ helm search repo speedtest  
$ helm install \
    speedtest \
    speedtest \
    --set ingressroute.enabled=True \
    --set ingressroute.hosts=speedtest.medogz.com \
    --set ingressroute.tls=true \
    --set ingressroute.tls=tls-traefikv2
```
## Uninstall
### repo
```
$ helm repo remove dougsland
```
### Uninstall chart
Example:
```
$ helm uninstall speedtest
```
