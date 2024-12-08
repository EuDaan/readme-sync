---
title: Consultar chave PIX para parceiros
api:
  file: readme-hml-baas.json
  operationId: get_v2-pix-key-account-partner-agency-account-key
hidden: false
---
## Explicação

A função deste serviço é pesquisar uma chave PIX atreladas a diversas contas bancarias cadastradas no sistema bancario do Banco Central do Brasil. A solicitação recebe as informações da conta original e a chave desejada. O resultado são as informações da chave, da conta e um novo End-to-end para ser utilizado em uma operação de envio pix. Este endpoint usa uma lógica de bucket para evitar bloqueios vindos do Banco Central do Brasil.

**URL** : `/v2/pix/key-account-partner/{agency}/{account}/{key}`

**Método** : `GET`

**Autenticação necessária** : `YES - JWT`