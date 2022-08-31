# Modelagem_BD_E-Commerce
Modelagem feita no MySQL workbench para Bootcamp DataBase Experience na DIO, utilizei o que foi feito em conjunto no curso e os refinamentos proposto pela especialista.
Deixo o PNG e o arquivo para edicao, se tiver dicas fico aberto para aprender, obrigado.


Para o refinamento do projeto proposto resolvi da seguinte forma:

1- Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações;
  Adcionei duas tables relacionadas a entidade "Cliente", optei por armazenar esses dados fora do "Cliente" para evitar de existir valores nulos, caso o cliente
seja um CPNJ ou um PF tera onde preencher e os elementos em comundo entre CNPJ e PF ficaram dentro da entidade clientes.

2- Pagamento – Pode ter cadastrado mais de uma forma de pagamento;
  Optei por adcionar na entidade "clientes" uma opcao para armazenar a forma de pagamento e criar uma entidade para o armazenamento dos "cartoes" visto que pode 
ocorrer o cadastro de mais de 1 cartao. Mantendo a entidade "cartao" esta referenciando o a entidade "cliente".

3- Entrega – Possui status e código de rastreio;
  Criei uma entidade "entrega" com relacionamento de 1:1 com a entidade "pedido", visto que um pedido tera apenas uma entrega, optei por criar uma nova entidade e nao 
  criar novos atributos dentro do pedido pois acredito que o pedido pode ser cancelado antes de passar para fase de entrega, assim sendo entidades separadas
  facilitara a visualizacao dessa movimentacao.
