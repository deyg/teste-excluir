
Tasks

Slice 0
- Criar projeto com nome HDIinsurance no SpringBoot no STS. Utilizar Spring Web, Lombok (@Data, @AllArgsConstructor), SpringWebFlux (consumidor WebClient), Java 8, DevTools.
- Instalar Lombok na IDE
- Criar Packages: com.hdi.insurance.api.model, com.hdi.insurance.api.service, com.hdi.insurance.api.resource  com.hdi.insurance.api.exception

Slice 1
- Criar model Broker (Corretor) contendo os (6) atributos dos dois serviços referidos neste documento.  Atributos name  document  code  createDate  active  commissionRate
-* Criar service BrokerService para consumir as duas APIs referidas realizando o mashup dos dados através da lib WebClient do Spring. (obter corretor por documento e usando o código retornado obter detalhes por código). Se o correto não estiver ativo lançar exception.
- Criar controller para expor os dados da nova API, contendo o método @GetMapping("/{document}") ResponseEntity<Broker> getBroker(documento)
Mapeamento da classe @RequestMapping (“/insurance/v1/broker”) BrokerController
- Teste Postman: localhost:8080/insurance/v1/broker/52225508003 

Slice 2
- Adicionar a service método de atualizacao de status do broker
- Adicionar a controller um Put para atualizar o status do broker (brokerData)
- Criado BrokerDetails para corrigir atualização do status

Slice 3
- Adicionar dependencias do Swegger no POM.
- Criar package com.hdi.insurance.api.config e adicionar classe de configuração
- Documentar a API com Swegger 2 (OpenAPI)
- Acesso em: http://localhost:8080/swagger-ui.html

Slice 4
- Disponibilizar Codigo no Github
