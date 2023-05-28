## Exercicios 4 ao 7
## Observação:
- Todos os exercicios tem como base os exemplos citados em aula, e foram catalogados através de imagens, para futuras consultas em estudo.

## Docker.
- Docker_Host: servidor que executa tudo o que acontece com os containers.
- Imagem: refere-se a uma instrução a ser executada "container".
- Dockerfile da as intruções para o Docker fazer a build e criar a imagem.
- DockerHub é uma registro de imagens Docker,onde se armazena, compartilha e gerencia imagens.

## Subindo imagem docker para AWS ECR.
- O ECR guarda as imagens docker.
- Deve-se criar um repositório na AWS, para a imagem Docker, depois de criado o repositório AWS CLI, faz o push da imagem.
- Ao fazer o push da imagem para o ECR, a uma disponibilização da aplicação do ambiente de DEV para Operação.
- para rodar a imagem no servidor precisa-se fazer a comunicação entre o ECR e o EC2.

## EC2.
- é ums serviço de computação em nuvem, onde pode-se criar e executar maquinas virtuais, oferecendo instancias para atender diferentes cargas de trabalho por meio da AWS, onde são processadas as informações.
- Lembre-se de desligar sua máquina EC2 (stop/parar).

## Gerenciamento de acesso.
- Cria-se uma politica na AWS (IAM), que é uma concessão de acesso entre AWS ECR e AWS EC2, o IAM é a permição para o funcionamento entre as duas aplicações ACR e EC2.
Função IAM é uma identidade com permissões validas por curtos periodos. 


 


