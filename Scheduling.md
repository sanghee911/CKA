#65. Resource Requirements and Limits
Containers default resource request
- cpu: 0.5
- memory: 256 Mi

Containers default resource limits
- cpu: 1
- memory: 512 Mi

Containers minimum resource request
- cpu: 0.1 or 100m
- memory: 

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: frontend
spec:
  containers:
  - name: app
    image: images.my-company.example/app:v4
    resources:
      requests:
        memory: "64Mi"
        cpu: "250m"
      limits:
        memory: "128Mi"
        cpu: "500m"
  - name: log-aggregator
    image: images.my-company.example/log-aggregator:v6
    resources:
      requests:
        memory: "64Mi"
        cpu: "250m"
      limits:
        memory: "128Mi"
        cpu: "500m"
```
