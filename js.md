permalink: /js

# Javascripts

<script src="prism.js"></script>



Apesar de não conhecer em absoluto essa linguagem, re-utilizei e adaptei diversos scripts para utilizar aqui no site.

- O [AnchorJS](https://www.bryanbraun.com/anchorjs/) facilita a obtenção de links diretos para títulos (h1-h4) em cada artigo.
- O [PrismJS](https://prismjs.com) realiza o realce de sintaxe nos blocos de código.
- [Um script](https://codepen.io/andybelldesign/pen/VOELMZ) que [encontrei online](https://piccalil.li/tutorial/create-a-user-controlled-dark-or-light-mode/) faz a alternância entre os modos claro e escuro quando o usuário clica no ícone do cabeçalho.


## Organizar alfabeticamente

Um pequeno script oferecido por David Merfield organiza os artigos em ordem alfabética na seção de tags.

```language-html
	<div id="entry-list"> <!-- Conteúdo --> </div>

	<script type="text/javascript">
		var list = document.querySelector('#entry-list');
		[...list.children]
		  .sort((a,b)=>a.getAttribute('data-sort')>b.getAttribute('data-sort')?1:-1)
		  .forEach(node=>list.appendChild(node));
	</script>
```


## De volta ao início

Esse trechinho, retirado do [W3Schools](https://www.w3schools.com/howto/howto_js_scroll_to_top.asp), é responsável pelo botão que aparece quando o usuário rola a página para baixo e que leva de volta ao início quando é ativado. 

```language-html

<button onclick="topFunction()" id="myBtn" title="Go to top">⬆︎</button>

<script>
//Get the button
var mybutton = document.getElementById("myBtn");
// When the user scrolls down 20px from the top of the document, show the button
window.onscroll = function() {scrollFunction()};
function scrollFunction() {
  if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
    mybutton.style.display = "block";
  } else {
    mybutton.style.display = "none";
  }
}
// When the user clicks on the button, scroll to the top of the document
function topFunction() {
  document.body.scrollTop = 0;
  document.documentElement.scrollTop = 0;
}
</script>

```