tags: Automação, Escrita, Pandoc
hashtags: #Automação, #Escrita, #Pandoc
permalink: /pandoc

# Pandoc

<script src="prism.js"></script>

[Instruções para instalar o Pandoc](https://pandoc.org/installing.html)

## Conversão simples de Markdown para PDF

Execute o seguinte comando no terminal/shell:  

```language-bash
pandoc -s -f markdown SeuArquivo.md --pdf-engine=xelatex -o SeuPDF.pdf
```

Entendendo o comando:

`-s`  stand-alone — Indica para o Pandoc que você deseja um arquivo como produto final da conversão. (Dependendo da conversão, o resultado poderia ser apenas um texto convertido na própria janela do terminal/shell).

`-f`  from — É o formato a partir do qual se converte (e.g. markdown / docx / html / gfm / etc) que deve ser seguido pelo nome do arquivo a partir do qual se converte (e.g. documento.md).

`-o` output — É o resultado desejado, no nosso caso, um PDF (ver próximo item).

`—pdf-engine=xelatex` — Como a conversão direta entre markdown e PDF não é possível, precisamos fazê-la via Latex ou HTML. A minha sugestão é usar XeLaTeX, pois tem a vantagem de suportar caracteres gregos e utilizar fontes do sistema
Atenção: você precisa ter os pacotes LaTeX instalados. E.g. http://www.tug.org/mactex/MacTex.

<br>

## Adicionando Variáveis

```language-bash
pandoc -s -f markdown SeuArquivo.md \
--pdf-engine=xelatex \
-V 'mainfont=Gentium Plus' \
-V 'sansfont=Source Sans Pro' \
-V 'monofont=Menlo' -V 'fontsize=13pt' \
-V 'geometry: top=3cm, left=3cm, right=2cm, bottom=2cm' \
-V 'linestretch:1.5' \
-V 'pagestyle:headings' \
--toc -o SeuPDF.pdf
```

`-V` variable — Indica uma variável a ser inserida durante a conversão. Sempre lembrar de colocar o valor entre aspas simples.

`mainfont=Gentium Plus` — Qualquer fonte do sistema pode ser utilizada com XeLateX. Para arquivos com textos em grego, eu gosto das seguintes fontes: Gentium Plus, Alegreya, EB Garamond e Linux Libertine. Você encontra todas elas [aqui](fontes-tipograficas).

`sansfont=Source Sans Pro` — Fonte sem serifa de escolha.

`monofont=Menlo` — Fonte de largura fixa de sua preferência. Recomendo Menlo, TheSansMono Office, DejaVu Sans Mono.

`geometry: top=3cm, left=3cm, right=2cm, bottom=2cm` — Pacote geometry para LaTex com a formatação da página configurada de acordo com a ABNT.

`linestretch:1.5` — Espaçamento entre linhas.

`pagestyle:headings` — Estilos diferentes de páginas: com cabeçalho, padrão e sem nada (headings / plain / empty).

`—toc` — Incluir *table of contents*.

`-V linkcolor:blue`

<br>


## Referências internas

Para facilitar as referências internas, podemos utilizar um filtro chamado [Pandoc Secnos](https://github.com/tomduck/pandoc-secnos) parte do pacote [Xnos](https://github.com/tomduck/pandoc-xnos). Depois de instalar o filtro ([instruções estão no repositório do pacote no github](https://github.com/tomduck/pandoc-secnos#installation)), basta evocar a bandeira `--filter pandoc-secnos` no comando. Isso deve necessariamente acontecer ANTES dos comandos relacionados à bibliografia, listados abaixo.

<br>

## Bibliografia

```language-bash
"--csl=$HOME/path/csl/chicago-author-date.csl" \
"--bibliography=$HOME/path/all.json"
```

`"--csl=$HOME/path/csl/associacão-brasileira-de-normas-tecnicas-para-estudos-classicos.csl"` Esse é o caminho para [o estilo](csl-abnt) (e.g. APA, Chicago, ABNT, etc) que deverá ser utilizado (em formato CSL, como o Zotero).  
`"--bibliography=$HOME/path/all.json"` Esse é caminho para o arquivo com as referências bibliográficas, que pode estar em BibTeX ou JSON (preferível).  


<br>

## Includes (transclusão)

```language-bash
"--lua-filter=$HOME/path/include-files.lua"
```

Para fazer transclusões usando o pandoc, é preciso usar um [filtro adicional em lua](https://github.com/pandoc/lua-filters) no comando.  



## Referências

- [Plain Text, Papers, Pandoc](https://kieranhealy.org/blog/archives/2014/01/23/plain-text/)
- [Formatting Open Science: agilely creating multiple document formats for academic manuscripts with Pandoc Scholar](https://peerj.com/articles/cs-112/)