# k3d Deployment Runbook

## 1) Build local image
```bash
docker build -f web/Dockerfile -t ghcr.io/neil795/neil-sinha-it-portfolio:local .
```

## 2) Import image into k3d cluster
```bash
k3d image import -c chat-erp ghcr.io/neil795/neil-sinha-it-portfolio:local
```

## 3) Apply manifests
```bash
kubectl apply -f deploy/k8s/namespace.yaml
kubectl apply -f deploy/k8s/deployment.yaml
kubectl apply -f deploy/k8s/service.yaml
```

## 4) Verify readiness
```bash
kubectl -n neil-portfolio rollout status deploy/neil-portfolio-web
kubectl -n neil-portfolio get pods,svc
```

## 5) Port-forward and smoke test
```bash
kubectl -n neil-portfolio port-forward svc/neil-portfolio-web 18081:8080
curl -s http://127.0.0.1:18081/ | grep -q "Neil Sinha" && echo "SMOKE_OK"
```
