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
