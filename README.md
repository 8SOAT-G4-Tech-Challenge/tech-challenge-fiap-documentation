## FIAP Tech-Challenge 8SOAT - Grupo 04

### Objetivo

Este projeto visa oferecer um sistema integrado de controle de pedidos para uma lanchonete em expansão. Por meio de um totem de autoatendimento, os clientes podem realizar seus pedidos, efetuar pagamentos e acompanhar o status em tempo real, otimizando o atendimento, reduzindo erros e aumentando a satisfação.

### Tecnologias Utilizadas
- **Node 20 e Typescript**: Backend
- **Prisma**: ORM
- **Fastify**: Framework web para Node
- **Jest**: Framework de testes
- **Docker**: Containerização da aplicação e gerenciamento de serviços
- **Kubernetes**: Orquestração de containers
- **Terraform**: Gerenciamento da infraestrutura na AWS
- **AWS Cloud**: Ambiente de nuvem para execução e deploy da aplicação
- **PostgreSQL**: Banco de Dados relacional
- **MongoDB**: Banco de Dados não relacional orientado a documentos
- **Redis**: Banco de Dados em memória para caching e otimização do desempenho.

### Fases
Abaixo estão detalhadas todas as fases do projeto, evidenciando sua evolução ao longo do tempo:

<details>
	<summary>
		<b>FASE 01 - DDD, Dockerização e Arquitetura de Software</b>
	</summary>

#### Requerimentos

- Node 20
- Docker / Docker Compose

#### Resumo

Na Fase 1, foi desenvolvida uma aplicação monolítica estruturada em uma arquitetura hexagonal, implementando uma API responsável por gerenciar produtos, pedidos e clientes. A aplicação foi containerizada utilizando Docker, configurada por meio de um Dockerfile e um docker-compose.yml.

#### Documentação

O projeto possui uma documentação completa, desenvolvida utilizando os conceitos de DDD, linguagem ubíqua e Event Storming, abrangendo os fluxos de realização do pedido, pagamento, preparação e entrega. Acesse [aqui](https://miro.com/app/board/uXjVK2WZuMs=/) a Documentação do Projeto. Também é possível visualizar a estrutura do banco de dados, acessando o [Diagrama ER](https://miro.com/app/board/uXjVK0gj0bg=/).

#### Execução

Para executar a aplicação da fase 1, siga a [Documentação de instalação](docs/fase1/INSTALACAO.md), que possui todos os passos para iniciar e executar a aplicação localmente.

</details>

<details>
	<summary>
		<b>FASE 02 - Kubernetes e Clean Architecture</b>
	</summary>

#### Requerimentos

- Node 20
- Docker / Docker Compose
- Kubernetes / KubeCTL

#### Resumo

Na Fase 2, o projeto foi evoluído adotando os princípios de Clean Code e Clean Architecture para aprimorar a qualidade do código. Foi implementado um webhook para receber confirmações de pagamento e, também, foi desenvolvida a parte de integração com o Mercado Pago, permitindo a geração de QRCodes para pagamento dos pedidos. Além disso, a aplicação foi migrada para uma arquitetura baseada em Kubernetes, garantindo escalabilidade dinâmica com o aumento e diminuição de Pods conforme a demanda. Para maiores detalhes de como a aplicação funcionará nessa fase, acesse o [Vídeo de Apresentação da Fase 2](https://www.youtube.com/watch?v=gasm0z2YOBg&ab_channel=JacksonAntunes).

#### Documentação

É possível visualizar e testar todos os endpoints [aqui](https://github.com/8SOAT-G4-Tech-Challenge/tech-challenge-bruno). Foi utilizada a API Client Bruno, uma alternativa ao Postman que permite que a documentação seja versionada através do GitHub.

#### Deploy

Para executar o deploy local da aplicação com Kubernetes da fase 2, siga a seguinte [documentação](docs/fase2/DEPLOY.md), que possui todos os passos para iniciar e executar a aplicação localmente.

#### Infraestrutura Local

![local](https://github.com/user-attachments/assets/77555751-c388-46b6-9e79-260dfd98e104)

#### Prévia de Infraestrutura de Cloud (To do)

![aws_cloud](https://github.com/user-attachments/assets/21b13369-caea-438a-ae8e-3ba085b4888e)

</details>

<details>
	<summary>
		<b>FASE 03 - Serverless, DevOps e Data Engineering </b>
	</summary>

#### Requerimentos

- Node 20
- Kubernetes / KubeCTL
- AWS CLI
- Terraform

#### Resumo
Na Fase 3, o projeto evoluiu com a implementação de práticas avançadas de CI/CD e a segregação do código em múltiplos repositórios, garantindo maior modularidade. Todos os repositórios realizam deploy automatizado na AWS utilizando GitHub Actions, com as branches main/master protegidas para que os commits sejam realizados apenas via pull request

Os repositórios são:

- **Repositório AWS Lambdas**: com funções lambda para autenticar clientes via CPF e usuários administradores. Clique [aqui](https://github.com/8SOAT-G4-Tech-Challenge/tech-challenge-lambdas) para acessar.
- **Repositório para infraestrutura Kubernetes com Terraform**: contém todo o mapeamento para a criação de todos os recursos de infraestrutura na AWS. Clique [aqui](https://github.com/8SOAT-G4-Tech-Challenge/tech-challenge-terraform) para acessar.
- **Repositório para infraestrutura de Banco de Dados com Terraform**: contém todo o mapeamento para a criação de todos os recursos de banco de dados, VPC e network e security group na AWS. Clique [aqui](https://github.com/8SOAT-G4-Tech-Challenge/tech-challenge-database) para acessar.
- **Repositório da Aplicação**: mantido o repositório da API executada no Kubernetes.
- **Repositório Bruno**: mantido o repositório que contém a documentação da API.

Para maiores detalhes de como a aplicação funcionará nessa fase, acesse o [Vídeo de Apresentação da Fase 3](https://www.youtube.com/watch?v=cCr7wOE1I6Y).

#### Infraestrutura de Cloud

[Desenho Arquitetura drawio](https://drive.google.com/file/d/1y7T1N6wRgpz-XEwMXWtzjVsCxz71yy1p/view?usp=sharing)

![Desenho Arquitetura drawio](https://github.com/user-attachments/assets/0f953ddc-52e4-4467-b566-e5f984addd6f)

#### Execução

Para executar a aplicação da fase 3, siga a seguinte [documentação](docs/fase3/EXECUCAO.md), que possui todos os passos para iniciar e executar a aplicação localmente.

</details>

<details>
	<summary>
		<b>FASE 04 - Microsserviços e Qualidade de Software</b>
	</summary>

Em andamento

</details>

### Participantes

- Amanda Maschio - RM 357734
- Jackson Antunes - RM357311
- Lucas Accurcio - RM 357142
- Vanessa Freitas - RM 357999
- Winderson Santos - RM 357315
