tags: Organização, Apps, macOS, DEVONthink  

# DEVONthink 3  

![DEVONthink 3](/Imagens/dt.png)  
  
1. **🕸️** [DEVONthink Pro 3](https://www.devontechnologies.com/apps/devonthink/new) () *Um software com diversas funcionalidades e que pode ser utilizado para construir uma Wiki. Funciona bem com o Bookends.*  
	1. 📃 [How I use wiki-links and aliases](https://discourse.devontechnologies.com/t/how-i-use-wiki-links-and-aliases/47846) *Como eu uso o DT3 para manter uma Wiki com as fontes primárias e um glossário de termos e ocorrências.*  
	2. 📃 [How I use Wiki-Links and Aliases (pt.2)](https://discourse.devontechnologies.com/t/how-i-use-wiki-links-and-aliases-pt-2/47873) *Como eu liguei a numeração Bekker ao texto de Aristóteles de modo que cada ocorrência de uma referência válida (e.g. 1094a1 ou EN I.1) seja um link para a passagem referida.*  
	3. 🔧 [Three Keyboard Maestro Macros for dealing with aliases  one for Pandoc](https://discourse.devontechnologies.com/t/three-keyboard-maestro-macros-for-dealing-with-aliases-one-for-pandoc/48062) *Ferramentas utilizadas para automatizar os processos envolvidos na construção da Wiki*  
  
  
# Ampliando as funções do DT3 
## Smart rules
* [@Bekker](https://www.dropbox.com/s/12as9gtww2xzz3z/%40Bekker.dtSmartRule?dl=0)  
Essa smart-rule contém um script que extrai a numeração do texto grego da edição Bekker das obras de Aristóteles.   




As possibilidades de links indiretos são inúmeras. Desde a utilização de tags com palavras chaves, etiquetas coloridas, buscas salvas/smart groups a partir de critérios de vários tipos. Eles são úteis para reunir trechos do corpus que discutem temas próximos, mas em obras diferentes.



/ novos campos de metadados customizados, como, por exemplo, "prioridade", "ano", etc. os itens em um banco de dados são *records*. Os records tem uma série de propriedades contidas no texto que seguem o padrão da numeração Bekker[^2] e adiciona como aliases[^3]. Para que a smart-rule funcione, você precisa ter o arquivo [RegexAndStuffLib.scptd](https://www.dropbox.com/sh/e1vrw5g272ibr35/AABi_JcnBoGxV5u81sV8RtNJa?dl=0) na pasta `~/Biblioteca/Script Libraries`.


## Applescript
  
DT3 Copiar link para linha ou palavra do documento  
DT3 Copiar referência da página do PDF em RTF  
DT3 Criar nova nota em Markdown  
DT3 Criar versão do record  
DT3 Restaurar versão do record  
Search Operators in DEVONthink  
  
[^1]: *Record* é o termo técnico para qualquer item dentro de um banco de dados do DEVONthink.
[^2]: Você pode facilmente adaptar o script para extrair a numeração utilizada na edição de referência do seu autor. No caso da numeração Bekker, o padrão é `\d*[a|b]\d\d`. Para entender o significado dessa expressão, veja a página sobre [RegEx](regex). 
[^3]: Aliases são nomes alternativos para o *record*. Quanto utilizamos wiki links automáticos, os aliases são úteis para que mais de um nome possa ser utilizado como link para um *record*. Exemplo: se eu tenho um record chamado Ethica Nicomachea I 3, e adicionar a referência 1094b12 como alias, então todas as ocorrências no meu banco de dados das expressões `Ethica Nicomachea I 3` e `1094b12` serão links para esse record.
[^4]: UUID = *Universally unique identifier*.
