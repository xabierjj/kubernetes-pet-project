# Kubernetes Pet project
This project demonstrates a basic web application connected to MongoDB using Kubernetes resources like Deployments, Services, Secrets, and ConfigMaps.

## Commands 

### 1. Start Minikube

```
minikube start
```

### 2. Apply resources
```
kubectl apply -f mongo-secret.yaml
kubectl apply -f mongo-config.yaml
kubectl apply -f mongo-deployment.yaml
kubectl apply -f mongo-service.yaml
kubectl apply -f webapp-deployment.yaml
kubectl apply -f webapp-service.yaml

```

### 3. Verify resources
```
kubectl get all
```

### Access Web App
This doesn't work if you're running Minikube with the QEMU driver on macOS (especially Apple Silicon), the following command will not work:
```
minikube service webapp-service
```

Instead, use kubectl port-forward:

```
kubectl port-forward service/webapp-service 3000:3000
```