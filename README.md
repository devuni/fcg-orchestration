# fcg-orchestration
# FCG – Fase 2 (Orquestração)

Este repositório é o **ponto de entrada** para subir e demonstrar o sistema completo da Fase 2:
- **Users API** (cadastro + autenticação JWT; publica `UserCreatedEvent`)
- **Catalog API** (CRUD de jogos + inicia compra; publica `OrderPlacedEvent`; consome `PaymentProcessedEvent`)
- **Payments API** (consome `OrderPlacedEvent`; publica `PaymentProcessedEvent`)
- **Notifications API** (consome eventos e simula e-mails via log no console)

A integração entre serviços é orientada a eventos via **RabbitMQ**.

---

## Pré-requisitos
- Docker + Docker Compose (v2)
- kubectl
- Um cluster Kubernetes local (Kind / Minikube / k3d / Docker Desktop Kubernetes)

---

## Estrutura esperada (multi-repo)
Para rodar com `docker compose up --build`, este repositório espera ter os microsserviços disponíveis em pastas com estes nomes:

