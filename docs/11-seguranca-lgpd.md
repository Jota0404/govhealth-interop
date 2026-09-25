# GovHealth Interop — Segurança e LGPD

## 1. Princípios

- menor privilégio;
- identidade forte;
- segregação por unidade/órgão;
- secrets fora do código;
- criptografia;
- auditoria;
- rastreabilidade;
- minimização de dados;
- falha segura.

## 2. Dados de saúde

Dados relacionados à saúde são dados pessoais sensíveis e exigem controles apropriados.

O sistema deve determinar:

- quais dados realmente precisa guardar;
- por quanto tempo;
- quem pode acessar;
- em qual finalidade;
- de qual sistema vieram.

## 3. Escopo

O acesso deve considerar:

```
Usuário
  +
Perfil
  +
Órgão
  +
Unidade
  +
Contexto assistencial
```

## 4. Auditoria

Registrar quando necessário:

- usuário;
- recurso;
- origem;
- operação;
- horário;
- resultado;
- sistema externo.

## 5. Segurança de integrações

Tokens, certificados e credenciais:

- não ficam no código;
- não aparecem em logs;
- não entram em commits;
- devem utilizar secret management apropriado.

## 6. LGPD

O projeto deverá definir base legal, controlador/operador, retenção e responsabilidades conforme o órgão contratante e o fluxo real.

Este documento não substitui análise jurídica ou regulatória.

## 7. Produção

Antes de produção pública, revisar:

- threat model;
- gestão de identidades;
- backup;
- recuperação;
- logs;
- monitoramento;
- resposta a incidentes;
- pentest;
- requisitos de contratação.
