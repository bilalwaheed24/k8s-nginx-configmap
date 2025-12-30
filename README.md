# Kubernetes Project 2: ConfigMap + Nginx

## Objective
Deploy a custom Nginx HTML page on Kubernetes using ConfigMap. Learn how to separate configuration from code.

## Steps
1. Start Minikube
2. Apply ConfigMap
3. Apply Deployment
4. Apply Service
5. Access Nginx via browser
6. Optional: Clean up

## Commands
```bash
# Start Minikube
minikube start

# Apply ConfigMap
kubectl apply -f configmap.yaml

# Apply Deployment
kubectl apply -f deployment.yaml

# Apply Service
kubectl apply -f service.yaml

# Check status
kubectl get pods
kubectl get configmap
kubectl get svc

# Access in browser
minikube service web
# OR
kubectl port-forward service/web 8080:80
# Then open http://localhost:8080

# Optional Clean up
kubectl delete -f .
