---
title: Consultar SAQUE PIX por EndToEndId
api:
  file: readme-hml-operations.json
  operationId: get_v1-cashout-pix-send-end-to-end-id-id
hidden: false
---
## Sobre

A consulta de cashout pelo EndToEnd ID permite rastrear e verificar o status e os detalhes de umatransação específica de saída de fundos (cashout). Isso é crucial para garantir a transparência, a precisão
e a eficiência na gestão de pagamentos e transferências. Neste modelo, teremos um campo adicional
“debitRejectionReason”, com o intuito de indicar o motivo da rejeição caso ocorra, se sucesso, retornará
nulo este objeto.  Possíveis status codes de rejeições poderão ser mapeados extraindo de nossa
documentação se status apartada, necessitando, solicite aos nossos times Geniais.