tags: Escrita, Apps, Markdown
permalink: /editores-de-texto

# Editores de texto  
  
Editores de texto, diferente dos [processadores de texto](processadores-de-texto), não suportam texto com formatação [rich text](texto-plano) nem seguem o modelo WYSIWYG (*What You See Is What You Get*). Esses são softwares com um propósito diferente: são capazes de lidar com diversas linguagens de marcação e de processar velozmente arquivos de texto. Para investigadores das humanidades, a importância desse tipo de software reside justamente nisso; *i.e.*, na capacidade de processar textos na casa dos milhões de caracteres, efetuando correções, modificações, buscas e substituições usando [expressões regulares](regex), etc.  
  
Para exemplificar, digamos que você tenha encontrado [uma edição do comentário de Alexandre de Afrodísias à Metafísica de Aristóteles](https://scaife.perseus.org/reader/urn:cts:greekLit:tlg0732.tlg004.opp-grc1:1/) em formato XML e decidido que pode ser importante ter uma cópia offline para consulta e citações. O comentário tem 3.399.933 caracteres. Consegue imaginar o Microsoft Word abrindo um arquivo desse tamanho? *Impossível*. Consegue se imaginar trabalhando no bloco de notas sem nenhum recurso adequado de busca e navegação pelo texto? *Improvável*.  
  
O software para esse tipo de tarefa é um **editor de texto**.  
  
### Qual software utilizar  
  
A maior parte dos editores compartilha de um núcleo comum de funções: realce de sintaxe para inúmeras linguagens (LaTeX, Markdown, Applescript, Javascript, HTML, CSS, Python, Ruby, etc…), busca e substituição avançada com [*RegEx*](RegEx), integração com o sistema git de versões e acesso integrado ao terminal/shell. Eventualmente algumas tarefas serão mais fáceis de executar em um programa do que no outro, mas em última instância todos são bem equipados e capazes de realizar as tarefas mais importantes. Qual processador utilizar, portanto, é em grande medida uma questão de preço, preferências pessoais e de compatibilidade. Minha sugestão é baixar qualquer um desses softwares mencionados e começar aos poucos a explorá-los. Há vários outros disponíveis por aí, mas esses são alguns dos melhores.  
  
- O [BBEdit](bbedit) (apenas macOS) é o processador que passo mais tempo utilizando.
	- [TextMate](http://www.macromates.com) (apenas macOS) é uma alternativa ao BBEdit que também é popular. Em muitos respeitos, ele é igualmente capaz, mas certamente oferece menos opções de automação para a edição de um grande volume de arquivos simultaneamente.  
- O [Sublime Text](http://www.sublimetext.com) é software modular e *cross-plataform* (Windows e Mac), com capacidades semelhantes ao BBEdit e que podem ser estendidas por [pacotes](http://www.packagecontrol.io). Digno de nota é a possibilidade de inserir múltiplos cursores (para editar várias linhas ao mesmo tempo) e o layout em grid que permite utilizar ter até 4 arquivos de texto abertos simultaneamente de maneira organizada. Aparentemente, é um programa que também pode funcionar em modo *trial* indefinidamente.  
- O [Visual Studio Code](https://code.visualstudio.com) é um software gratuito, *cross-plataform* (por ser baseado em electron) e de código aberto, mantido pela Microsoft. Assim como o Sublime, o VSC tem um repositório de pacotes para estender as funções nativas. Definitivamente vale a pena ter disponível no sistema, apesar de provavelmente não ser a melhor opção disponível.  
- [Brackets](http://brackets.io) é semelhante ao VSC, mas é mantido pela *Adobe*.  

VEJA também:  
- [Editores de markdown](markdown).  
- [Por que deveríamos parar de usar o Word](markdown-versus-word)  
  