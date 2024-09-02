#Prometheus Operator
I stumbled accross [Prometheus Operator](https://prometheus-operator.dev/docs/getting-started/installation/) which provides an out of box monitoring stack for your K8s cluster. 

I installed this using [Helm](https://helm.sh/docs/), using the community [kube-prometheus-stack](https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack#kube-prometheus-stack) Helm chart. It all seem to go relatively smoothly. 

## Gotchas and notes
- I'm a big dumb dumb and it took me far too long to figure out the syntax to install the Helm chart which is ```helm install kube-prometheus-stack prometheus-community/kube-prometheus-stack``` 
- The default credentials for Grafana will be username: **admin** and pw: **prom-operator**

