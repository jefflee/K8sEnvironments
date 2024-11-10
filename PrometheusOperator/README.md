Follow by these sequestion to create a Prometheus Operator in local Kubernetes.

1. Install Prometheus operator
```
kubectl create -f bundle.yaml
```

2. Apply prometheus_instance.yaml for Prometheus instance
    - Test Prometheus URL: http://localhost:30000/ 
```
kubectl apply -f prometheus_instance.yaml
```

3. Apply prometheus_rbac.yaml for RBAC

```
kubectl apply -f prometheus_rbac.yaml
```

4. Apply prometheus_test_app.yaml 
    - Test APP URL: http://localhost:30080/metrics 

```
kubectl apply -f prometheus_test_app.yaml
```

5. Apply prometheus_rules.yaml 
```
kubectl apply -f prometheus_rules.yaml
```

Enjoy!