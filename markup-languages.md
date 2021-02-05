permalink: /markup-languages
tags: Escrita, Markdown

# Linguagens de marcação
<script src="prism.js"></script>

Linguagens de marcação são linguagens de computação que usam etiquetas para definir elementos de estrutura e estilo em um documento. E.g.: \<p>Assim é que se representa um parágrafo em HTML\</p>. As linguagens mais populares são XML, HTML e Markdown.

## HTML

HTML usa etiquetas pré-definidas para representar uma página. Para definir as seções utiliza-se: \<head>, \<body>, \<div>; para definir elementos: \<p>, \<table>, \<form>, \<image> e \<a>; para definir a formatação do texto: \<h1>, \<h2>, \<h3>, … , \<b> e \<i>.

```language-html
<html>
    <body>
        <h1>Platão</h1>
        <h2>Parmênides</h1>
        <p>126a1 Ἐπειδὴ Ἀθήναζε οἴκοθεν ἐκ Κλαζομενῶν ἀφικόμεθα, 126a2 κατ᾽ ἀγορὰν ἐνετύχομεν Ἀδειμάντῳ τε καὶ Γλαύκωνι· καί 126a3 μου λαβόμενος τῆς χειρὸς ὁ Ἀδείμαντος, Χαῖρ᾽, ἔφη, ὦ 126a4 Κέφαλε, καὶ εἴ του δέῃ τῶν τῇδε ὧν ἡμεῖς δυνατοί, φράζε.</p>
        <p>After arriving in Athens from our home town, Clazomenae, we happened to meet Adeimantus and Glaucon in the marketplace; and Adeimantus, taking my hand, said:</p>
        <p>But why Socrates, don't you just <a href="www.google.com">Google it?</a></p>
    </body>
</html>    

```

HTML é a linguagem utilizadas pelas páginas da internet e pelos eBooks (arquivos com extensão .epub, .mobi e .azw). Para maiores informações, recomendo conferir o [W3Schools](https://www.w3schools.com).

## XML

XML é um desdobramento do HTML e funciona do mesmo modo, com uma importante diferença: não há etiquetas pré-definidas. É uma linguagem que serve, sobretudo, para guardar dados de uma maneira estruturada. 

```language-xml
<fonte primária>
  <autor>Platão</autor>
  <obra>Parmênides</obra>
  <texto>
    <grc>126a1 Ἐπειδὴ Ἀθήναζε οἴκοθεν ἐκ Κλαζομενῶν ἀφικόμεθα, 126a2 κατ᾽ ἀγορὰν ἐνετύχομεν Ἀδειμάντῳ τε καὶ Γλαύκωνι· καί 126a3 μου λαβόμενος τῆς χειρὸς ὁ Ἀδείμαντος, Χαῖρ᾽, ἔφη, ὦ 126a4 Κέφαλε, καὶ εἴ του δέῃ τῶν τῇδε ὧν ἡμεῖς δυνατοί, φράζε.</grc>
    <eng>After arriving in Athens from our home town, Clazomenae, we happened to meet Adeimantus and Glaucon in the marketplace; and Adeimantus, taking my hand, said:</eng>
  </texto>
</fonte primária>

```

XML é o formato utilizado pelas edições digitais dos textos antigos disponíveis no Perseus e no First1kGreek. Há uma iniciativa chamada  [TEI](https://tei-c.org/)  (text encoding initiative) que fornece diretrizes e padrões para a codificação eletrônica de textos em formato XML. O editor do novo dicionário de grego antigo da Cambridge (a ser publicado até o início de 2021) descreve do seguinte modo as vantagens desta linguagem de marcação:

> There will be an electronic edition on the Perseus site. The system means that it can be easily and accurately searched. Dictionaries which are tagged after they were written necessarily contain fewer tagged elements than ours (as they were not composed with such a precise structure), so fewer types of search are possible. A reader of our lexicon can, for example, see how vocabulary changes across the range of Ancient and Koiné Greek, because we mark usage in a corpus of 70 authors, from Homer to Plutarch, and so we can compare word frequency in different writers. And our system will also be linked to other Perseus databases, to images as well as to texts. (Fonte:  [https://www.classics.cam.ac.uk/research/projects/glp/tagging](https://www.classics.cam.ac.uk/research/projects/glp/tagging)  )

Esse exemplo mostra como o XML é extremamente versátil em associação com um ambiente de leitura que representará o texto. Podemos marcar no texto, por exemplo, as falas de cada personagem, a divisão dos argumentos, a análise morfológica de cada termo, etc. No ambiente de leitura que representa o texto, poderíamos optar por ver apenas as falas de Sócrates, por exemplo; por exibir as falas de cada personagem em cores diferentes; por exibir as falas de cada personagem com cores que refletem seu estado emocional, etc. As possibilidades são praticamente ilimitadas.

Uma dado importante que nós leigos costumamos ignorar é que todo texto com estrutura em um computador (sem exceção) usa alguma linguagem de marcação. Programas como o Microsoft Word e outros processadores de texto também costumam utilizar (um tipo próprio de) XML. Quando selecionamos alguma palavra e a transformamos em um título, por exemplo, o programa adiciona as etiquetas ao seu redor sem que nos demos conta. Não há nenhum problema nesse procedimento, mas ao utilizar o formato docx, por exemplo, é importante ter consciência de que estamos armazenando nossas anotações em uma linguagem que apenas um programa específico de uma empresa estrangeira consegue interpretar e exibir. Não há nenhuma garantia de que a aparência do texto seguirá a mesma em versões futuras do programa. (Quem usa o programa há mais tempo passou por isso quando o formato padrão deixou de ser .doc e passou a ser .docx).

## Markdown

Markdown é uma linguagem minimalista [criada em 2004](https://daringfireball.net/projects/markdown/) por [John Gruber](https://en.wikipedia.org/wiki/John_Gruber) e [Aaron Swartz](http://www.aaronsw.com/weblog/001189) com o propósito de possibilitar a geração de texto *html* — i.e. *hypertext markup language*, a principal linguagem utilizada na internet — a partir de um texto legível e com poucas distrações. O que começou como uma linguagem de marcação, digamos, anêmica e voltada apenas para a internet, evoluiu para uma linguagem extremamente popular com um bom conjunto de funcionalidades, capaz de satisfazer todas as necessidades do mundo científico e acadêmico. Utilizando a ferramenta de conversão chamada [Pandoc](pandoc), além disso, é possível transformar um texto em Markdown em praticamente qualquer outro formato existente, de um eBook a um livro acabado, passando por documentos em rtf, latex, docx ou html. É mais fácil obter um produto final com alta qualidade tipográfica utilizando Markdown do que qualquer outro processador de texto, como o Word.

Para os nossos fins, Markdown é extremamente relevante, pois é o meio mais simples de estruturar um texto de [fonte primária](https://gdct.blot.im/tagged/fontes-primárias) excessivamente longo, de registrar e manter anotações de pesquisa a longo prazo em um formato agnóstico ([pode ser lido por qualquer programa](markdown)) e que não demanda gastar tempo se ocupando da aparência do texto. É também a linguagem utilizada pela maioria das implementações digitais do [Zettelkasten](zettelkasten). Ou seja, é uma linguagem que podemos utilizar na construção de uma [Wiki Pessoal](Wikis) de pesquisa.

### Parágrafos

Para terminar um parágrafo e introduzir uma quebra de linha, basta acrescentar dois espaços em branco e um retorno (enter). 

```language-markdown
Eis uma linha.  
Eis uma linha nova.
```

Se você acrescentar apenas um retorno, sem os dois espaços em branco no fim da linha, isso será interpretado apenas como **um** espaço em branco. É importante saber também que 2, 3 ou 10 espaços em branco serão sempre representados como apenas um espaço.


### Títulos de seções  

São marcados com `#`.  É sempre boa prática saltar uma linha depois do título de uma seção. 
Exemplo:  

```language-markdown
# Título  

## Subtítulo  

### Subsubtítulo  

#### Etc...  

```  

### Citações  

São indicadas pelo maior `>`.  
Exemplo:  

```language-markdown  
 > Lorem ipsum…  
```  

### Notas de rodapé  

Podem ser feitas de mais de um modo.  
Exemplo 1:  

```language-markdown  
Lorem ipsum[^texto da nota de rodapé].  
```  

Exemplo 2:  
```language-markdown    
Lorem ipsum[^1].  
Etc.  

[^1]: Texto da nota de rodapé.  
```  

### Ênfase  

Pode variar, mas no geral é feita com um único asterisco antes e depois para *itálico* e dois asteriscos para **negrito**.  Exemplo:  

```language-markdown    
*Texto em itálico* e **texto em negrito**.  
```  

### Listas  
A lista ordenada é indicada por um número `1.` e a lista não ordenada pelo asterisco.  

```language-markdown    
1. Item 1  
1. Item 2  

- item  
- item  
```  

![Multimarkdown Composer](./img/apps/__mmd.png)  

Há bastante material na internet sobre markdown e seus diferentes sub-tipos, mas tudo que você precisa saber está nesse resuminho aí em cima. 

