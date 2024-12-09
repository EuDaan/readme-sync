---
title: Consultar Saque - REDIS - Por duas horas
api:
  file: readme-hml-baas.json
  operationId: get_v1-pix-status-callback-endtoendid
hidden: false
---
## Sobre

A consulta de cashout pelo EndToEnd ID permite rastrear e verificar o status e os detalhes de umatransação específica de saída de fundos (cashout). Isso é crucial para garantir a transparência, a precisão
e a eficiência na gestão de pagamentos e transferências. Neste modelo, teremos um campo adicional
“rejection”, com o intuito de indicar o motivo da rejeição caso ocorra, se sucesso, retornará nulo este
objeto.  Possíveis status codes de rejeições poderão ser mapeados extraindo de nossa documentação se
status apartada, necessitando, solicite aos nossos times Geniais.

**IMPORTANTE:**Consulta apenas disponível em até duas após a sua conclusão, comportamento esperado por estar
locado em nosso cache, após este período favor acionar o nosso serviço mencionado anteriormente em
nosso banco de dados.