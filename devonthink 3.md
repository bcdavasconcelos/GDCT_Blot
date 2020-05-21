tags: Organização, Apps, macOS, DEVONthink

# DEVONthink 3  
  
  
![DEVONthink 3](/Imagens/dt.png)  

**🕸️** [DEVONthink Pro 3](https://www.devontechnologies.com/apps/devonthink/new) () *é um software com diversas funcionalidades e que pode ser utilizado para construir uma caixa fichário ou Wiki, e para armazenar e organizar livros, documentos e arquivos em geral.*  

O DEVONthink gerencia bancos de dados que são basicamente pacotes de arquivos de todos os tipos. Quando um arquivo é adicionado a um banco de dados, ele se torna um *record* (um *record* é apenas um termo técnico para qualquer item no DEVONthink), e cada record tem uma série de propriedades (*identificador único e universal*, *nome*, *aliases*, *tipo*, *extensão*, *url*, *etc*…). Além dessas propriedades, ou metadados básicos, ele permite ainda ao usuário criar seus próprios campos de metadados (e.g. *prioridade*, *projeto*, *comentário*, etc.). 

## Endereço dentro do programa

O *uuid* automático de cada record é único e universal. Ele aparece no link do record, formado por um prefixo especial, `x-devonthink-item://`, e o `UUID`. Esse link é como um link para um site, com a diferença que funciona apenas no seu próprio computador e que ele pode ser acessado a partir de qualquer programa. Se você ativá-lo ele irá ativar o programa e abrir o *record*. Essa função é excepcionalmente útil já que podemos agregar comandos ao link, como abrir e ir direto para uma página do PDF ou buscar uma palavra no arquivo de texto. Isso significa que sempre que eu citar uma determinada passagem, posso guardar não apenas a referência com a informação bibliográfica, mas também o link direto para a passagem em questão. Se estiver trabalhando com uma fonte primária, e se eu guardar esses textos das fontes primárias no programa -- que é o que eu faço -- é possível ter um atalho para as passagens mais importantes sempre à mão. Se eu vejo que em `EN VII 1` Aristóteles está citando o *Mênon* de Platão, eu posso criar uma nota com a referência do texto de Platão e associar um link direto para a linha relevante.

## Wiki links

Uma função interessante para quem utiliza arquivos de texto plano ou rtf, são os wiki links. *Wiki links são um tipo simplificado de link direto entre arquivos de texto*. A ideia é poder criar links para outros arquivos no próprio fluxo da escrita, sem precisar sair e consultar o endereço de um outro *record*. 

O DT pode operar com 3 tipos diferentes de wiki links. 

1. O primeiro tipo transforma em links apenas as palavras entre colchetes `[[link]]`. 
2. O segundo tipo transforma em link as palavras em `CamelCase` (e.g. `LiNk`). 
3. O terceiro tipo é um modo automático, que transforma em link a ocorrência de qualquer nome de arquivo (e.g. se eu tenho uma página chamada Platão, cada ocorrência do nome "Platão" em qualquer outro arquivo de texto vira um link). 

Com os dois primeiros métodos, é possível criar novos arquivos de texto a qualquer momento; basta colocar o nome da página entre colchetes ou em CamelCase. Essa é uma função muito comum em outros programas (na versão entre colchetes), como o *Connected Text* (para Windows), *Bear*, *Noteplan*, *Tinderbox*, *Notebooks*, *The Archive*, *nvUltra*. 

O terceiro tipo, por sua vez, é o que mais me interessa pessoalmente, por tornar possível manter um glossário de termos gregos e constultá-lo a qualquer momento durante a leitura. Do modo como eu construí o meu banco de dados, qualquer ocorrência de um termo grego (em qualquer uma das suas formas[^3]) vira um link para a página daquele conceito. Lá eu mantenho uma definição básica, a tradução que eu tenho preferido para o português, talvez a transcrição de uma passagem relevante do dicionário e links para outras passagem do *corpus* onde Aristóteles discute o conceito.

## Sugestões de leitura


* 📃 [How I use wiki-links and aliases](https://discourse.devontechnologies.com/t/how-i-use-wiki-links-and-aliases/47846) *Como eu uso o DT3 para manter uma Wiki com as fontes primárias e um glossário de termos e ocorrências.*  
* 📃 [How I use Wiki-Links and Aliases (pt.2)](https://discourse.devontechnologies.com/t/how-i-use-wiki-links-and-aliases-pt-2/47873) *Como eu liguei a numeração Bekker ao texto de Aristóteles de modo que cada ocorrência de uma referência válida (e.g. 1094a1 ou EN I.1) seja um link para a passagem referida.*  
  
# Automação

O propósito da automação é facilitar a execução de certas tarefas. Uma extensão que eu desenvolvi, por exemplo, me apresenta, sempre que eu abro um arquivo de texto, os demais arquivos que contém links para aquele arquivo que estou visualizando. São os *back links* ou *return links*. Outra extensão extrai em cada arquivo as referências *Bekker* no texto e as adiciona como *aliases* ao *record*. Isso significa que sempre que a referência, por exemplo, 1041a20 aparecer, ela será um link para EN VII 1. Isso reduz drasticamente a necessidade de criar novos links manualmente. No caso de Aristóteles, basta que eu cite a referência para que ela automaticamente apareça para mim como um atalho até ela. 

Automação no DEVONthink pode acontecer por diferentes caminhos: *smart-rules*, *templates* e *scripts*, sendo que o primeiro é o mais acessível para quem está começando e o último depende de algum conhecimento da linguagem *applescript* (que é relativamente simples).

## Smart rules

* [@Aliases](https://www.dropbox.com/s/v8o452g9ro5c81l/%40Aliases.dtSmartRule?dl=0) - Essa smart-rule procura no texto a linha que começar com `@` e adiciona seu conteúdo ao campo `aliases`.
* [@Bekker](https://www.dropbox.com/s/12as9gtww2xzz3z/%40Bekker.dtSmartRule?dl=0) - Essa smart-rule procura no texto qualquer referência dentro do padrão Bekker e adiciona ao campo `aliases`.
* [Auto return links](https://www.dropbox.com/s/4hlbyu54y1benbs/Return%20Links.dtSmartRule?dl=0) - Gera uma lista nos metadados do *record* A com todos os demais *records* B, C e D que contém um link até ele. São os *back links* ou *return links*.   
* [Filter empty-tags](https://www.dropbox.com/s/4q55onsy5k63291/Filter%20empty%20tags.dtSmartRule?dl=0) - Faz exatamente o que o nome indica: apaga tags que não tem nenhum arquivo associado a ela.  

Para que as smart-rules funcionem, você precisa ter o arquivo [RegexAndStuffLib.scptd](https://www.dropbox.com/sh/e1vrw5g272ibr35/AABi_JcnBoGxV5u81sV8RtNJa?dl=) na pasta `~/Biblioteca/Script Libraries`.

## Templates
* [Import reference as markdown](https://www.dropbox.com/sh/cuxn62rqv9ryvul/AAAzeRErIpxnxIngdEi5ivKra?dl=0) - Esse template serve para importar a referência selecionada no Bookends como arquivo em markdown.  
* [Corpus Aristotelicum](https://www.dropbox.com/sh/apr8yk4ltqgmpaq/AAC9FJkMtXjaVoAH7vSgViHQa?dl=0) - Esse template cria uma pasta para cada obra de Aristóteles com o título latino e o código TLG da obra.  
* [Corpus Platonicum](https://www.dropbox.com/sh/qyyd2ci6sgeysez/AADXH8DK87TISN8cisA7kAqea?dl=0) - Esse template faz o mesmo com as obras de Platão.

## Applescripts
  
[DT3 Copiar link para linha ou palavra do documento](dt3-link) - Abre uma caixa de diálogo com três opções de link a serem copiados para a área de transferência.  
[DT3 Copiar referência da página do PDF em RTF](dt3-link-pag-rtf) - Apresenta uma caixa de diálogo solicitando o número correto da página que deve aparecer na citação em rtf gerada. A referência é extraída do Bibkey ou dos aliases ou do próprio título, nessa ordem de prioridade.  
[DT3 Criar nova nota em Markdown a partir da seleção](dt3-new-md) - Cria um novo arquivo markdown utilizando o texto selecionado como título e o conteúdo da área de transferência como corpo do texto.    
[DT3 Criar versão do record ](dt3-versão) - Cria uma versão datada do *record* na pasta backup.  
[DT3 Restaurar versão do record](dt3-restaurar) - Procura pelas versões do *record* na pasta backup que pode ser recuperadas.  
[DT3 Tag Selector](dt3-tag-selector) - Script gera uma lista de tags existentes no banco de dados para serem escolhidas e aplicadas ao *record* selecionado.  
[DT3 To Bookends.scpt](https://www.dropbox.com/s/7oq8fmzpb1rigb8/To%20Bookends.scpt?dl=0) - Script que   transfere os metadados do *record* selecionado no DEVONthink e transfere para a entrada selecionada no *Bookends*.
  
[^1]: *Record* é o termo técnico para qualquer item dentro de um banco de dados do DEVONthink.
[^2]: Você pode facilmente adaptar o script para extrair a numeração utilizada na edição de referência do seu autor. No caso da numeração *Bekker*, o padrão é `\d*[a|b]\d\d`. Para entender o significado dessa expressão, veja a página sobre [RegEx](regex). 
[^3]: Possível graças aos *aliases* onde mantenho as formas declinadas dos termos. 