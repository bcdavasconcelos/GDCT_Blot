tags: Automação, RegEx
permalink: /padrões úteis

# Padrões úteis de RegEx

## Palavras no alfabeto latino
 [Ver no RegEx 101](https://regex101.com/r/Lt2oEq/1).
 
* `\b[A-Za-z]+\b`  
    * `\b` *indica a posição no limite de uma palavra*  
    * `A-Z` *um caractere maiúsculo único no intervalo entre A e Z*  
    * `a-z` *um único caractere minúsculo no intervalo entre a e z*  
    * `+` *quantificador que corresponde a 1 ou mais, quantas vezes for possível*  
  
## Caracteres gregos  
[Ver no RegEx 101](https://regex101.com/r/4qEt6k/2)

* `\p{Greek}+` 
    * `\p`  Indica uma propriedade.  

## Numeração Bekker
[Ver no RegEx 101](https://regex101.com/r/6yLgjG/1)

* `\d{1,4}[a|b]\d{1,2}` 
    * `\d{1,4}` Corresponde ao intervalo entre 1 e 4 dígitos
    * `[a|b]` Corresponde a "a" ou "b".
    * `\d{1,2}` Corresponde ao intervalo entre 1 e 2 dígitos

## Numeração Stephanus
[Ver no RegEx 101](https://regex101.com/r/LMbkkI/1)

* `\d*[a|b|c|d|e]\d{1,2}`  


## Limpeza do texto do corpus aristotélico depois da conversão (betacode → unicode)
[Ver no RegEx 101](https://regex101.com/r/30DtfC/1)

* `\d*\s*[A-Za-z]{1,6}\.(\d{1,4}[a|b])\.(\d*)\s:\s(.+)\n`
* Substituição: `\1\2 \3 `

## Remoção da hifenização em texto da ed. Bekker do corpus aristotelicum
[Ver no RegEx 101](https://regex101.com/r/6yLgjG/3)

* `–\s*(\d*[a|b]\d*) (\p{Greek}+)`
* Substituição: `\2 \1`


***  
<br>
  
## Exemplo com posição e quantificador não-avarento
Na linha abaixo, eu preciso encontrar a referência Bekker.

> Metaph. A 1 980a21 Πάντες ἄνθρωποι τοῦ εἰδέναι ὀρέγονται φύσει. σημεῖον δ᾽ 980a22 ἡ τῶν αἰσθήσεων ἀγάπησις·  

1. `(^.*)` é uma expressão que encontraria, do começo da linha em diante, o maior número possível de qualquer caractere que aparece zero ou mais vezes.  
2. `(^.*?)` é uma expressão que encontraria, do começo da linha em diante, o menor número possível de qualquer caractere que aparece zero ou mais vezes.
3. `(\d+[a|b]\d\d)` é uma expressão que encontraria tanto `980a21` quanto `980a22`.  

### Resultados

`(^.*)(\d+[a|b]\d\d)` encontraria...  

> Metaph. A 1 980a21 Πάντες ἄνθρωποι τοῦ εἰδέναι ὀρέγονται φύσει. σημεῖον δ᾽ 980a22.`  

`(^.*?)(\d+[a|b]\d\d)` encontraria...  

> Metaph. A 1 980a21
