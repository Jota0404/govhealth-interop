# GovHealth Interop — Plano de Testes

## 1. Estratégia

Os testes serão divididos em:

- unitários;
- integração;
- contrato;
- end-to-end;
- segurança;
- validação operacional.

## 2. Casos essenciais

### T-001 — Login e contexto

Verificar identificação correta de:

- usuário;
- profissional;
- unidade;
- escopo.

### T-002 — Contexto do cidadão

Confirmar associação correta entre cidadão e atendimento.

### T-003 — Sistema externo

Abrir integração sem alterar o contexto errado.

### T-004 — Falha externa

Simular timeout/erro e garantir que:

- o erro seja registrado;
- não seja classificado como sucesso;
- o usuário seja informado.

### T-005 — Auditoria

Confirmar que ações relevantes produzam AuditEvent.

### T-006 — Isolamento

Confirmar que um usuário não consiga acessar dados fora de seu escopo.

## 3. Teste de produto

Antes/depois:

```
Tempo atual
Redigitações
Sistemas abertos
Erros
Retrabalho
   ↓
GovHealth
   ↓
comparação
```

O piloto deve produzir números reais.
