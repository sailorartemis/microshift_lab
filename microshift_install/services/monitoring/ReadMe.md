oc adm policy add-scc-to-user hostmount-anyuid \
  -z node-exporter \
  -n observability

or

oc adm policy add-scc-to-user privileged \
  -z node-exporter \
  -n observability



1860
https://grafana.com/grafana/dashboards/1860-node-exporter-full/

13332
https://grafana.com/grafana/dashboards/13332-kube-state-metrics-v2/


https://grafana.com/grafana/dashboards/
