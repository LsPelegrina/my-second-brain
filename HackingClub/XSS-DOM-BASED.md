O xss dom based, tem o mesmo funcionamento dos demais, entretanto, as informações não são renderizadas por um backend, é uma falha que acontece explicitamente no front-end da aplicação, no navegador. 

Podemos perceber que é exclusivamente, e unicamente no front-end, pois quando analisamos o código fonte depois de fazer uma requisição, ele não aparece o input que fizemos, ou seja não é o back-end o resposavel por enviar e concatenar o resultado no front-end. Um exemplo seria utilizando o innerHTML, função do proprio DOM. que grava a informação direta em uma tag.



<h1>Laboratório</h1>
NO laboratório em questão, temos um navbar, que tem uma barra de pesquisa, e nele podemos inserir valorar, ou seja um input, quando inserimos ele reflete na tela, normalmente, mas quando vamos olhar no código fonte, não existe o input que colocamos, ou seja, se caracteriza como dom based, adicionando uma payload maliciosa com um script, ele retorna a flag.