O sql injection blind time based, é quando não temos visualmente disponivel algo que nós mostre quais são os valores que as queries estão retornando, então utilizamos algo chamado sleep na linguagem sql, que faz com que as sentenças demorem certo tempo para serem executadas quando entram em uma condição verdadeira, ou falsa, ou seja, se a query demora o tempo selecionado, por exemplo sleep(3), 3 segundos, significa que o valor existe.




<h1>Laboratório</h1>
No laboratorio temos um input de login, e percebemos que o campo de usuario é vulneravel a sql, porém ele não tem nenhum dado visivel, e é possivel quebrar a autenticação também, fazendo ignorar totalmente a password, utilizando o ' or 1=1, onde ele vai retornar algum usario do bd para se autenticar.


nome do bd: cc
versão do bd:
usuario:

nome das tabelas: users
nome das colunas: id, login, password 

nome do login: carlos | admin
senhas: s3nh4@123| h4rd_p@ssw0rd_t0_gu3ss


Aqui está o script utilizado para realizar a exfiltração dos dados: