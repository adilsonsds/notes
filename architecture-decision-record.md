# Architecture Decision Record

Documentação e templates disponíveis em [https://adr.github.io/](https://adr.github.io/)

Anotações:

* Arquivos podem ter uma numeração de 4 dígitos para facilitar a organização.
* Ter uma data é importante para formar um contexto.
* Deve ser um documento curto e objetivo. Nada muito extenso.
* Importante colocar uma data para colocar um contexto.
* Ideal que, caso uma ADR venha a ser substituída ou alterada, que que contenha o link para a nova ADR para manter a rastreabilidade.

# Architecture Decision Record Template by Michael Nygard

Template baseado no artigo [Documenting Architcecture Decisions - Michael 
Nygard](https://github.com/joelparkerhenderson/architecture-decision-record/tree/main/locales/en/templates)

## Title

Contém uma breve frase sobre a decisão a ser tomada.  Exemplo: `Escolha por um Message Broker.`

O título pode conter o que foi decidido. Pegando o exemplo anterior, caso tenha sido optado por RabbitMQ, o título poderia ser: `RabbitMQ como solução de Messa Broker.`

Data pode ser colocada no título.

## Status

Em que pé está a decisão. Exemplos: proposta, aceita, rejeitada, depreciada, substituída, etc.

## Context

Pontos importantes que podem ser descritos:

* O que estava acontecendo no momento?
* Qual era a situação?
* Em que momento do projeto estava?
* Qual problema que tinha que resolver?
* Quais eram as motivações?

## Decision 

Quais eram as opções e o que foi decidido.

## Consequences

O que vai se tornar mais fácil ou mais difícil, bom ou ruim, prós ou contras, etc.
