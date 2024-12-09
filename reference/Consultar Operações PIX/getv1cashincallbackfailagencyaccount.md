---
title: Consultar DEPOSITO com falha no envio WEBHOOK
api:
  file: readme-hml-operations.json
  operationId: get_v1-cashin-callback-fail-agency-account
hidden: false
---
## Sobre

O endpoint em questão serve como um mecanismo dedicado à conciliação de eventos webhooksrelacionados a transações de cashin (depósitos) que resultaram em falha. Sua função é buscar esses
eventos, proporcionando uma visão clara das comunicações malsucedidas, permitindo a identificação do
status da transação e todos os dados pertinentes a operação PIX pelo período configurado.