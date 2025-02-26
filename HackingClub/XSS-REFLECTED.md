Ocorre quando eu tenho um input de texto que me retorna exatamente o que eu estou enviando no front-end.

O input de tela, é o mesmo parâmetro que aparece na URL. Setar tanto pelo input, quando pela URL funciona.

exemplo: eu envio em um input a palavra, word. E o back-end retorna para o front-end que renderiza a palavra word sem nenhuma validação. 


Se possível injetar tags html, a vulnerabilidade vira um HTML injection(HTMLi), como por exemplo passar um: 
~~~HTML
<h1>Algumas coisa</h1>
~~~
Então renderizará isso em tela, "<strong>REFLETINDO</strong>" o que eu estou passando como "<strong>PARAMETRO</strong>"


Agora se for possível utilizar javascript nesses inputs passando pela tag:
~~~HTML
<script>Algo</script>
~~~
Nós podemos pegar dados do usuário, como o que ele está digitando, ou os cookies de sessão, para que pudêssemos passar por esse usuário.
<strong>O HTTP-ONLY na definição do cookie não pode estar ativo</strong> para que possamos pegar o cookie utilizando JS 

Aqui temos algumas coisas interessantes, pois não necessariamente precisamos rodar uma tag script para rodar um script js, podemos utilizar tags de imagens, ou svgs por exemplo, onde podemos passar campos como onload, ou onerror, e colocar para executar uma função, exemplo: onload=alert(1), ou onerror=alert(2), o que faz com que rode um script js, mesmo não utilizando uma tag script.

<h1>Laboratório</h1>
O laboratório era 3 inputs, onde um refletia pegando o meu nome em real time, então colocando uma tag de negrito, ele já renderizou o html, resultando em um HTMLi, ou seja, quando colocamos a tag de script ele já resultou em um xss, e entregou a flag para nós.