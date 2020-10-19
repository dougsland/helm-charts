# helm-charts
Just Another Helm Charts repo.

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
## Devel
### Creating the repo
1. Create the helm charts and repo  
```
$ mkdir helm-charts && cd helm-charts  
$ helm create speedtest  (remove files not needed)  
$ helm package speedtest  
$ helm repo index .  
```

2. Create the github pages
2.1 Go to github repo settings and enable githubpages on master
