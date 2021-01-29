# Roadmap

## Source Code Management Integration

Integrar com os seguintes serviços:

- [x] Gitlab
- [ ] Github
- [ ] Aws CodeCommit
- [ ] Azure VSTS
- [ ] BitBucket

Requisitos:

- Ser um repositório GIT
- Possuir feature de MR
  - Desejavel integrar com as pipelines
- Possuir funcionalidade de Tags e Releases
- Possuir funcionalidade de Executores de Pipelines externos
- Possuir funcionalidade que permita rodar pipelines de multiplos destinos do Git, tais como branches, tags e merge_requests*. Configurações a mais sao diferenciais
- Possuir funcionalidade que permita o cliente sobrescrever scripts pré definidos do **PowerPipes**

### Executores de Pipelines e Jobs

- Utilizar estrutura de Pipes do SCM.
- Capacidade de usar Docker Images como executar de jobs das pipelines.
- Permitir integrar com serviços externos através de Imagens Docker.
- Catalogar as Imagens Docker que forem criadas pelas comunidades e serão chamadas de **PowerPipes Images**. 
  Essas imagens devem seguir um conjunto de regras de implementaçoes e utilizar a SDK do PowerPipes.
- SDK do PowerPipes para padronizar e agilizar integração com APIs.

## Clouds e Ferramentas similares

Integrar com as seguintes Clouds

- [ ] AWS
- [ ] Azure
- [ ] Google Cloud
- [ ] Kubernetes
- [ ] Heroku
 
## PowerPipes Funcionalidades

- Permitir configurar tipos de ambientes, sendo produtivos ou não
- Permitir configurar agrupadores de ambientes.
- Permitir configurar predecessão entre ambientes.
- Permitir configurar ambientes obrigatórios por estratégia de git (branches, tags, etc ..)
- Permitir configurar ambientes produtivos e nao produtivos, de maneira a utiliza-los na SDK pelas **PowerPipes Images**
- Permitir configurar credenciais, senhas, tokens e similares em cofres seguros e serem consumidos pelas **PowerPipes Images**
- Api para armazenar cache das **PowerPipes Images**.
- Api para consumo de informações sobre ambientes.

### Metricas e Dados

Apresentar dados sobre:

- [ ] Acelerate Devops
- [ ] DORA
- [ ] Perfornace de Pipelines
- [ ] Dados detalhados de repositórios
- [ ] Dados detalhados de deploys
- [ ] Dados detalhados de LeadTime
- [ ] Dados detalhados qualidade de software
- [ ] Dados detalhados segurança de software

### Plugins

- Permitir de forma padronizada de o cliente criar e plugar serviços externos nas pipelines (Golden Images)
  - Todo plugin deve ter documentação de Arquitetura (README.md) e para o Cliente (Docs)
  - Todo plugin deve gerar dados/métricas sobre o mesmo e ter um canal comum para publica-los através do serviço de pipelines
  - Todo plugin deve respeitar as regras de ambientes
- A plataforma deverá fornecer uma estrutura de APIs para conectar plugins externos
  - Todo plugin que for consumir senha, credencial, token ou informação de acesso a qualquer ferramenta de terceiros deve acontecer de forma segura e com contratos bem estabelecidos
  - Todo trafego de dados dos plugins devem acontecer de forma criptografada
- API para gerar dados de plugins
- API de consulta de os dados gerados por outros plugins da plataforma, podendo assim criar integraçao entre os plugins.
  - Somente dados do mesmo cliente podem ser consultados e do repositório da pipeline onde o plugin esta sendo executado
  - Todo trafego de dados dos plugins devem acontecer de forma criptografado

### CI

Considerado CI os seguintes jobs da pipeline:

- Lint
- Build
- Unit Test

Suporte e scripts pré-definidos para as seguintes linguagens

- [ ] Java: 6,7,8,11,13,14,15
  - gradle
  - maven
- [ ] Python: 2,3.x
- [ ] NodeJS: 4,10
- [ ] Kotlin
- [ ] .NetCore 2,3
- [ ] .NetFramework 4.5, 4.7, 4.8
- [ ] .Net 5
- [ ] Ruby
  - [ ] Rails
  - [ ] Sinatra
- [ ] C++
- [ ] C#

### PowerPipes Images pré-definidas

#### SAST

- [ ] SonarQube
- TODO: Definir opensources por tecnolgia/linguagen

#### DAST

- TODO: Definir opensources por tecnolgia/linguagen
- TODO: Definir privador por tecnolgia/linguagen

#### PUBLISH

- [ ] Nexus
- [ ] JFrog Artifactory

#### CD

- [ ] Kubernetes
- [ ] AWS Services
  - [ ] Lambda
  - [ ] ApiGateway
  - [ ] ECS
  - [ ] Beanstalk
  - [ ] S3

> TODO: Definir estratégias de deploy para as imagens pré definidas
  
#### Infra as Code

- [ ] Terraform
- [ ] Chef Privisioner
- [ ] Ansible
- [ ] SaltStack
