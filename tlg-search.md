permalink: /tlg-search
tags: TLG, Fontes primárias, 
hashtags: #TLG, #Fontes primárias

# Como fazer buscas no TLG

*Atualizado em 4 de jan. de 2021 11:28:03*

*Nesse breve artigo explico alguns pontos importantes sobre a [pesquisa nos textos do TLG Online](http://stephanus.tlg.uci.edu/Iris/demo/tsearch.jsp)*.

Todas as buscas no TLG Online têm o seguinte comportamento:

- Ignoram pontuação.
- Ignoram diacríticos (acentos e espíritos).
- Ignoram se as letras são maiúsculas ou minúsculas.
- Podem ser feitas utilizando o alfabeto grego ou latino (obs.: para escrever utilizando o alfabeto latino, use o [betacode](https://en.wikipedia.org/wiki/Beta_Code)).

Para reverter qualquer um desses comportamentos, você pode marcar as opções que ficam sob o campo de busca:

- **Case sensitive** torna a busca sensível a letras maiúsculas e minúsculas.
- **Diacritics sensitive** torna a busca sensível a acentos e espíritos.
- **Exact match** evita que o termo buscado seja parte de um termo maior nos resultados. Ou seja, essa opção torna a busca sensível à fronteira entre as palavras.   


## Word index

A busca usando o "Word Index" acontece em uma lista de palavras do TLG. Ou seja, é como se a sua busca estivesse acontecendo em uma lista de palavras. Os termos são confrontados com os termos da lista de palavras e as passagens nas quais eles ocorrem são retornadas. É possível buscar por um único termo ou mesmo por uma frase inteira.

Para exemplificar, eis um fragmento de Parmênides:  

> ἡ δὲ κρίσις περὶ τούτων ἐν τῷδ’ ἔστιν·  
> ἔστιν ἢ οὐκ ἔστιν

Para todos os fins, é como se a busca ocorresse na seguinte lista:

> δὲ   
> ἐν    
> ἔστιν  
> ἢ  
> ἡ   
> κρίσις   
> οὐκ  
> περὶ   
> τούτων   
> τῷδ’       

Toda sequência de caracteres buscada será tomada como início de uma palavra da lista. Se a sequência ocorrer em um item, ainda que não coincida com a palavra inteira, ele aparecerá nos resultados.  


### Exemplo  

Se eu buscar por **`ανδρ`** eu terei como resultado: <mark>ἄνδρ</mark>α, <mark>ἄνδρ</mark>ας e <mark>ἀνδρ</mark>άσι (sempre lembrando que a posição dos acentos é completamente ignorada).

### Em resumo  

- É uma pesquisa em uma lista.
- O início da sequência de busca deve necessariamente equivaler ao resultado almejado.
- Não há necessidade de utilizar diacríticos (espíritos e acentos).
- No caso de busca por uma frase, não há necessidade de utilizar pontuação. 


## Lemma

Esse modo de busca usa lemmata (entradas dos dicionários indexados pelo TLG) como referência. Se você buscar por uma palavra (note que o auto-completar está ativo e pode servir de auxílio), e ela existir em um dos dicionários, o TLG irá evocar todas as formas conhecidas da palavra e buscar por todas elas.

### Exemplo  

Assim que uma sequência de caracteres é registrada, e.g. **`λε`**, uma lista de opções aparece. Escolhendo o termo **`λέγω`**, o TLG buscará por:

```
ἔλεγ, ἔλεγε, ἔλεγεν, ἔλεγες, ἐλέγεσθε, ἐλέγετ, ἐλέγετε, ἐλεγέτην, ἐλέγετο, ἐλέγευ, ἐλέγομεν, ἔλεγον, ἐλέγοντο, ἐλέγου, ἐλέλεκτο, ἔλεξ, ἔλεξα, ἐλέξαμεν, ἐλεξάμην, ἔλεξαν, ἔλεξας, ἐλέξατο, ἔλεξε, ἔλεξεν, ἐλέχθη, ἐλέχθην, ἐλέχθησαν, κἄλεξας, λέγ, λέγε, λέγεθ, λέγει, λέγειν, λέγεις, λέγες, λέγεσθαι, λέγεσθε, λέγεσθον, λεγέσθω, λεγέσθωσαν, λέγετ, λέγεται, λέγετε, λέγετον, λεγέτω, λεγέτωσαν, λέγῃ, λέγηθ, λέγῃς, λέγητ, λέγηται, λέγητε, λέγοι, λέγοιεν, λέγοιθ, λέγοιμ, λεγοίμεθα, λέγοιμεν, λεγοίμην, λέγοιμι, λέγοιντ, λέγοιντο, λέγοις, λέγοισα, λεγοίσθην, λέγοιτ, λέγοιτο, λέγομαι, λεγόμεθα, λεγόμεν, λέγομεν, λεγόμενα, λεγόμεναι, λεγομέναις, λεγομένας, λεγομένη, λεγομένῃ, λεγομένην, λεγομένης, λεγόμενοι, λεγομένοις, λεγομένοισι, λεγόμενον, λεγόμενος, λεγομένου, λεγομένους, λεγομένω, λεγομένῳ, λεγομένων, λέγομες, λεγον, λέγον, λέγονθ, λέγοντ, λέγοντα, λέγονται, λέγοντας, λέγοντε, λέγοντες, λέγοντι, λέγοντο, λεγόντοιν, λέγοντος, λεγόντων, λέγουσ, λέγουσα, λέγουσαι, λεγούσαις, λέγουσαν, λεγούσας, λεγούσῃ, λεγούσης, λέγουσι, λέγουσιν, λεγουσῶν, λέγω, λεγώμεθ, λεγώμεθα, λέγωμεν, λέγωμες, λέγων, λέγωνται, λέγωντι, λέγωσ, λέγωσι, λέγωσιν, λέλεγμαι, λελεγμένα, λελεγμένῃ, λελεγμένης, λελεγμένοι, λελεγμένοις, λελεγμένον, λελεγμένος, λελεγμένου, λελεγμένους, λελεγμένων, λέλεκται, λέλεκτο, λελέξεται, λελέξομαι, λελέχθαι, λελέχθω, λέξαθ, λέξαι, λέξαιμ, λεξαίμην, λέξαιμι, λέξαις, λέξαιτο, λεξάμεναι, λεξάμην, λέξανθ, λέξαντα, λέξαντες, λέξαντος, λεξάντων, λέξασ, λέξασα, λέξασθαι, λεξάσθην, λεξάσθων, λέξατε, λέξατο, λεξάτω, λέξεαι, λέξει, λέξειαν, λέξειας, λέξειε, λέξειεν, λέξειν, λέξεις, λέξεται, λέξετε, λεξέων, λέξεων, λέξῃ, λέξῃς, λέξητε, λέξοιεν, λέξομαι, λέξομεν, λέξον, λέξονθ, λέξοντ, λέξοντα, λέξοντας, λέξοντες, λέξοντι, λεξοῦντι, λέξουσ, λέξουσι, λέξουσιν, λέξω, λέξωμεν, λέξων, λεχθείη, λεχθείς, λεχθεῖσα, λεχθεῖσαι, λεχθεῖσαν, λεχθείσας, λεχθεισέων, λεχθείσῃ, λεχθείσης, λεχθείσῃσι, λεχθεῖσι, λεχθεῖσιν, λεχθεισῶν, λεχθέν, λεχθέντα, λεχθέντας, λεχθέντε, λεχθέντες, λεχθέντι, λεχθέντος, λεχθέντων, λεχθῇ, λεχθῆναι, λεχθήσεσθαι, λεχθήσεται, λεχθήσομαι, λεχθησόμενα, λεχθησομέναις, λεχθησομένην, λεχθησομένοις, λεχθησομένου, λεχθησομένων, λεχθῶσιν
```

É possível também ignorar o autocompletar. Fazendo uma busca por `ἐλέχθην`, por exemplo, o TLG corretamente identifica o lemma como sendo o verbo `λέγω` e procede a buscar pelas formas conhecidas.


### Em resumo  

- Função autocompletar ativada.
- A busca é apenas por um termo.
- Se você estiver pesquisando um conceito específico e quiser encontrar todas as ocorrências de todas as suas formas conhecidas, esse é o modo mais indicado.

## Textual Search

A busca textual é uma busca por uma sequência de caracteres no corpo dos textos. Todas as ocorrências dessa sequência aparecem como resultado, independentemente do lugar onde elas ocorrem (início, meio ou fim de qualquer palavra).

### Exemplo  

Uma busca por **`λεγω`** retornará todas as palavras que contenham a sequência de caracteres `λ`, `ε`, `γ`, `ω`, como <mark>λέγω</mark>, προ<mark>λέγω</mark>ν, συλ<mark>λεγῶ</mark>σιν, δια<mark>λέγω</mark>μαι, φ<mark>λέγω</mark>ν, <mark>λεγώ</mark>μεθα, ἀ<mark>λέγω</mark>, oὐκα<mark>λέγω</mark>ν, ἀντι<mark>λέγω</mark>. 

### Textual Search x Lemma   

A *busca textual* retorna toda e qualquer palavra que contenha `λεγω`, ainda que faça parte de um verbo distinto, como `διαλέγω`. O que *busca textual* nunca faria é retornar uma forma como `ἐλέχθην` (aoristo passivo de λέγω), ainda que seja uma de suas formas conhecidas. 

A busca por *lemmata*, por sua vez, tem o comportamento oposto. Ela retorna toda e qualquer forma do verbo λέγω, incluindo ἐλέχθην, mas jamais outros verbos parecidos, como διαλέγω.


### Em resumo

- Modo mais lento que não utiliza o conhecimento da plataforma sobre a relação entre as diferentes formas declinadas dos termos. 
- Os resultados são rigorosamente determinados pelos caracteres utilizados na busca.
- Recomendado apenas em corpora previamente delimitados.


## Proximidade

### Simples

A busca por proximidade difere pela sua possibilidade de buscar por mais de um termo. É possível buscar pelos termos ocorrendo em conjunto com um intervalo de até **N** palavras entre eles.


#### Exemplo 

Uma busca possível apenas nesse modo é por dois termos, e.g. ἀκρασία e ψυχὴ, com um intervalo de até 10 palavras entre eles.


### Avançada

A **proximidade avançada** faz o mesmo, mas com a possibilidade de utilizar categorias gramaticais ao invés de termos específicos.


#### Exemplo

É possível buscar por todas ocorrências de *uma preposição* **+** *ψυχὴ*.
