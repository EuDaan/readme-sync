---
title: Realizar pagamento TED
api:
  file: readme-hml-corebank.json
  operationId: post_v2-payment-ted
hidden: false
---
## Sobre

A API CoreBank de Operações de TED e TEF é uma solução robusta destinada a facilitar aintegração de sistemas financeiros com a infraestrutura bancária para a realização de transferências
eletrônicas de fundos. TED (Transferência Eletrônica Disponível) e TEF (Transferência Eletrônica de
Fundos) são métodos vitais para a movimentação de dinheiro entre contas bancárias, sendo a TED
utilizada para transferências entre bancos diferentes e a TEF para transações internas dentro do mesmo
banco. A API CoreBank é projetada para proporcionar um meio seguro, eficiente e automatizado para
gerenciar essas operações, suportando a interconectividade e a interoperabilidade entre diversas
plataformas financeiras.

## Como Funciona

A API CoreBank opera por meio de uma série de endpoints bem definidos, permitindo aosdesenvolvedores realizar uma ampla gama de ações relacionadas às transferências de fundos. Abaixo,
detalhamos o funcionamento da API

* **Autenticação e Autorização:**
  * Segurança: Para garantir a segurança das operações financeiras, a API exige que as solicitaçõessejam autenticadas. Isso é normalmente realizado através de tokens de acesso.
  * Autorização: Além da autenticação, a API verifica se o cliente tem permissão para realizar aoperação solicitada, garantindo que apenas usuários autorizados possam iniciar transferências.
* **Iniciação de Transferência:**
  * Requisição: O cliente envia uma solicitação de transferência contendo informações detalhadas,incluindo dados da conta de origem, conta de destino, valor a ser transferido, e outras informações
    necessárias.
  * Dados Necessários: As informações geralmente incluem número da conta, agência, nome dobeneficiário, CPF/CNPJ, e detalhes específicos da transação.
* **Validação de Dados:**
  * Verificação: A API valida os dados fornecidos para assegurar que todas as informações estãocorretas e que a transação está em conformidade com as políticas do banco e regulamentações
    financeiras.
  * Checagem de Saldo: Para TED, é verificado se há saldo suficiente na conta de origem e se os limitesde transação não foram ultrapassados.
    5
* **Processamento da Transferência:**
  * TED: Envolve a comunicação com outros bancos através da rede do Sistema de PagamentosBrasileiro (SPB), garantindo que os fundos sejam transferidos de um banco para outro de forma
    rápida e segura.
  * TEF: A transferência é processada internamente dentro do mesmo banco, utilizando a infraestruturainterna para mover os fundos entre contas.
* **Consulta e Relatórios:**
  * Status das Transferências: A API permite consultar o status de transferências em andamento,oferecendo visibilidade em tempo real sobre o progresso das transações.
  * Relatórios Detalhados: Geração de relatórios abrangentes de transações concluídas, permitindouma gestão financeira precisa e eficiente, além de facilitar a reconciliação bancária