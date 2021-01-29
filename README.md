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

- Capacidade de usar Docker Images como executar de jobs das pipelines
- Permitir integrar com serviços externos através de Imagens Docker
- Catalogar as Imagens Docker que forem criadas pelas comunidades e serão chamadas de **PowerPipes Images**. 
  Essas imagens devem seguir um conjunto de regras de implementaçoes e utilizar a SDK do PowerPipes.

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
- Api para consumo de informações sobre ambientes.

