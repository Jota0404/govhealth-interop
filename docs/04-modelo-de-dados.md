# GovHealth Interop — Modelo de Dados

**Status:** CONCEITUAL / NÃO FINAL

O modelo abaixo existe para guiar a investigação. Não deve ser convertido diretamente em schema de produção.

## Entidades iniciais

### Organization

Órgão/ente responsável pelo ambiente.

### HealthUnit

Unidade de saúde.

### User

Usuário autenticado.

### Professional

Profissional de saúde/servidor.

### Citizen

Cidadão/paciente.

### Encounter

Atendimento/evento assistencial.

### ExternalSystem

Sistema integrado.

### ExternalIdentity

Identidade do cidadão/profissional/unidade em um sistema externo.

### IntegrationEvent

Evento de comunicação com sistema externo.

### Task

Pendência ou tarefa operacional.

### AuditEvent

Evento de auditoria.

### DashboardMetric

Métrica agregada.

## Relacionamentos

```
Organization
    │
    └── HealthUnit
           │
           ├── User
           ├── Professional
           └── Encounter
                  │
                  └── Citizen

ExternalSystem
    │
    └── ExternalIdentity

Encounter
    └── IntegrationEvent

User
    └── AuditEvent
```

## Princípios

1. IDs externos não substituem IDs internos.
2. Origem do dado deve ser preservada.
3. Dados de saúde devem possuir escopo e autorização explícitos.
4. Integrações devem ser rastreáveis.
5. O modelo deve ser capaz de representar múltiplos sistemas para o mesmo cidadão.
