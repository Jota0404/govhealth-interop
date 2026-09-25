# GovHealth Interop

**Plataforma de interoperabilidade, operação e apoio à gestão da saúde pública.**

**Status documental:** baseline 0.1 — pesquisa e definição inicial  
**Data:** 2026-09-25  
**Repositório:** Jota0404/govhealth-interop

## 1. Visão

O GovHealth Interop é um projeto paralelo ao **HealthCare System**. Não substitui aquele produto e não deve ser tratado como sua versão governamental.

A proposta é criar uma plataforma destinada à saúde pública, inicialmente concebida para **complementar e integrar-se ao ecossistema de sistemas já utilizado pelos órgãos de saúde**, com foco inicial no contexto do Distrito Federal.

A hipótese central é que existe valor em uma camada que reduza:

- fragmentação entre sistemas;
- redigitação e retrabalho;
- falta de visão operacional consolidada;
- dificuldade de acompanhar fluxos entre unidades;
- dificuldade de interoperabilidade;
- ausência de indicadores operacionais em tempo útil.

A plataforma deve começar resolvendo problemas verificáveis e poderá, somente após validação e requisitos formais, assumir funções hoje desempenhadas por módulos/sistemas existentes.

## 2. Relação com o E-Saúde / e-SUS

A documentação **não assume que “E-Saúde” seja um único produto técnico nacional**. No contexto deste projeto, o termo é uma referência ao ecossistema utilizado na saúde pública e aos sistemas que hoje participam da operação.

O projeto deverá identificar, antes do MVP definitivo:

- qual sistema específico o órgão-alvo chama de E-Saúde;
- quais módulos são usados;
- quais outros sistemas participam do fluxo;
- quais integrações são oficialmente suportadas;
- onde existe operação manual ou duplicada.

O e-SUS APS possui documentação oficial de integração com sistemas externos e disponibiliza mecanismos de contexto de cidadão, profissional e CNES. [Fonte oficial](https://sisaps.saude.gov.br/sistemas/esusaps/docs/manual/APOIO/Sistemas%20externos/).

## 3. Hipótese de produto

A primeira versão deve ser uma **camada de interoperabilidade + operação + gestão**, não um “novo e-SUS”.

Fluxo conceitual:

```
Sistemas existentes
   ├── e-SUS / e-SUS APS
   ├── TrakCare
   ├── MV / outros
   ├── Regulação
   └── demais sistemas locais
          │
          ▼
   GOVHEALTH INTEROP
          │
   ┌──────┼────────┐
   ▼      ▼        ▼
Operação Dados   Gestão
          │
          ▼
   RNDS / integrações
```

## 4. Princípio estratégico

**Complementar antes de substituir.**

O sistema oficial permanece sendo a referência institucional enquanto o GovHealth Interop comprova valor.

Evolução desejada:

```
Complementar
   ↓
Integrar
   ↓
Otimizar fluxos
   ↓
Assumir módulos específicos
   ↓
Possível substituição de partes
```

Qualquer substituição integral é uma hipótese futura, não requisito do MVP.

## 5. Documentação

| Documento | Objetivo |
|---|---|
| [01 — Visão e Escopo](./docs/01-visao-e-escopo.md) | problema, público, proposta e fronteiras |
| [02 — ERS](./docs/02-ers.md) | requisitos funcionais e não funcionais |
| [03 — DAS](./docs/03-das.md) | arquitetura e fronteiras |
| [04 — Modelo de Dados](./docs/04-modelo-de-dados.md) | entidades iniciais |
| [05 — Dicionário de Dados](./docs/05-dicionario-de-dados.md) | campos e significados |
| [06 — User Stories](./docs/06-user-stories.md) | histórias para backlog |
| [07 — Plano de Testes](./docs/07-plano-de-testes.md) | testes e aceitação |
| [08 — Lacunas e Evidências](./docs/08-lacunas-e-evidencias.md) | controle de incertezas |
| [09 — Pesquisa E-Saúde](./docs/09-pesquisa-e-saude.md) | pesquisa externa e evidências |
| [10 — Interoperabilidade](./docs/10-interoperabilidade.md) | estratégia de integração |
| [11 — Segurança e LGPD](./docs/11-seguranca-lgpd.md) | baseline de segurança |
| [12 — Roadmap](./docs/12-roadmap.md) | evolução por gates |
| [13 — Backlog](./docs/13-backlog.md) | prioridades |
| [14 — Riscos](./docs/14-riscos.md) | riscos técnicos/produto/comerciais |
| [15 — ADR-001](./docs/decisions/ADR-001-complementar-antes-de-substituir.md) | decisão de estratégia |
| [16 — ADR-002](./docs/decisions/ADR-002-adapters-por-sistema.md) | isolamento das integrações |

## 6. Regra documental

O projeto segue a filosofia do PCA-Auto:

1. evidência antes de conclusão;
2. hipóteses explicitamente marcadas;
3. decisões arquiteturais registradas;
4. integração externa isolada;
5. nenhum dado ou comportamento crítico inventado;
6. cada requisito importante deve possuir uma fonte ou decisão rastreável.

## 7. Relação com o HealthCare System

O HealthCare System privado continua sendo um projeto independente.

O GovHealth Interop pode reutilizar **conceitos, padrões e aprendizados técnicos**, mas possui:

- domínio próprio;
- usuários próprios;
- requisitos próprios;
- integrações próprias;
- modelo de dados próprio;
- estratégia comercial própria.

## 8. Próximo gate

O próximo gate não é “começar a programar”.

É comprovar:

- sistema-alvo real;
- processos afetados;
- usuários;
- dados disponíveis;
- integração possível;
- principal gargalo;
- métrica de sucesso.
