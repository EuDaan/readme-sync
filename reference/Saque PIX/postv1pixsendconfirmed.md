---
title: Confirmar SAQUE PIX
api:
  file: readme-hml-baas.json
  operationId: post_v1-pix-send-confirmed
hidden: false
---
## Sobre

O endpoint de confirmação de PIX é utilizado como etapa final para concluir um saque via PIX. Para realizar o saque com sucesso, é necessário informar o idempotencyId gerado no endpoint anterior (Inicializar Saque) nesta requisição. Essa operação deve ser realizada em até 60 segundos após a geração do idempotencyId, garantindo a consistência e o sucesso da transação.