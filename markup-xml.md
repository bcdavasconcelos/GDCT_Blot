permalink: /xml
tags: Linguagens de marcação

# XML

<script src="prism.js"></script>

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
