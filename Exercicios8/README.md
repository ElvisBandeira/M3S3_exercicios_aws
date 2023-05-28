## Exercicio 8.
## Observação:
- Todos os exercicios tem como base os exemplos citados em aula, e foram catalogados através de imagens, para futuras consultas em estudo.

## CI/CD
- É um acrônimo para integrar, entregar e implementar códigos de forma continua.
- Integração continua: integra código de diferentes desenvolvedoresem um repositório compartilhado.
- Entrega continua: garante que o código esteja pronto para ser implementado automaticamente.
- Implementação continua: envolve implementação automática do código, garantindo atualizações sem erros humanos.

## Pipeline
- São etapas que um código passa antes da implantação. No pipeline faz-se os testes e revisões de código, permitindo uma entrega rápida e eficiente do código.

## Pipeline de CI/CD com Github Actions: build, tag and push to ECR.
- Github Actions é a plataforma de trabalho integrada ao GitHub. Oferece ações para ajudar na automatização de tarefas comuns de CI/CD.
- Pode ser implementado para serviços em nuvem, execução de testes, notificando as equipes de trabalho sobre alterações no código.

### Deploy.yml
## Ação
- nome: Deploy to ECR
## workflow
- on:
- push:
- branches: [ main ]
- jobs:
-  build:    
-  nome: Build Image
-  runs-on: ubuntu-latest
-  steps:
-  nome: Check out code
-  uses: actions/checkout@v2
## credenciais AWS
- nome: Configure AWS credentials
- uses: aws-actions/configure-aws-credentials@v1
- with:
- aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
- aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
- aws-region: us-east-1
## ECR login
- nome: Login to Amazon ECR
- id: login-ecr
- uses: aws-actions/amazon-ecr-login@v1
## build, tag e push para ECR
- nome: Build, tag, and push image to Amazon ECR
- env:
- ECR_REGISTRY: ${{ steps.login-ecr.outputs.registry }}
- ECR_REPOSITORY: teste2
- IMAGE_TAG: teste2
- run: 
- docker build -t $ECR_REGISTRY/$ECR_REPOSITORY:$IMAGE_TAG .
- docker push $ECR_REGISTRY/$ECR_REPOSITORY:$IMAGE_TAG





