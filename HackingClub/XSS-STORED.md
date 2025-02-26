No xss-stored, tem o mesmo funcionamento do xss-reflected, porém ele fica armazenado em algum lugar do site, seja em um banco de dados, ou em cache, ou em cookie, o que faz com que a vitima apenas tenha que acessar o site, pois o payload já estará nele, como se fosse direto do código fonte, diferente do reflected, que teriamos que fazer uma engenharia social para a vitima abrir nossa payload maliciosa. 



<h1>Laboratório</h1>

No laboratório temos um input que quando enviamos alguma coisa, ele fica salvo como se fosse um comentário de um vídeo, e se reiniciarmos a página ele ainda fica lá, o que indica que está sendo armazenado em algum lugar.
Quando nós colocamos uma payload maliciosa, ou testamos com um simples HTMLi, ele retorna o valor sem ser renderizado, ou seja, apenas o texto cru, mas quando fazemos o reload da página, ele renderiza a payload, e nós da o resultado esperado, no caso da tag de negrito, o texto fica em negrito. Então só criarmos um payload de script e a flag aparecerá