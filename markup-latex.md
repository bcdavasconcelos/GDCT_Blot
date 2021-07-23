permalink: /latex
tags: Linguagens de marcação

# LaTeX

<script src="prism.js"></script>

Pronuncia-se *latek/lateq* e não *látex* ou *latex/latequis*. É um sistema de tipografia de alta qualidade, utilizado para preparar livros e artigos para publicação. Nas ciências naturais e na matemática é muito comum alunos/as aprenderem desde cedo a escrever utilizando LaTeX para facilitar o trabalho com equações. Nas ciências humanas dificilmente encontramos a oferta ou a exigência de conhecimentos sobre LaTeX. Apesar disso, há inúmeras vantagens de conhecer e aprender um pouco sobre esse sistema. Aqui listarei algumas poucas referências úteis para quem quiser se aventurar. O universo do LaTeX é vasto e dominar os principais recursos desse sistema demanda tempo e muita disposição para ler documentação.

## Instalando LaTeX

- MacOS: [MacTeX](http://www.tug.org/mactex/)
- Windows: [MiKTeX](https://miktex.org), [TeXLive](http://www.tug.org/texlive/), [ProTeX](http://www.tug.org/protext/)
- Linux: [TeXLive](https://www.tug.org/texlive)

## Primeiros passos

- [ABNTex-o-matic](https://github.com/bcdavasconcelos/ABNTeX-o-matic) - Template para teses e dissertações que preparei para auxiliar na conversão de [markdown](markdown) para PDF. Se você não tem interesse em aprender LaTeX e quer apenas um template para conversão com [Pandoc](https://pandoc.org), esse é o melhor caminho.
- [WikiBooks: Latex](https://en.wikibooks.org/wiki/LaTeX)
- [The LaTeX Project](https://www.latex-project.org)
- [Overleaf](https://www.overleaf.com/) - Obs.: Estudantes podem criar uma conta gratuita.
- [LaTeX for Humanities](https://www.overleaf.com/blog/636-guest-blog-post-latex-for-the-humanities)

## Alguns pacotes dignos de nota

- [Polyglossia](https://ctan.org/pkg/polyglossia) - Para utilizar mais de uma língua no documento e manter a hifenização funcionando corretamente.
- [HyperRef](https://ctan.org/pkg/hyperref) - Para a criação de ligações internas no documento.
- [Glossaries](https://ctan.org/pkg/glossaries) - Para a criação de um glossário no seu trabalho.
- [Schemata](https://ctan.org/pkg/schemata) - Preparação de diagramas no estilo utilizado pelos escribas da idade média. 
- [Reledmac](https://ctan.org/pkg/reledmac) e [reledpar](https://ctan.org/pkg/reledpar) - Para a preparação de edições críticas.
- [Ekdosis](https://ctan.org/pkg/ekdosis) - Também para a preparação de edições críticas, mas desta vez utilizando [TEI-XML](https://teipublisher.com/index.html).
- [MicroType](https://ctan.org/pkg/microtype) - Para controlar alguns detalhes da tipografia da fonte e deixar o documento mais agradável de ler.


## Alguns pacotes indispensáveis

- [Geometry](https://ctan.org/pkg/geometry?lang=en) - Para controlar a configuração das margens do documento.
- [KOMA-SCRIPT](https://ctan.org/pkg/koma-script) - Trata-se de uma substituição das classes tradicionais do documentos em LaTeX (e.g. livro, artigo, carta, relatório) que oferece maior flexibilidade e melhor qualidade tipográfica.
    - [scrbook](https://ctan.org/pkg/scrbook) - Documentação da classe "livro" do KOMA-SCRIPT.


## BibLaTeX

- [BibLaTeX Philosophy](https://ctan.org/pkg/biblatex-philosophy) - Esse é o melhor pacote disponível para processar bibliografia usando [BibLaTeX](https://ctan.org/pkg/biblatex) em trabalhos de filosofia. Altamente recomendado.
- Demais estilos (*e.g.* ABNT, APA, Chicago, Oxford, *etc*) para [BibLaTeX](https://ctan.org/topic/biblatex)

## Templates

Templates são muito bons para aprender sobre LaTeX, pois é muito mais fácil modificar um template existente do que começar um do zero. Muitas vezes, o código possui comentários que ajudam a elucidar a função da cada item.

- [Mimosis](https://github.com/Pseudomanifold/latex-mimosis)
- [Kaobook](https://github.com/fmarotta/kaobook)
- [novathesis](https://github.com/joaomlourenco/novathesis)
- [Eisvogel](https://github.com/Wandmalfarbe/pandoc-latex-template)
- [ElegantBook](https://ctan.dcc.uchile.cl/macros/latex/contrib/elegantbook/elegantbook-en.pdf)
- [Tufte](https://github.com/Tufte-LaTeX/tufte-latex)


## Exemplo de arquivo LaTeX


```language-latex

\documentclass[12pt]{article}

\begin{document}

\section{Primeira seção}

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

\end{document}


```