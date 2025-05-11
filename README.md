# Kubernetes Pet project
This project demonstrates a basic web application connected to MongoDB using Kubernetes resources like Deployments, Services, Secrets, and ConfigMaps.

## Commands 

### 1. Start Minikube

```
minikube start --driver=docker
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

### 3. Check Resource Status
```
kubectl get all
```

### Access Web App
If using the Docker driver, you can open the service in your browser:

```
minikube service webapp-service
```


### Load image to minikube
```
minikube image load <image name>
```

### Delete all resources

```
kubectl delete all --all
```

### Restart 

```
kubectl rollout restart deployment/<deployment-name>
```

### Get pod logs

````
kubectl logs <pod name>

```

