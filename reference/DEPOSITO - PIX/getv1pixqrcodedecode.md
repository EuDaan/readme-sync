---
title: Decodificar QRCODE
api:
  file: readme-hml-baas.json
  operationId: get_v1-pix-qrcode-decode
hidden: false
---
## Sobre

Este serviço realiza a decodificação de QR Codes gerados ou recebidos, fornecendo informações essenciais para conciliação de dados e pagamento via copy-paste, caso necessário. A resposta inclui dados bancários associados, valores e configurações preparatórias para liquidação.

**Funcionalidades:**

* Retorna informações úteis para a conciliação de dados.
* Disponibiliza os seguintes dados após a decodificação:
  * Informações bancárias relacionadas ao QR Code;
  * Valores associados;
  * Configurações prévias para a liquidação.