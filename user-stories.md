# User Stories

## Template
- User Story Card: As `<who>` `<when>` `<where>`, I want `<what>` because `<why>` 
- Acceptance Test Card: 
  - Scenario `00`: Given `and` .. `and` .. When `and` Then `and`

## `U01` Comprar Moeda
- Como usuário cliente da lex
- Eu quero realizar a compra de moedas ao preço atual
- Debitando do saldo da minha carteira principal em $

### Cenário 01 - [Diagrama](https://balsamiq.cloud/s96ib5a/pg260a7)
- Dado que eu tenho $ 50 de saldo na minha carteira principal
  - E desejo comprar 40 lexcoin na cotação atual para minha carteira
  - E na cotação atual de $ 0.25 que vale então $ 10 no valor bruto
  - E que a LEX cobra 0,005%
- Quando houver uma venda disponível nesta quantidade e cotação
- Então eu consigo ver que minha compra foi realizada
  - E é debitado $ 10,05 da minha carteira principal
  - E é depositado 40 lexcoin na minha carteira
  - E é debitado 40 lexcoin da carteira do vendedor da oferta 
  - E é depositado $ 9,95 na carteira principal do vendedor
  - E é depositado $ 0,10 na carteira principal da lex

## `U02` Vender Moeda
- Como usuário cliente da lex
- Eu quero realizar a venda de moedas por um valor específico
- Para receber na minha carteira principal em $

### Cenário 01 - [Diagrama](https://balsamiq.cloud/s96ib5a/pg260a7)
- Dado que eu tenho 200 lexcoin de saldo 
  - E $ 0 de saldo na carteira principal
- Quando eu lançar a oferta de 40 lexcoins para venda 
  - E que eu informe no preço de $ 0.50 cada lexcoin
- Então eu consigo ver que minha oferta de venda foi realizada

## `U03` Cadastrar Cliente
- Como usuário cliente da lex
- Eu quero realizar o meu cadastro
- Para que eu possa realizar atividades na plataforma

### Cenário 01
- Dado que eu não tenho cadastro na lex
- Eu desejo realizá-lo 
  - E eu informe meus dados básicos como nome, nascimento e outros não mais que 5 campos
  - E o pix é gerado automáticamente aleatório de 16 dígitos gerado automaticamente pela api
  - E eu informo também a minha senha e o nickname (nome do usuário na aplicação) com perfil USER
  - E a api entende que eu como cliente possuo relação com o usuário logado criado .. 
  - Ou seja, a classe cliente (que é uma conta) possui um user (spring security)
- Então eu recebo a mensagem que meu cadastro foi realizado com sucesso

## Refs
- [User Story Wikipedia](https://en.wikipedia.org/wiki/User_story)
- [Exemplo de Estória de Usuário e Critérios de Aceitação](https://www.researchgate.net/figure/Figura-2-Exemplo-de-historia-de-usuario_fig2_228842194)
- [Delivering User Stories for Implementing Logical Software Architectures by Multiple Scrum Teams, 2014](https://sci-hub.se/10.1007/978-3-319-09150-1_55)
- [Acceptance Criteria for User Stories: Purposes, Formats, Examples, and Best Practices, 2021](https://www.altexsoft.com/blog/business/acceptance-criteria-purposes-formats-and-best-practices/)
