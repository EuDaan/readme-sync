---
title: Enviar PIX Manual
api:
  file: readme-hml-baas.json
  operationId: post_v1-pix-send-manual
hidden: false
---
## Sobre

O envio manual de PIX é um processo em que não se utiliza uma chave PIX específica (como CPF, e-mail ou telefone). Em vez disso, é necessário fornecer todos os dados bancários do recebedor para completar a transação.

**Dados Necessários para o Envio Manual:**

* Nome do recebedor
* Agência
* Conta
* Tipo de conta (corrente ou poupança)
* Documento (CPF/CNPJ)
* ISPB (Identificador do Sistema de Pagamentos Brasileiro, um código único para cada instituição financeira)

**Requisição:**\
Etapa de pagamento: Apenas uma requisição é necessária. Todos os dados mencionados acima são informados em uma única etapa, e a transferência é processada de uma vez.