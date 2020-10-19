# Welcome
- [Welcome](#welcome)
  * [About](#About)
  * [Supported Charts](#supported-charts)
  * [Usage](#usage)
  * [Uninstall](#uninstall)
    + [repo](#repo)
    + [Uninstall chart](#uninstall-chart)

## About
Just Another Helm Charts repo.

## Supported charts:

| Chart     | Based on Image              |
|-----------|-----------------------------|
| speedtest | [adolfintel/speedtest:latest](https://hub.docker.com/r/adolfintel/speedtest) |
| --        | --                          |
| --        | --                          |
| --        | --                          |

## Usage
Example:
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
