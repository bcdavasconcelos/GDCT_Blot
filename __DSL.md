Montando seu próprio glossário

O formato de dicionários/glossários mais simples é sem dúvida o DSL. Trata-se de um texto plano em formato de lista. 

**EXEMPLO**

```
Entrada 1
	Primeira definição.
	Segunda definição
Entrada 2
	Perceba que a definição começa com um espaço ou tab no início da linha.
	Qualquer item que estiver no começo da linha será uma entrada no dicionário.
Entrada 3
Nome alternativo da entrada número 3
Outro nome alternativo da entrada número 3
	Definição 3.
	Segundo definição de 3.
```

Alguma formatação é possível utilizando tags parecidas com HTML.

```
[b]Palavra[/b] para negrito
[i]Palavra[/i] para itálico
[m0]Para estipular a que distância da margem a definição de aparecer.[/m]
[m1]São 8 níveis possíveis (m0, m1, m2 m3...) [/m]
[url]www.google.com[/url] para acrescentar um URL
<<Entrada 1>> para criar um link direto para outra entrada
[!trd]Seção não indexada pelo programa[/!trd] para efeitos da realização de busca direto no corpo dos dicionários.
```