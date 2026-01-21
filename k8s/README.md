# Kubernetes Manifests - FCG Fase 2

Este diretório contém os manifestos Kubernetes exigidos pelo checklist do professor.

## O que existe aqui
- Deployments (obrigatório): para gerenciar os Pods.
- Services (obrigatório): para comunicação interna via nome do Service.
- ConfigMap (obrigatório): configurações não sensíveis (nomes de filas, host do broker, URLs internas).
- Secret (obrigatório): dados sensíveis (RabbitMQ user/pass, JWT secret, connection strings).

## Aplicar no cluster
A partir da raiz do repositório (onde existe a pasta `k8s/`):

```bash
kubectl apply -f k8s/
kubectl get pods
kubectl get svc
