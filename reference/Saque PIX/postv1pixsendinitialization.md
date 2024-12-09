---
title: Inicializar SAQUE PIX
api:
  file: readme-hml-baas.json
  operationId: post_v1-pix-send-initialization
hidden: false
---
## Sobre

PIX é um sistema de pagamentos instantâneos criado pelo Banco Central do Brasil, lançado em novembro de 2020. Ele permite transferências e pagamentos em tempo real, funcionando 24 horas por dia, sete dias por semana, incluindo feriados. Esse sistema revolucionou a maneira como transações financeiras são realizadas no Brasil, tornando o processo mais rápido, prático e acessível.

## Como Funciona

<br />

* Chaves PIX: Para utilizar o PIX, o usuário precisa cadastrar uma chave PIX em sua instituição financeira. As chaves podem ser:
  * **CPF/CNPJ:**
    * Deverá conter para CPF: 11 números
    * Deverá conter para CNPJ: 14 números
  * **Número de telefone:**
    * Sempre iniciado com o DDI = +55 e com a sua sequencia de DDD = Código local do estado responsável pelo numero do telefone do cliente. Exemplo = +5511922334455
  * **E-mail:**
    * Sempre em formato de caracteres minúsculos, com @ aplicado e válido.
  * **Chave aleatória:**
    * (Uma sequência de números e letras gerada pelo sistema)
* **Recebimento de Pagamentos:**\
  Ao fornecer sua chave PIX, você pode receber transferências de qualquer pessoa ou empresa.
  O valor é creditado instantaneamente na conta cadastrada.

## Vantagens

* Velocidade: As transferências são concluídas em até 10 segundos, independente do dia ou horário.
* Disponibilidade: Funciona 24/7, inclusive em finais de semana e feriados.
* Segurança: O PIX utiliza mecanismos avançados de segurança, como autenticação multifator e criptografia.
* Praticidade: O uso de chaves PIX simplifica o processo de transferência, eliminando a necessidade de fornecer diversos dados bancários.

## Envio de PIX

O PIX se tornou uma ferramenta essencial no cotidiano financeiro dos brasileiros, proporcionando uma forma moderna, eficiente e acessível de realizar pagamentos e transferências.\
Os envios acontecem por duas modalidades, relacionados abaixo:

* Manual
* Inicialização e Confirmação

## Envio com Inicialização e Confirmação

Neste formato, a transferência é feita utilizando apenas a chave PIX do recebedor, simplificando o processo e minimizando a necessidade de inserir vários dados.

**Dados Necessários:**\
Chave PIX do recebedor (CPF, CNPJ, e-mail, telefone ou chave aleatória)

**Requisição:**\
Etapas: O processo é dividido em duas etapas distintas:
Inicialização: Onde se fornece a chave PIX do recebedor e recebe os dados bancários relacionados a chave PIX informada.
Confirmação: Onde se verifica e confirma a transferência.

## Garantindo a Integridade e Não Duplicidade

O ecossistema de pagamentos instantâneos, notadamente representado pelos PIX, revolucionou a forma como as transações financeiras são conduzidas. No âmbito dessa evolução, é essencial compreender e implementar práticas robustas para garantir a integridade e evitar a duplicidade de transações. Neste artigo, exploraremos duas camadas cruciais de proteção na API PIX, destacando os campos "idempotencyId" e "ignorePaymentDuplication".

## Camada 1: ignorePaymentDuplication

O campo "ignorePaymentDuplication" desempenha um papel crucial como a primeira linha de defesa contra transações duplicadas. Configurado como "FALSE", este campo aciona uma verificação em nossa base de operações, analisando dados de origem, destino e valor nas últimas 2 horas. Se a busca revelar uma duplicidade, a API notificará a ocorrência, fornecendo informações sobre a transação duplicada e o horário em que ocorreu o envio de sucesso na janela de duas horas.

Configurado como "TRUE", indica apenas que devemos ignorar essa primeira camada de verificação e pular para a segunda camada de proteção, segue abaixo.

## Camada 2: idempotencyId

A segunda camada de proteção é fornecida pelo campo "idempotencyId", um identificador único atribuído a cada transação PIX. Este campo desempenha um papel crucial na prevenção de transações duplicadas.

Quando um "idempotencyId" é incluído no corpo da requisição, a API garante que apenas um status de sucesso pode estar associado a essa transação específica. Mesmo que o cliente envie múltiplas requisições com o mesmo "idempotencyId", a duplicidade é evitada porque a transação está vinculada apenas ao primeiro status de sucesso. Isso garante rastreabilidade e unicidade em cada transação, simplificando a gestão e eliminação de possíveis redundâncias.

## Conclusão

A integridade e não duplicidade de transações são preocupações centrais em qualquer sistema financeiro, e o ecossistema PIX não é exceção. Ao compreender as nuances dos campos "ignorePaymentDuplication" e "idempotencyId", os desenvolvedores podem implementar uma estratégia de defesa em camadas, garantindo que as transações sejam processadas com eficiência, segurança e confiabilidade. A combinação dessas camadas proporciona uma abordagem robusta para lidar com os desafios inerentes à natureza instantânea e dinâmica das transações PIX.