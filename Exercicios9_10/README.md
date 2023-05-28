## Exercicios 9 ao 10.
## Observção:
- Todos os exercicios tem como base os exemplos citados em aula, e foram catalogados através de imagens, para futuras consultas em estudo.

## Escalabilidade
- São aplicações que respondem demandas, ou seja, aumento ou diminuição de carga de trabalho sem comprometer desempenhos.
- Trabalha em duas estrategias, uma vertical que aumenta a capacidade computacional, e outra horizontal que aumenta a quantidade de servidores.

### Amazon ECS
- ECS é um gerenciador de containers em nuvem, sem a necessidade de gerenciar infraestrutura adjacente.
- Cluster é uma grupo de instancias do Amazon EC2 ou ambiente serveless que executam containers gerenciados pelo ECS.

### Kubernetes (minikube)
- plataforma open-source, que permite gerenciar aplicativos em ambientes de nuvem e datacenters.
- Deve-se fazer as instalações do minikube para rodar o kubernetes na maquina local.
- Kubectl precisa ser instalado para uso do kubernetes na cloud para poder se comunicar com o cluster.
- Usamos um projeto local para rodar dentro de um cluster kubernetes, sendo que antes ativamos os addons no minikube.
- Para executar um container no kubernetes, chama o kubecte e coloca o nome da imagem.

   

