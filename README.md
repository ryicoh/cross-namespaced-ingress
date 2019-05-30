# cross-namespaced-ingress

## インストール方法
```
kubectl apply -f namespace/
kubectl apply -f development/ --record --prune -l=app=sample-web,stage=development
kubectl apply -f staging --record --prune -l=app=sample-web,stage=staging
kubectl apply -f production --record --prune -l=app=sample-web,stage=production
kubectl apply -f nginx-ingress/ --record --prune -l=group=nginx-ingress
```
