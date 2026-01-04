## Argo CD

![Alt text](screenshots/Screenshot_Argo.png "Argo CD")

### Install
Deploy Argo CD
```bash
oc apply -k microshift_install/services/argo/argo_install/
oc get pods -n argocd
```

Get the Argo CD admin password
```bash
oc get secret argocd-initial-admin-secret -n argocd -o jsonpath={.data.password} | base64 -d
```

Get the Argo CD URL
```bash
echo "https://$(oc get route argocd-server -n argocd -o jsonpath='{.spec.host}')"
```

Install the bootstrap app for Argo CD
```bash
oc apply -f microshift_install/services/argo/argo_bootstrap_cluster/bootstrap-cluster.yaml
```


