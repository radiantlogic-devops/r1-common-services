# r1-common-services

This Helm chart deploys the following helm charts:
- Prometheus
- Grafana
- Elastic Search
- Kibana
- Argo CD
- HA Proxy

## Usage

```
helm dependency uppdate charts/services
helm upgrade --install my-release charts/services
```

## Access

```
kubectl port-forward svc/haproxy 8080:80
```

Access the services as the following locations

- Prometheus - http://localhost:8080/prometheus
- Grafana - http://localhost:8080/grafana
- Elastic Search - http://localhost:8080/elacticsearch
- Kibana - http://localhost:8080/kibana
- Argo CD - http://localhost:8080/argocd

