# maratona-devops-ia

Link para ter $ 200 na Digital Ocean

https://m.do.co/c/a939ecc60dfa


# Estrutura Inicial

```yaml
name: CI-CD

on:
  push:
    branches: [ "main" ]
  workflow_dispatch:

jobs:
    CI:
        runs-on: ubuntu-latest
        steps:
            - run: echo "Obter o código"
            - run: echo "Executar o Docker Build"
            - run: echo "Enviar a Imagem Docker para o Docker Hub"

    CD:
        runs-on: ubuntu-latest
        
        steps:
            - run: echo "Obter o código"
            - run: echo "Configurar o Kubeconfig"
            - run: echo "Executar o apply"
```        


# Grafana

Obter a senha do admin
```        
kubectl get secret --namespace default grafana -o jsonpath="{.data.admin-password}" | base64 --decode ; echo
```        