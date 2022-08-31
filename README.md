# Modelagem_BD_E-Commerce
Modelagem feita no MySQL workbench para Bootcamp DataBase Experience na DIO



Para o refinamento do projeto proposto resolvi da seguinte forma:

1- Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações;
  Adcionei duas tables relacionadas a table "Cliente", optei por armazenar esses dados fora do "Cliente" para evitar de existir valores nulos, caso o cliente
seja um CPNJ ou um PF tera onde preencher e os elementos em comundo entre CNPJ e PF ficaram dentro da table clientes.

2- Pagamento – Pode ter cadastrado mais de uma forma de pagamento;
  Optei por adcionar na table "clientes" uma opcao para armazenar a forma de pagamento e criar uma table para o armazenamento dos "cartoes" visto que pode 
ocorrer o cadastro de mais de 1 cartao. Mantendo a table "cartao" esta referenciando o a table "cliente".

3- Entrega – Possui status e código de rastreio;
  Criei uma table "entrega" com relacionamento de 1:1 com a table "pedido", visto que um pedido tera apenas uma entrega, optei por criar uma nova table e nao 
  criar novas entidades dentro do pedido pois acredito que o pedido pode ser cancelado antes de passar para fase de entrega, assim tendo tables separadas
  facilitara a visualizacao desse movimentacao.
