tags: Automação, RegEx
hashtags: #Automação, #RegEx
permalink: /regex

# RegEx  

RegEx (expressões regulares) são sequências de caracteres que definem um padrão de pesquisa, comumente utilizados para operações de busca e busca e substituição.

<br>  

***

<br>  
  
## Coringas (a.k.a. wildcard)

Ao fazer uma busca, você pode substituir partes de uma palavra por caracteres coringas que correspondem a um ou mais caracteres (ou mesmo a um intervalo). 

- `?` Corresponde a uma letra ou um número.
- `.` Corresponde a qualquer caractere[^1].
- `\w` Corresponde a uma palavra (no alfabeto latino).
- `[abc…]` ou `[a|b|c|…]` Corresponde a qualquer um dos caracteres listados.
- `[^abc]` Corresponde a qualquer caractere que não está listado ou dentro do intervalo estipulado. 
- `\d` Corresponde a qualquer dígito entre 0-9.

### Intervalos

- `[a-z]` Corresponde ao intervalo entre “a” e “z”.  
- `[0-9,a-f]` Corresponde a qualquer dígito ou qualquer letra.

<br>  

***  

<br>  

## Quantificadores

Quantificadores afetam o caractere ou grupo anterior.

- `*` Corresponde a zero, um ou múltiplos caracteres.
- `+` Corresponde um ou múltiplos caracteres.
- `{1}` Corresponde a um caracter.
- `\d{1,4}` Corresponde a 1, 2, 3 ou 4 caracteres.

> O nada nadifica.  

- `nad.*` pode corresponder a `nada` ou `nadifica`.

### Quantificadores não-avarentos 

O comportamento padrão dos quantificadores é corresponder ao maior número de caracteres possível. Para ter o comportamento oposto, basta utilizar os quantificadores não avarentos, cuja especificidade é corresponder sempre ao menor número de caracteres.

- `+?` Corresponde a um ou mais.
- `*?` Corresponde a zero ou mais.

Tomando a paravra `Alfabeto` como exemplo:

- `Alf.+` corresponde a `Alfabeto`.
	* `.` corresponde a qualquer caractere.
	* `+` indica que estamos buscando um ou mais ocorrências.
- `Alf.+?` corresponde a `Alfa`.
	* Novamente, `.` corresponde a qualquer caractere.
	* `+?` indica que estamos buscando uma ou mais ocorrências, mas preferindo sempre o menor número.

<br>  

***  

<br>  

## Posição

Algumas expressões especiais podem ajudar a refinar a busca determinando a posição do caractere buscado.

- `^` Indica o início da linha.
- `$` Indica o fim da linha, logo antes da quebra de linha.
- `\b` Corresponde ao limite de uma palavra (no alfabeto latino).
- `x(?=abc)` nessa expressão `abc` tem acontecer depois de `x`
- `x(?!abc)` nessa expressão `abc` não pode acontecer depois de `x`
- `(?<=abc)x` nessa expressão `abc` tem que acontecer antes de `x`.
- `(?<!abc)x` nessa expressão `abc` não pode acontecer antes de `x`.

Um exemplo muito útil é `^.+`,  corresponde a todos os caracteres que ocorrem partindo do começo da linha.

<br>  

***  

<br>  

## Outras expressões especiais

- `\A` Indica o início do documento. 
- `\Z` Indica o final do documento.
- `\n` Uma quebra de linha
- `\t` Tabulação horizontal
- `\s` Um espaço em branco (dependendo do sistema de regex, pode corresponder ou não à quebra de linha; geralmente é o caso que sim.)
- `\h` Um espaço em branco (nunca corresponde à quebra de linha).

## Veja também

- [Padrões úteis de RegEx](padrões úteis)
- [Aprenda RegEx do jeito fácil](https://github.com/ziishaned/learn-regex/blob/master/translations/README-pt_BR.md)

## E ainda...

- [PDF Grep](https://pdfgrep.org/index.html)
- [Regex 101](https://regex101.com)
- [RegexOne](https://regexone.com)
- [RegExr](https://regexr.com)


[^1]: Em alguns casos é possível fazer com que `.` também corresponda a quebras de linha, mas esse geralmente não é o caso. No BBEdit, por exemplo, basta adicionar `(?s)` à expressão.  



