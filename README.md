# Deploy kubernetes apps

## create external api

```bash
gcloud compute addresses create hispanie-ip --global
```

## Run configuration

```bash
kubectl apply -f postgres-deployment.yaml
kubectl apply -f backend-deployment.yaml
kubectl apply -f frontend-deployment.yaml

kubectl apply -f postgres-service.yaml
kubectl apply -f backend-service.yaml
kubectl apply -f frontend-service.yaml

kubectl apply -f certificates.yaml
kubectl apply -f ingress.yaml
```

## Check cluster

```bash
kubectl get deploy,svc,po,ingress
```

## Delete all configuration

```bash
kubectl delete -f postgres-deployment.yaml
kubectl delete -f backend-deployment.yaml
kubectl delete -f frontend-deployment.yaml

kubectl delete -f postgres-service.yaml
kubectl delete -f backend-service.yaml
kubectl delete -f frontend-service.yaml

kubectl delete -f certificates.yaml
kubectl delete -f ingress.yaml
```

## Basic architecture diagram

![diagram](images/hispanie_architecture_diagram.png)
