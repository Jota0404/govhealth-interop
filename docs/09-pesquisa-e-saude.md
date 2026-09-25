# Pesquisa — E-Saúde / e-SUS / Saúde Digital no DF

**Data da pesquisa:** 2026-09-25

## 1. Contexto importante

“E-Saúde” não deve ser tratado neste projeto como sinônimo automático de um único sistema nacional.

O ecossistema público possui diferentes sistemas e níveis de atenção. O e-SUS APS é um sistema específico da Atenção Primária e possui documentação própria de integração.

Fonte oficial:
https://sisaps.saude.gov.br/sistemas/esusaps/docs/manual/PEC/

## 2. Interoperabilidade do e-SUS APS

O manual oficial documenta o cadastro de **Sistemas Externos** e permite disponibilizar esses sistemas dentro do PEC.

O manual também descreve parâmetros de contexto para o sistema externo, incluindo identificador do cidadão, identificador do profissional e CNES do estabelecimento.

Fonte:
https://sisaps.saude.gov.br/sistemas/esusaps/docs/manual/APOIO/Sistemas%20externos/

### Implicação para o projeto

Existe uma superfície oficialmente documentada que pode ser estudada para uma experiência integrada, sem assumir acesso irrestrito ao banco ou às APIs internas do e-SUS.

## 3. Fragmentação no DF

Documento da SES-DF registra reclamações sobre:

- sistemas pouco amigáveis;
- necessidade de redigitação;
- falta de integração;
- falta de interoperabilidade;
- poucos recursos de gestão.

O mesmo documento registra iniciativas de integração entre sistemas da rede.

Fonte:
https://www.saude.df.gov.br/documents/37101/824400/Plano%2BDiretor%2Bde%2BTecnologia%2Bda%2BInforma%C3%A7%C3%A3o%2B2019%2B%E2%80%93%2B2022.pdf/

## 4. Integração de prontuários como demanda institucional

Em 22/04/2026, a CLDF disponibilizou a IND 10246/2026, cuja ementa sugere medidas para planejar e executar integração completa e unificada dos sistemas de prontuários eletrônicos da rede assistencial do DF, abrangendo SES-DF e IGES-DF.

Fonte:
https://www.cl.df.gov.br/proposicao/-/documentos/IND_10246_2026

A justificativa da proposição deve ser tratada como **posição/justificativa apresentada na proposição**, não como estudo independente.

## 5. Diversidade de sistemas

Fontes da própria SES-DF demonstram a coexistência de sistemas como:

- TrakCare;
- e-SUS;
- SISLeitos;
- sistemas laboratoriais;
- sistemas regulatórios.

Isso reforça a hipótese de que o projeto deve ser pensado como camada de interoperabilidade e operação, e não somente como substituto de um único software.

## 6. RNDS

A RNDS é a infraestrutura nacional de interoperabilidade do Ministério da Saúde e utiliza padrões de interoperabilidade, incluindo HL7 FHIR em sua arquitetura.

Fonte oficial:
https://www.gov.br/saude/pt-br/composicao/seidigi/rnds/estrutura-do-projeto

## 7. O que a pesquisa ainda não prova

A pesquisa pública não determina:

- qual fluxo é mais doloroso na unidade piloto;
- qual funcionalidade deve ser o MVP;
- quais APIs estarão disponíveis ao produto;
- quais permissões o órgão concederá;
- qual é o custo do problema;
- qual sistema poderá ou não ser substituído.

Esses pontos precisam de validação de campo.

## 8. Conclusão operacional

A evidência atual sustenta uma hipótese inicial:

> **O GovHealth Interop deve começar como uma camada de integração/contexto/operação sobre um ecossistema fragmentado, usando interfaces oficialmente suportadas sempre que possível.**

A hipótese será aceita ou rejeitada durante a validação do primeiro ambiente real.
