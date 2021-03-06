# Welcome
- [Welcome](#welcome)
  * [About](#About)
  * [Supported Charts](#supported-charts)
  * [Usage](#usage)
  * [Upgrade](#upgrade)
  * [Uninstall](#uninstall)
    + [repo](#repo)
    + [Uninstall chart](#uninstall-chart)

## About
Just Another Helm Charts repo.

## Supported charts:

| Chart     | Based on Image              |
|-----------|-----------------------------|
| speedtest | [adolfintel/speedtest:latest](https://hub.docker.com/r/adolfintel/speedtest) |
| dnstools  | [infoblox/dnstools:latest](https://hub.docker.com/r/infoblox/dnstools) |
| --        | --                          |
| --        | --                          |

## Usage
Example:
```
$ helm repo add dougsland https://dougsland.github.io/helm-charts  
$ helm search repo speedtest  
$ helm install \
    speedtest \
    dougsland/speedtest \
    --set ingressroute.enabled=True \
    --set ingressroute.hosts=speedtest.medogz.com \
    --set ingressroute.tls=true \
    --set ingressroute.tls=tls-traefikv2
```

## Upgrade
```
$ helm upgrade speedtest dougsland/speedtest
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
