# Resource Order Infra

O Ingress do Nginx no Kubernetes atua como API Gateway expondo externamente as APIs do sistema.

O MongoDB é utilizado para persistir dados.

Para habilitar o monitoramento da infraestrutura instale o objeto ingress-monitoring.yaml e também os que estão no diretório grafana e prometheus.


```
kubectl apply -f ingress.yaml 
kubectl apply -f mongodb-configmap.yaml 
kubectl apply -f mondodb-secret.yaml 
kubectl apply -f mongodb-deployment.yaml 
kubectl apply -f serviceaccount-rbac.yaml
kubectl apply -f elastic.yaml
kubectl apply -f kibana.yaml
kubectl apply -f fluentd-rbac.yaml
kubectl apply -f fluentd-daemonset.yaml
```

