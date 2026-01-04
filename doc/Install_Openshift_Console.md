
## Openshift Console  

### Install 
```bash
oc apply -k microshift_install/services/openshift-console
oc get pods -n openshift-console
```

Get URL from Openshift Console  
```bash
echo "http://$(oc get route openshift-console -n openshift-console -o jsonpath='{.spec.host}')"
```