# GovHealth Interop — Visão e Escopo

**Versão:** 0.1  
**Status:** baseline de pesquisa  
**Data:** 2026-09-25

## 1. Objetivo

Criar uma plataforma GovTech de apoio à operação e interoperabilidade da saúde pública, inicialmente orientada ao contexto do Distrito Federal.

O produto deverá funcionar ao lado dos sistemas oficiais existentes e reduzir problemas operacionais comprovados.

## 2. Problema

A documentação pública da SES-DF registra historicamente problemas de integração e interoperabilidade entre sistemas. Um documento da SES-DF registra, por exemplo, reclamações sobre falta de integração/interoperabilidade em sistemas de saúde e necessidade de integração entre TrakCare, MVSoul e e-SUS.

Em 2026, a CLDF também publicou proposição sugerindo integração completa e unificada dos sistemas de prontuários eletrônicos em toda a rede assistencial do DF, abrangendo SES-DF e IGES-DF.

Essas fontes demonstram que **integração e comunicação entre sistemas são problemas institucionais relevantes**, mas não provam sozinhas a magnitude de cada problema para todas as unidades.

## 3. Público-alvo inicial

### Operacional

- profissionais de saúde;
- enfermagem;
- recepção/apoio;
- equipes administrativas das unidades.

### Gestão

- gestores de unidade;
- coordenações;
- gestores regionais;
- secretaria.

### Técnico

- equipes de TI;
- responsáveis por integração;
- administração de sistemas.

## 4. Escopo inicial

### Incluído

- contexto unificado do atendimento;
- navegação entre sistemas;
- interoperabilidade;
- visão operacional;
- dashboards;
- filas e pendências;
- rastreabilidade;
- auditoria;
- integração com sistemas existentes;
- integração com padrões de interoperabilidade quando aplicável.

### Não incluído inicialmente

- substituir integralmente o e-SUS;
- substituir toda a rede de sistemas da SES;
- criar um ERP hospitalar;
- assumir todos os fluxos de regulação;
- criar prontuário universal antes da validação;
- IA clínica autônoma;
- diagnóstico automatizado;
- decisões clínicas automatizadas;
- dezenas de integrações sem demanda comprovada.

## 5. Proposta de valor inicial

O produto deve reduzir a distância entre:

**profissional → sistema → informação → decisão operacional.**

Exemplo conceitual:

```
Profissional inicia atendimento
        ↓
GovHealth identifica contexto
        ↓
Recupera contexto autorizado
        ↓
Apresenta informações necessárias
        ↓
Permite executar fluxo
        ↓
Registra resultado
        ↓
Sincroniza / envia dados conforme integração suportada
```

## 6. Critério de sucesso

O MVP só deve ser considerado validado quando houver comparação mensurável entre processo atual e processo com GovHealth.

Indicadores possíveis:

- tempo por atendimento/fluxo;
- quantidade de sistemas abertos;
- quantidade de redigitações;
- erros;
- retrabalho;
- tempo para localizar informação;
- tempo de fechamento do atendimento;
- pendências administrativas;
- satisfação operacional.

Os indicadores definitivos dependem da unidade piloto.

## 7. Fronteira

O GovHealth é uma **camada de produto independente**, não uma cópia do e-SUS.

Sua capacidade de substituir funcionalidades deve ser consequência de validação, interoperabilidade e requisitos formais.
