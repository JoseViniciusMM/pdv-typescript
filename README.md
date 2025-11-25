# pdv-typescript

Desenvolver uma aplicação para um Ponto de Venda (PDV) com banco de dados SQLite.

## Camadas:
1. Models: Interfaces representando usuários, produtos, compras e itens das compras.
2. Acesso ao Banco de Dados: Criar schema, inserir, listar, alterar e deletar.
3. Regras de Negócio.
4. Controller: Funções para produto, listar produtos, realizar compras, etc.

## Regras de Negócio:
Vendas no PIX têm 5% de desconto. (Assumi que "Si" era um erro de digitação para 5% ou Sim)
Vendas no débito não têm desconto e nem acréscimo.
Vendas no crédito têm acréscimo e podem ser parceladas.

## Fluxo Controller / Repository:
Função RealizarVenda(venda: Venda) -> Regras de Negócio -> gravarVenda(SQL)
