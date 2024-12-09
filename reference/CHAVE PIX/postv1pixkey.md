---
title: Registrar chave PIX
api:
  file: readme-hml-baas.json
  operationId: post_v1-pix-key
hidden: false
---
# Sobre

Seviço API para registrar uma chave PIX da sua conta bancária aqui no Banco Genial ao projeto BAAS no diretório do Banco Central do Brasil.

Tipos epserados:

* CNPJ: 14 números
* CPF: 11 números
* EMAIL: Deverá conter @ e ser válido
* EVP: Chave aleatória no formado GUID devendo compor 32 dígitos hexadecimais em um dos seguintes formatos: "123e4567-e89b-12d3-a456-426655440000" (hífens em locais padrão)
* TELEFONE: (DDI) + (DDD) + TELEFONE = Exemplo: +5511945408483