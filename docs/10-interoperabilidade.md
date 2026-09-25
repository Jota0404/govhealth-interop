# GovHealth Interop — Estratégia de Interoperabilidade

## 1. Hierarquia de preferência

A integração deve seguir esta ordem:

1. API oficial;
2. padrão oficial/documentado;
3. mecanismo oficial de sistema externo;
4. arquivo/integração formal;
5. automação de interface somente quando autorizada e necessária.

## 2. Adapters

Cada sistema recebe uma implementação própria.

```
IntegrationPort
   ├── EusAdapter
   ├── RndsAdapter
   ├── TrakCareAdapter
   ├── MvAdapter
   └── ...
```

## 3. Canonical Model

O GovHealth deve possuir um modelo interno independente.

Exemplo:

```
Citizen
Professional
HealthUnit
Encounter
Document
Observation
Appointment
```

Mapeamentos externos ficam fora do domínio.

## 4. Identidade

Um cidadão pode possuir identificadores diferentes em sistemas diferentes.

Nunca assumir:

```
CPF = ID externo universal
```

O sistema deve preservar:

- sistema de origem;
- identificador externo;
- tipo de identificador;
- data de sincronização.

## 5. Contratos

Cada adapter deve possuir:

- contrato;
- testes;
- tratamento de erros;
- timeout;
- retry controlado;
- observabilidade.

## 6. RNDS / FHIR

FHIR deve ser usado quando a integração aplicável o exigir e quando os recursos/perfis necessários estiverem oficialmente definidos.

Não modelar todo o produto em FHIR antes de existir necessidade real.

## 7. Automação por navegador

Playwright/browser automation não é arquitetura-base.

Quando inevitável e autorizado:

- isolar no adapter;
- nunca contaminar o domínio;
- não persistir credenciais indevidamente;
- registrar apenas informações operacionais necessárias;
- implementar detecção explícita de sucesso/falha.
