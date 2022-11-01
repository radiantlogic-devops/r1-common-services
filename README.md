# r1-common-services

This Helm chart deploys the following applications using helm charts. These applications are proxied using HA Proxy.

- [Prometheus](https://github.com/prometheus-community/helm-charts/tree/main/charts/prometheus)
- [Grafana](https://github.com/grafana/helm-charts)
- [Elasticsearch](https://github.com/elastic/helm-charts/tree/main/elasticsearch)
- [Kibana](https://github.com/elastic/helm-charts/tree/main/kibana)
- [Argo CD](https://github.com/argoproj/argo-helm/tree/main/charts/argo-cd)
- [HA Proxy](https://github.com/haproxytech/helm-charts/tree/main/haproxy)

## Usage

```
helm dependency uppdate charts/services
helm upgrade --install my-release charts/services
```

## Access

```
kubectl port-forward svc/haproxy 8080:80
```

Access the services using these URLs.

- Prometheus - http://localhost:8080/prometheus
- Grafana - http://localhost:8080/grafana
- Elastic Search - http://localhost:8080/elacticsearch
- Kibana - http://localhost:8080/kibana
- Argo CD - http://localhost:8080/argocd

