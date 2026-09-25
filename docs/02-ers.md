# GovHealth Interop — Especificação de Requisitos de Software

**Versão:** 0.1  
**Status:** baseline inicial — requisitos sujeitos à validação com unidade piloto

## 1. Requisitos funcionais

### RF-001 — Identificar contexto do usuário

O sistema deve identificar, de acordo com as credenciais e permissões, o profissional, unidade e contexto operacional aplicáveis.

### RF-002 — Consolidar contexto assistencial

O sistema deve apresentar, quando permitido, uma visão consolidada das informações disponíveis para o fluxo selecionado.

### RF-003 — Navegar para sistema externo

O sistema deve permitir acesso contextual a sistemas externos compatíveis com o fluxo.

### RF-004 — Interoperar com sistemas externos

A integração deve ser implementada por adapters independentes por sistema.

### RF-005 — Preservar origem

Todo dado externo deve manter sua origem, identificador e momento de obtenção quando essas informações forem relevantes para auditoria.

### RF-006 — Registrar eventos

O sistema deve registrar eventos de consulta, integração, envio, falha e retorno.

### RF-007 — Exibir pendências

O usuário deve conseguir identificar pendências operacionais e a origem de cada uma.

### RF-008 — Dashboard operacional

O sistema deve fornecer indicadores operacionais de acordo com o perfil de acesso.

### RF-009 — Auditoria

Ações relevantes devem registrar usuário, unidade, horário, recurso e resultado.

### RF-010 — Falha explícita

Falhas de integração não devem ser silenciosamente tratadas como sucesso.

### RF-011 — Modo de diagnóstico

Deve existir modo controlado para validar uma integração sem modificar dados de produção, quando tecnicamente possível.

### RF-012 — Retomada

Operações interrompidas devem ter estado suficiente para serem retomadas sem duplicar operações comprovadamente concluídas.

### RF-013 — Exportação

O sistema deve permitir exportação de dados operacionais conforme requisitos autorizados e contrato.

### RF-014 — Controle de acesso

O acesso deve respeitar função, unidade, vínculo institucional e escopo do usuário.

## 2. Requisitos não funcionais

### RNF-001 — Segurança

Segredos não podem ficar no código.

### RNF-002 — Auditabilidade

Ações sensíveis devem possuir trilha de auditoria.

### RNF-003 — Interoperabilidade

Integrações devem preferir padrões documentados e APIs oficiais quando disponíveis.

### RNF-004 — Resiliência

Uma falha de integração externa não deve indisponibilizar desnecessariamente as funcionalidades internas.

### RNF-005 — Observabilidade

Falhas devem permitir diagnóstico por sistema, unidade, fluxo e período.

### RNF-006 — Desacoplamento

Domínio e casos de uso não devem depender diretamente de HTTP, browser automation ou detalhes internos de sistemas externos.

### RNF-007 — Privacidade

Tratamento de dados pessoais e dados de saúde deve seguir LGPD e requisitos adicionais aplicáveis ao contrato/órgão.

## 3. Requisitos explicitamente pendentes

- sistema exato denominado E-Saúde no primeiro cliente;
- APIs disponíveis;
- método de autenticação;
- volume;
- SLA;
- integrações obrigatórias;
- modelo final de dados;
- requisitos contratuais;
- requisitos de infraestrutura governamental.
