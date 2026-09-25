# ADR-001 — Complementar antes de substituir

**Status:** ACEITA  
**Data:** 2026-09-25

## Contexto

O projeto pretende atuar sobre um ecossistema público de saúde já utilizado e não deve depender da substituição imediata de sistemas oficiais.

## Decisão

O GovHealth Interop será construído inicialmente como **camada complementar e integradora**.

## Consequências

### Positivas

- menor escopo inicial;
- menor risco institucional;
- permite validar valor antes de substituir;
- possibilita coexistência;
- permite aproveitar interfaces existentes.

### Negativas

- dependência de sistemas externos;
- possíveis limitações de integração;
- necessidade de manter múltiplos adapters.

## Critério para revisão

A decisão pode ser revisada somente após evidência de:

- valor operacional;
- estabilidade;
- segurança;
- capacidade de integração;
- necessidade real de substituição.
