## Argo CD

![Alt text](screenshots/Screenshot_Argo.png "Argo CD")

### Install
Add Helm repo 4 Argo
```bash
helm repo add argo https://argoproj.github.io/argo-helm
helm repo update
```

Install ArgoCD via Helm
```bash
helm install argocd argo/argo-cd \
  -n argocd \
  --create-namespace \
  -f microshift_install/services/argo/argo_install/argo-helm.yaml.yaml
```



Get the Argo CD admin password
```bash
oc get secret argocd-initial-admin-secret \
    -n argocd \
    -o jsonpath={.data.password} | base64 -d
```

Get the Argo CD URL
```bash
echo "https://$(oc get route argocd-server \
    -n argocd \
    -o jsonpath='{.spec.host}')"
```

Install the bootstrap app for Argo CD
```bash
oc apply -f microshift_install/services/argo/argo_bootstrap_cluster/bootstrap-cluster.yaml
```


