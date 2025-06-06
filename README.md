# Projeto conversão de temperatura

### Sobre o projeto
O projeto conversão de temperatura é um projeto desenvolvido em NodeJS. O projeto tem como objetivo ser um exemplo para a criação de ambiente com containers usando NodeJS.

### Observações do projeto
A aplicação é exposta usando a porta 8080

Caso queira realizar um build de imagem personalizada, você precisará alterar a imagem selecionada no arquivo `k8s/deployment.yaml`.

### Rodar com o Kubernetes

Criar um cluster com o **k3d**
```bash
k3d cluster create meucluster --servers 3 --agents 3 -p "30000:30000@loadbalancer"
```

Aplicar configurações do cluster Kubernetes
```bash
kubectl apply -f k8s/deployment.yaml
```