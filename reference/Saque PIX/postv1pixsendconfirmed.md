---
title: Confirmar SAQUE PIX
api:
  file: readme-hml-baas.json
  operationId: post_v1-pix-send-confirmed
hidden: false
---
## Sobre

O endpoint de confirmação de PIX é utilizado como etapa final para concluir um saque via PIX. Para realizar o saque com sucesso, é necessário informar o idempotencyId gerado no endpoint anterior (Inicializar Saque) nesta requisição. Essa operação deve ser realizada em até 60 segundos após a geração do idempotencyId, garantindo a consistência e o sucesso da transação. 

### "historicComplement"

O campo historicComplement desempenha um papel essencial na inclusão de um ID personalizável para conciliação no arquivo de extrato. Ele permite registrar seu ID de forma clara e eficiente, facilitando o rastreamento e a conciliação das transações de maneira mais precisa.