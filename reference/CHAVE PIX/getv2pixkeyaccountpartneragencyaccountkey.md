---
title: Consultar chave PIX para parceiros
api:
  file: readme-hml-baas.json
  operationId: get_v2-pix-key-account-partner-agency-account-key
hidden: false
---
## Sobre

A chave PIX é um identificador utilizado no sistema de pagamentos instantâneos brasileiro, o PIX,que foi desenvolvido pelo Banco Central do Brasil. Lançado em novembro de 2020, o PIX permitetransferências de dinheiro entre contas bancárias em questão de segundos, funcionando 24 horas por
dia, sete dias por semana, incluindo feriados.

A chave PIX serve como um "apelido" para as contas bancárias, simplificando o processo de envio erecebimento de dinheiro. Em vez de precisar de vários dados bancários, como número de agência e
conta, o usuário só precisa fornecer uma chave PIX. Essas chaves podem ser associadas a diferentes
tipos de informações: CPF/CNPJ, número de telefone celular, endereço de e-mail ou um código
aleatório gerado pelo próprio sistema. Cada chave pode estar vinculada a apenas uma conta bancária,
mas uma conta pode ter várias chaves diferentes associadas a ela.

## Como Funciona

O funcionamento da chave PIX é bastante simples e eficiente. Aqui estão os principais passos ecomponentes envolvidos:

* **Cadastro da Chave PIX:** O usuário deve cadastrar uma ou mais chaves PIX em sua instituição financeira. Isso pode ser feitoatravés do aplicativo do banco ou pelo internet banking. Durante o cadastro, o usuário escolhe o
  tipo de chave que deseja usar (CPF/CNPJ, número de telefone, e-mail ou chave aleatória) e a
  associa à sua conta bancária.
* **Envio de Dinheiro:** Para enviar dinheiro usando o PIX, o pagador precisa apenas da chave PIX do recebedor. Ele insereessa chave no campo apropriado no aplicativo do banco, especifica o valor a ser transferido e
  confirma a operação. Não há necessidade de informar outros dados bancários.
* **Recebimento de Dinheiro:** É possível também receber dinheiro pela chave PIX, basta apenas informa-la ao pagador. Orecebedor receberá uma notificação instantânea da transação quando ocorrida.
* **Alteração ou Exclusão de Chaves:** O usuário pode alterar ou excluir suas chaves PIX a qualquer momento. Isso oferece flexibilidade econtrole sobre como ele deseja gerenciar suas informações de pagamento.