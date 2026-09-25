# ADR-002 — Adapter por sistema externo

**Status:** ACEITA  
**Data:** 2026-09-25

## Contexto

O ecossistema de saúde pública pode envolver múltiplos sistemas com APIs, autenticação, formatos e limitações diferentes.

## Decisão

Cada integração externa será isolada em um adapter.

## Consequências

O domínio não dependerá diretamente de:

- HTTP;
- DOM;
- APIs específicas;
- Playwright;
- contratos externos.

Isso permite substituir uma implementação de integração sem reescrever a lógica central do produto.

## Regra

Uma integração nova deve ter:

- contrato;
- testes;
- logs;
- tratamento de erro;
- documentação;
- estratégia de versionamento.
