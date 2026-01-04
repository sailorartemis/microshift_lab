## OpenShift Console

![Alt text](screenshots/Screenshot_Pods2.png "OpenShift Console")

### Install

Deploy OpenShift Console
```bash
oc apply -k microshift_install/services/openshift-console
oc get pods -n openshift-console
```

Get the OpenShift Console URL
```bash
echo "http://$(oc get route openshift-console -n openshift-console -o jsonpath='{.spec.host}')"
```