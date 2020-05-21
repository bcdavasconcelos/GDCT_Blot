tags: Escrita, Apps  
permalink: /word

# Por que deveríamos parar de usar o Word  
  
## Dois problema com os formatos rtf e docx  
Uns tempos atrás, precisei lidar com arquivos de texto grandes. *Muito grandes*. Para se ter uma ideia, um desses arquivos, que continha todo o *Corpus Aristotelicum*, tinha mais de 6 milhões de caracteres (equivalente a mais de 1 milhão de palavras) e "pesava" mais de 19 MB em formato *txt*. Ou seja, **sem qualquer tipo de formatação e sem nenhuma imagem**.  
  
Programas como o Microsoft Word não são *sequer* capazes de abrir um arquivo tão grande. Nem o são programas como Open Office, Libre Office & semelhantes. Esses são programas úteis, sem dúvidas, mas padecem da mesma falha fundamental: operam apenas a partir do princípio WYSIWYG (*What You See Is What You Get*).  
  
Dizendo de outro modo, *são programas que gastam uma quantidade enorme de recursos — e que ocupam constantemente o usuário — com a tarefa de formatar e cuidar da aparência do texto.* Isso é um problema por dois motivos:  
  
Em primeiro lugar, a tentativa de ter-se um software capaz de fazer absolutamente tudo — desde oferecer ao usuário um local para capturar o texto até compilar o produto final — resulta em programas com alta demanda de recursos, propensos a toda sorte de problemas — sobretudo a fecharem abruptamente por algum erro fatal ou pelo esgotamento da capacidade de processamento da máquina.  
  
Em segundo lugar, há uma demanda sendo constantemente imposta aos usuários de se ocuparem de tarefas cosméticas de formatação que estão fadadas a serem repetidas inúmeras vezes até o produto final ser alcançado. É verdade que com um pouco de treinamento no uso dos estilos e dos templates essa tarefa pode ser mitigada, mas mesmo aqueles de nós que fazem uso dessa ferramenta perdem um tempo considerável lutando contra tabelas mal posicionadas, notas de rodapé fora do lugar, espaçamento disforme, estilos mal aplicados, enfim. Quando se concerta um problema, criam-se outros dois.  
  
A despeito de tudo isso, o poder de empresas como a *Microsoft* é tão grande que muitos, na academia e fora dela, não conseguem sequer conceber a possibilidade de escrever utilizando alguma ferramenta diferente do *Microsoft Word*. Quando muito, utiliza-se a versão gratuita de código aberto que tenta ao máximo imitar o modelo da versão paga. Optar pelo software livre é uma excelente ideia, claro, mas como espero ter deixado claro, esse não é o problema real. Não há sentido em mudar para a versão gratuita de código aberto de um modelo ruim de software.  
  
Mas se o não com o *Word*, então como...?  
  
  
## Sugestão: escreva em Markdown  
  
Para escrever em markdown você pode utilizar absolutamente qualquer programa de texto, do bloco de notas aos [editores de texto](editores-de-texto), passando pelos [editores](editores-de-markdown) desenvolvidos especificamente para markdown que são bastante úteis.  
  
Markdown é uma linguagem de marcação[^1] minimalista [criada em 2004](https://daringfireball.net/projects/markdown/) por [John Gruber](https://en.wikipedia.org/wiki/John_Gruber) e [Aaron Swartz](http://www.aaronsw.com/weblog/001189) com o propósito de possibilitar a geração de texto *html* — i.e. *hypertext markup language*, a principal linguagem utilizada na internet — a partir de um texto legível e com poucas distrações. O que começou como uma linguagem de marcação, digamos, anêmica e voltada apenas para a internet, evoluiu para uma linguagem extremamente popular com um bom conjunto de funcionalidades, capaz de satisfazer todas as necessidades do mundo científico e acadêmico. Hoje, graças ao Pandoc, já é mais fácil produzir um PDF de excelente qualidade tipográfica no padrão ABNT a partir de um texto plano escrito em Markdown do que utilizando o Microsoft Word.  
  
## Formatando um texto com markdown  
  
### Títulos de seções  
  
São marcados com `#`.  
Exemplo:  
  
```  
# Título  
## Subtítulo  
### Subsubtítulo  
#### Etc...  
```  
  
### Citações  
  
São indicadas pelo maior `>`.  
Exemplo:  
  
```  
 > Lorem ipsum…  
```  
  
### Notas de rodapé  
  
Podem ser feitas de mais de um modo.  
Exemplo 1:  
  
```  
Lorem ipsum[^texto da nota de rodapé].  
```  
  
Exemplo 2:  
```  
Lorem ipsum[^1].  
Etc.  
  
[^1]: Texto da nota de rodapé.  
```  
  
### Ênfase  
  
Pode variar, mas no geral é feita com um único asterisco antes e depois para *itálico* e dois asteriscos para **negrito**.  
Exemplo:  
  
```  
*Texto em itálico* e **texto em negrito**.  
```  
  
### Listas  
A lista ordenada é indicada por um número `1.` e a lista não ordenada pelo asterisco.  
  
```  
1. Item 1  
1. Item 2  
  
* item  
* item  
```  
  
  
![Multimarkdown Composer](/Imagens/mmd.png)  
  
Há bastante material na internet sobre markdown e seus diferentes sub-tipos, mas tudo que você precisa saber está nesse resuminho aí em cima.  
  
[^1]: Ou seja, é um modo de escrever indicando a estrutura e a formatação no próprio corpo do texto.
