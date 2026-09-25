# GovHealth Interop — Documento de Arquitetura de Software

**Versão:** 0.1  
**Status:** arquitetura conceitual

## 1. Princípio

A arquitetura deve proteger o domínio contra detalhes específicos de cada sistema governamental.

## 2. Arquitetura lógica

```
                    Usuário Web
                        │
                      HTTPS
                        ▼
                ┌────────────────┐
                │ Presentation   │
                └───────┬────────┘
                        ▼
                ┌────────────────┐
                │ Application    │
                │ Use Cases      │
                └───────┬────────┘
                        ▼
                ┌────────────────┐
                │ Domain         │
                │ regras/estado  │
                └───┬────────┬───┘
                    │        │
          ┌─────────┘        └─────────┐
          ▼                            ▼
   PostgreSQL                  Integration Layer
                                      │
                     ┌────────────────┼───────────────┐
                     ▼                ▼               ▼
                  e-SUS           TrakCare         Outros
```

## 3. Camadas

### Domain

Não conhece:

- navegador;
- HTTP;
- Playwright;
- PostgreSQL;
- APIs de terceiros.

### Application

Orquestra:

- autenticação;
- contexto;
- consulta;
- consolidação;
- execução;
- auditoria.

### Infrastructure

Implementa:

- PostgreSQL;
- HTTP;
- APIs;
- adapters;
- armazenamento;
- observabilidade.

### Integration

Cada sistema externo possui adapter próprio.

Exemplo:

```
EusAdapter
TrakCareAdapter
MvAdapter
RndsAdapter
RegulationAdapter
```

Os nomes são conceituais até que os sistemas do piloto sejam confirmados.

## 4. Regra de integração

Nenhum caso de uso deve conhecer:

- URL específica;
- endpoint específico;
- nome de campo específico;
- seletor DOM;
- cookie;
- token de sistema externo.

Esses detalhes pertencem ao adapter.

## 5. Estratégia de implantação

Começar como modular monolith é a hipótese preferida para o MVP, porque reduz complexidade operacional.

Microserviços somente quando houver justificativa real de escala, isolamento ou integração.

## 6. Banco

PostgreSQL é a hipótese inicial.

O modelo definitivo será criado somente após o primeiro fluxo real ser mapeado.

## 7. Interoperabilidade

A arquitetura deve suportar tanto:

- APIs;
- padrões de interoperabilidade;
- mecanismos de contexto fornecidos pelos próprios sistemas;

quanto mecanismos de integração legados, quando houver autorização e necessidade.

Automação por interface deve ser exceção e não premissa arquitetural.
