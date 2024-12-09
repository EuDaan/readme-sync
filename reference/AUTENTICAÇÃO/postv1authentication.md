---
title: Autenticação
api:
  file: readme-hml-auth.json
  operationId: post_v1-authentication
hidden: false
---
Para acessar toda a API do BAAS, é necessário autenticar-se usando um token de usuário criptografado, que será fornecido pela nossa equipe técnica. Uma vez autenticado, será gerado um token JWT com uma validade de 20 minutos para permitir o acesso aos recursos protegidos.

* A chave de autorização básica é necessária e o valor é o token de usuário criptografado fornecido por nossa equipe técnica.
* X-ORIGEM é um cabeçalho OBRIGATÓRIO para melhor controle de nossos logs e segurança da API.