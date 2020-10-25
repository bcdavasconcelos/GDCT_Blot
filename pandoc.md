tags: Automação, Escrita, Pandoc
hashtags: #Automação, #Escrita, #Pandoc
permalink: /pandoc

# Pandoc
[Instruções para instalar o Pandoc](https://pandoc.org/installing.html)

## Conversão simples de Markdown para PDF
Execute o seguinte comando no terminal/shell:  

```Bash+shell
pandoc -s -f markdown SeuArquivo.md --pdf-engine=xelatex -o SeuPDF.pdf
```

Entendendo o comando:

`-s`  stand-alone — Indica para o Pandoc que você deseja um arquivo como produto final da conversão. (Dependendo da conversão, o resultado poderia ser apenas um texto convertido na própria janela do termina/shell).

`-f`  from — É o formato a partir do qual se converte (e.g. markdown / docx / html / gfm / etc) que deve ser seguido pelo nome do arquivo a partir do qual se converte (e.g. documento.md).

`-o` output — É o resultado desejado, no nosso caso, um PDF (ver próximo item). 

`—pdf-engine=xelatex` — Como a conversão direta entre markdown e PDF não é possível, precisamos fazê-la via Latex ou HTML. A minha sugestão é usar XeLaTeX, pois tem a vantagem de suportar caracteres gregos e utilizar fontes do sistema
Atenção: você precisa ter os pacotes LaTeX instalados. E.g. http://www.tug.org/mactex/MacTex. 

<br>

---

<br>

## Adicionando Variáveis

```Bash
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

---

<br>

## Bibliografia

```bash
"--csl=$HOME/path/csl/chicago-author-date.csl" \
"--bibliography=$HOME/path/all.json"
```

`"--csl=$HOME/path/csl/chicago-author-date.csl"` Esse é o caminho para o estilo (e.g. APA, Chicago, ABNT, etc) que deverá ser utilizado (em formato CSL, como o Zotero).  
`"--bibliography=$HOME/path/all.json"` Esse é caminho para o arquivo com as referências bibliográficas, que pode estar em BibTeX ou JSON (preferível).  

<br>

---

<br>

## Includes (transclusão)

```bash
"--lua-filter=$HOME/path/include-files.lua"
```

Para fazer transclusões usando o pandoc, é preciso usar um [filtro adicional em lua](https://github.com/pandoc/lua-filters) no comando.  

