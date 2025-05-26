Setup instructions:
```
git clone <>
helm install webapp ./webapp
helm install minio -f minio_values.yaml -n storage --create-namespace
helm install prometheus
```
Architecture diagram:
![Selfhosted-S3](https://github.com/user-attachments/assets/974fdc70-eb9d-4cab-af55-dbb809baaa38)


Description of your design decisions

Explanation of the security incident & how you fixed it
Any assumptions or known issues


Code:
Helm charts or Kustomize manifests
YAML configs for Deployments, Services, NetworkPolicies, Secrets
OPA/Kyverno/Falco policy files (if used)
Dockerfiles if you modified anything (optional)
Exported Grafana dashboards (as JSON)
