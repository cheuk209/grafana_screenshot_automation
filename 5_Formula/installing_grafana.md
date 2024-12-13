

🎯 **Summary: Installing Grafana with Bitnami Helm Chart**

🚀 **Quick Install Steps**
- `helm repo add bitnami https://charts.bitnami.com/bitnami` // Add Bitnami repo
- `helm repo update` // Get latest charts
- `kubectl create namespace grafana-monitoring` // Create namespace
- `helm install grafana bitnami/grafana --namespace grafana-monitoring` // Install Grafana

🔑 **Access Setup**
- `kubectl get secret grafana-admin -n grafana-monitoring -o jsonpath="{.data.GF_SECURITY_ADMIN_PASSWORD}" | base64 -d` // Get admin password
- `minikube ip` // Get access URL
- Access via: `http://<minikube-ip>:30300` // Default port

⚙️ **Optional Configuration (values.yaml)**
```yaml
admin:
  user: admin
  password: your-password

persistence:
  enabled: true
  size: 10Gi

service:
  type: NodePort
  nodePorts:
    grafana: 30300

metrics:
  enabled: true
```

🔍 **Verification**
- `kubectl get pods -n monitoring` // Check pod status
- `kubectl get svc -n monitoring` // Check service status

Would you like me to help with dashboard setup or data source configuration? 🤔


prompt:
- Hello can I use helm and bitnami to install grafana instead?
- Create a summary
- Use emojis
- Use succinct, one-line comment
- Eliminate duplicate information