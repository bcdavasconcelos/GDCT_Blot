tags: Fontes primárias, TLG  
hashtags: #Fontes-primárias, #TLG  
permalink: /tlg-intro

# Thesaurus Linguae Graecae  

O [TLG](http://www.tlg.uci.edu) é um projeto da Universidade da California e um *serviço por assinatura online* que fornece acesso à maior parte dos textos gregos antigos que sobreviveram. Parte do corpus de textos na base de dados pode ser livremente acessado criando um login, mas acesso ao corpus completo sai por US$140/ano por pessoa. No hemisfério norte, a maior parte das universidades com programas de clássicos mantém uma assinatura institucional que pode ser livremente utilizada pelos alunos.  

Uma versão desatualizada do banco de dados circula há anos na internet e no meio acadêmico. Essa versão é a de 1999, época em que a distribuição ainda acontecia por CD-ROM. Nela, o banco de dados é composto por milhares de arquivos de texto plano[^1] em um formato conhecido como betacode[^2]. O famoso software [Diogenes](https://d.iogen.es/d/download.html) foi desenvolvido para possibilitar a visualização desse banco de dados em formato unicode e a navegação em um ambiente integrado ao dicionário Liddell Scott.  

O arquivo com o texto em *betacode* pode facilmente ser convertido para unicode usando o próprio Diogenes, ou com o [betacode Converter](https://cental.uclouvain.be/beta2uni/#extended). Essa última opção gera um resultado superior, mas não pode ser utilizada com mais de um arquivo por vez. Para maiores informações, veja o artigo [extraindo textos do TLG](tlg-betacode).  

## Sistema de identificação  
O TLG possui um sistema de identificação universal dos autores e obras. Autores tem um código de 4 dígitos[^3] e as obras um código de 3 dígitos.  

| Autor              | Cód. | Obra        | Cód. |  
| ------------------ | ---- | ----------- | ---- |  
| Apollonius Rhodius | 0001 | Argonautica | 001  |  
| Apollonius Rhodius | 0001 | Fragmenta   | 002  |  
| Apollonius Rhodius | 0001 | Epigrammata | 003  |  
| Theognis           | 0002 | Elegiae     | 001  |  
| Theognis           | 0002 | Epigrammata | 004  |  
| Thucydides         | 0003 | Histories   | 001  |  
| Thucydides         | 0003 | Epigramma   | 002  |  
|[*Ver a lista completa*](tlg-ref)|

Se Aristóteles é o autor **0086** e a *Physica* é a obra **031**, então, no sistema de referência do TLG, o identificador universal da *Physica* de Aristóteles é **0086.031**. Esse código é utilizado pelos URLs do site do TLG[^4] e do Diogenes[^5], no [Perseus Catalog](https://catalog.perseus.org) e nas referências utilizando a [arquitetura CITE](http://cite-architecture.github.io/about/).[^6]  

## Ferramentas especiais  
O TLG online oferece algumas ferramentas especiais para análise dos textos. São várias ferramentas com diversas configurações possíveis, de modo que não seria possível fazer aqui um relatório de todas elas. Eis algumas particularmente interessantes:

- Em cada página de texto, a plataforma automaticamente oferece sugestões de outros textos do corpus que contém frases semelhantes. A análise pode ser feita a partir dos lemmas, ignorando a ordem e desconsiderando [as palavras mais comuns](https://github.com/aurelberra/stopwords/blob/master/revision_notes.md#greek-stopwords), ou considerando a forma das palavras declinadas.

![](https://www.dropbox.com/s/s6wy6t5lxtfcdxe/2020-04-12_18-49-29.png?raw=1)

- A mesma análise pode ser feita em duas ou três obras específicas gerando um relatório de todas as passagens semelhantes com base nos critérios escolhidos (e.g. distância possível entre os termos). São os chamados [N-GRAMS](http://stephanus.tlg.uci.edu/helppdf/ngrams.pdf).
- Há diversas opções de gráficos para a visualização de dados relativos à ocorrências de um determinado lemma, e.g. ocorrências por século, por região, por autor, etc.

Mais informações podem ser encontradas [aqui](http://stephanus.tlg.uci.edu/help.php)

## Limitações do TLG  
Uma das principais limitações do TLG é a ausência do aparato crítico que acompanha os textos. Essa limitação provavelmente[^9] se deve ao fato do aparato ser protegido por leis de direitos autorais e pertencer, portanto, à editora. A questão da aplicabilidade da lei de direitos autorais com relação a um texto antigo é complexa e controversa. A prática corrente, ao que tudo indica, é considerar que o texto não está protegido, por ser de um autor antigo, mas o aparato sim, por ser fruto do trabalho de um editor vivo ou falecido no passado recente (>100 anos). Para ter acesso ao aparato, não há outra opção que não a aquisição da edição impressa ou do download de um arquivo em PDF.  

Se você leu com atenção as seções acima, deve ter percebido que uma outra limitação importante para aqueles que usam o *banco de dados offline* ou *a versão gratuita online* é o **tamanho do corpus**.  

Para ficar em um único exemplo sobre a importância disso: quem efetua uma busca pela *República* de Platão, encontra a edição de John Burnet de 1902[^7]. Na versão completa, **a versão de Burnet sequer aparece nos resultados**. A edição de referência disponível é a do S. R. Slings de 2003[^8]. Ou seja, versão recente fica para os assinantes; o resto do mundo precisa contentar-se com a de 118 anos atrás.  

Felizmente, esse estado de coisas está mudando e já está em desenvolvimento um projeto mais democrático e aberto chamado [First Thousand Years of Greek and Latin](https://opengreekandlatin.github.io/First1KGreek/).  

[^1]: São arquivos sem formatação (como acontece quando usamos *rich text formating*) que usam a extensão `.txt`.  
[^2]: Esse formato foi desenvolvido por David Packard (filho do engenheiro Packard que fundou a Hewlett-Packard, a.k.a. HP.) para grafar o grego politônico usando caracteres ASCII.  
[^3]: Se você entrar na pasta de textos do banco de dados do TLG, perceberá que os arquivos estão numerados de acordo com o código do respectivo autor.  
[^4]: Links do TLG tem a seguinte estrutura:  
  "http://stephanus.tlg.uci.edu/Iris/indiv/browser.jsp#doc=tlg&aid=AUTORwid=OBRA&st=0".  
  Logo, para a Physica {0086.031} teríamos:  
  "http://stephanus.tlg.uci.edu/Iris/indiv/browser.jsp#doc=tlg&aid=0086&wid=031&st=0".  
[^5]: O Diogenes na verdade funciona como um servidor e como um navegador. Faça um experimento, abra o Diogenes e depois vá até seu browser (*e.g.* Safari, Firefox, Chrome, *etc.*) e acesse [http://localhost:8888/Diogenes.cgi](http://localhost:8888/Diogenes.cgi).  
[^6]: A arquitetura CITE foi desenvolvida para resolver um problema antigo da internet: links quebrados. Basta abrir uma página de alguns anos atrás para perder qualquer esperança de encontrar links funcionando. Essa arquitetura pretende estabelecer um padrão na referência a textos antigos de modo a preservar a ligação e mantê-la sempre funcionando. O exemplo que demos acima da ilustra isso: qualquer link com o código **0086.031** deve apontar para a *Physica* de Aristóteles, não importa onde o texto esteja hospedado, basta ter um sistema capaz de processar essa informação; i.e. um sistema compatível com a arquitetura CITE.  
[^7]: Respublica {0059.030} Platonis opera, vol. 4. Ed.: John Burnet. Oxford: Clarendon Press, 1902
[^8]: Respublica {0059.042} Platonis Respublicam. Ed.: S. R. Slings. Oxford: Uni Press, 2003
[^9]: A prioridade do projeto claramente não é essa, mas sim expandir o corpus para incluir textos de outras fases da literatura grega (e.g. bizantina/medieval).   
