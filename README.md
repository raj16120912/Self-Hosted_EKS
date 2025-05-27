**Setup instructions:**
```
git clone https://github.com/raj16120912/Self-Hosted_EKS.git
helm install webapp ./Self-Hosted_EKS/webapp
helm install minio bitnami/minio -n storage --create-namespace -f minio-values.yaml
```
**Architecture diagram:**
![Selfhosted-S3](https://github.com/user-attachments/assets/974fdc70-eb9d-4cab-af55-dbb809baaa38)

**Description of the design decisions:**
1. As mentioned in the task, deployed Gateway and Data-service, Auth-service in different namespace named system and app respectively.
2. Deployed minio using [bitnami/minio](https://artifacthub.io/packages/helm/bitnami/minio) helm chart and provided values from `minio-values.yaml` included in the repository.

Grafana Dashboard is also include in the repository.

**Incident:**
Deleted a pod to display a spike in grafana dashboard.
![Screenshot 2025-05-26 064557](https://github.com/user-attachments/assets/ac7dd166-c769-462d-85ba-54dee3450536)
![image](https://github.com/user-attachments/assets/acb268f0-ef30-4b78-bd3a-5306c9d48ba7)
