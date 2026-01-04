## ArgoCD

### Install

Add Helm Repo for Trivy
```bash
helm repo add aqua https://aquasecurity.github.io/helm-charts/
helm repo update
```

Install Trivy via Helm
```bash
helm install trivy-operator aqua/trivy-operator \
  -n trivy-system \
  --create-namespace \
  -f values.yaml
```

Prometeus config:
```yaml
    scrape_configs:
      - job_name: 'trivy-operator'
        static_configs:
          - targets: ['trivy-operator.trivy-system.svc.cluster.local:8080']
        metrics_path: /metrics
        scrape_interval: 30s
```
