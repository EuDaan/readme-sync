---
title: Gerar Qrcode Dinâmico
api:
  file: readme-hml-qrcode.json
  operationId: post_v2-qrcode-dynamic
hidden: false
---
## Sobre

* A geração de QR Codes para transações PIX via API é uma solução moderna e eficiente para integrar pagamentos instantâneos no Brasil. O PIX é um sistema de pagamentos instantâneos criado pelo Banco Central do Brasil, que permite transferências e pagamentos rápidos, 24 horas por dia, todos os dias do ano.
* No contexto de pagamentos e transações financeiras, os QR Codes dinâmicos permitem a atualização das informações contidas no código após sua criação. Isso significa que detalhes como o valor da transação, a descrição e outros parâmetros podem ser modificados conforme necessário, sem a necessidade de gerar um novo código. Por exemplo, se o valor de um pagamento mudar, o QR Code pode ser atualizado para refletir essa alteração.

## Como Funciona

* Configuração do Endpoint: É necessário fornecer parâmetros como o valor da transação, dados do recebedor, e outras informações específicas do PIX.
* Envio da Requisição: Com a configuração feita, uma requisição HTTP (POST) é enviada à API com os dados necessários.
* Recebimento do QR Code PIX: A API retorna um ID único para este QR Code gerado, e a partir deste, o destinatário poderá liquidar a transferência em seu banco de preferência.

## Vantagens

* Automatização: Integrando-se perfeitamente com sistemas de pagamento e reduz a necessidade de intervenção manual.
* Segurança: A geração de QR Codes PIX via API reduz significativamente o risco de erros de digitação e fraudes, assegurando que as transações sejam processadas de maneira precisa e segura.

## Formatos

* IMMEDIATO
  * O QR Code Imediato é um tipo de QR Code dinâmico utilizado em transações financeiras, especialmente no sistema de pagamentos PIX no Brasil. Ele é gerado no momento da transação e contém informações específicas e detalhadas para aquele pagamento único.
  <br />
* Billing Due Date
  * PIX Cobrança é um serviço que permite a geração de cobranças com vencimento utilizando o sistema de pagamentos instantâneos do Brasil, PIX. Ele facilita a emissão de boletos eletrônicos e QR Codes para pagamentos, proporcionando maior agilidade e eficiência nas transações financeiras, além de reduzir custos operacionais para empresas e consumidores.
  * Ainda é possível criar um ou mais PIX Cobranças em lote em uma única requisição. Isso gera uma lista de itens na resposta da API, facilitando o controle das cobranças dentro da sua regra de negócio.