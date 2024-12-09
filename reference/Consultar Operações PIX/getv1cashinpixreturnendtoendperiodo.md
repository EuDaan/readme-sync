---
title: Consultar DEPOSITO de Devolução OriginalEndToEndId
api:
  file: readme-hml-operations.json
  operationId: get_v1-cashin-pix-return-endtoend-periodo
hidden: false
---
## Sobre

A consulta de devolução pelo EndToEnd ID permite rastrear e verificar o status e os detalhes deuma transação específica de devolução de fundos. Isso é crucial para garantir a transparência, a precisãoe a eficiência na gestão de reembolsos e estornos. Neste modelo, teremos um campo “rejection”, com o
intuito de indicar o motivo da rejeição caso ocorra, se sucesso, retornará nulo este objeto. Possíveis
status codes de rejeições poderão ser mapeados extraindo de nossa documentação se status apartada,
necessitando, solicite aos nossos times Geniais.