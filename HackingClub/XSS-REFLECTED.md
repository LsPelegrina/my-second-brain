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