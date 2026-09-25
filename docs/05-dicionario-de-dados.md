# GovHealth Interop — Dicionário de Dados

**Status:** inicial / sujeito à validação

| Entidade | Campo | Significado | Status |
|---|---|---|---|
| Organization | id | identificador interno | Conceitual |
| Organization | legal_name | nome oficial | Conceitual |
| HealthUnit | id | identificador interno | Conceitual |
| HealthUnit | cnes | CNES da unidade | Validar |
| User | id | identificador interno | Conceitual |
| Professional | cpf | CPF do profissional | Validar necessidade |
| Professional | cns | CNS do profissional | Validar |
| Citizen | id | identificador interno | Conceitual |
| Citizen | cpf | CPF do cidadão | Validar |
| Citizen | cns | CNS do cidadão | Validar |
| Encounter | id | identificador interno | Conceitual |
| Encounter | started_at | início do atendimento | Conceitual |
| ExternalSystem | code | identificador do sistema integrado | Conceitual |
| ExternalIdentity | external_id | identificador no sistema externo | Conceitual |
| IntegrationEvent | direction | entrada/saída | Conceitual |
| IntegrationEvent | status | estado da integração | Conceitual |
| AuditEvent | actor_id | usuário que executou ação | Conceitual |
| AuditEvent | occurred_at | data/hora | Conceitual |

## Regra

Nenhum campo será promovido a definitivo sem evidência do fluxo real ou documentação oficial.
