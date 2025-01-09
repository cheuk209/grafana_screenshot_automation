kubectl get secret grafana-admin -n grafana-monitoring -o jsonpath="{.data.GF_SECURITY_ADMIN_PASSWORD}" | base64 -d
Error from server (NotFound): secrets "grafana-admin" not found