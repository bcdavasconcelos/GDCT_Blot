tags: Automação, Markdown, Pandoc, Python
hashtags: #Automação, #Markdown, #Pandoc, #Python
permalink: /mdfootnotes

# Convertendo o formato das notas de rodapé em arquivos markdown

Eventualmente, pode ser útil ou necessário mudar o estilo das notas de rodapé em markdown. O método comumente adotado envolve utilizar uma marcação para indicar a origem da nota (e.g. `[^1]`) e deixar o seu conteúdo propriamente no final do texto (mais ou menos como seria em processadores de texto como o Word).

```
# Título

Parágrafo A[^1]

Parágrafo B[^2]

Parágrafo C[^3]

[^1]: Primeira nota de rodapé.
[^2]: Segunda nota de rodapé.
[^3]: Terceira nota de rodapé.
```

## Problema

Via de regra, isso funciona muito bem. O problema surge quando queremos dividir esse arquivo de algum modo. Se eu o dividisse em parágrafos, por exemplo, possivelmente usando algum script para agilizar o processo[^1], isso separaria a marcação da nota do seu conteúdo. (O script não sabe que o conteúdo da nota está no fim do texto.) 

Esse seria o resultado:

```
# Título

Parágrafo A[^1]
```

```
Parágrafo B[^2]
```

```
Parágrafo C[^3]

[^1]: Primeira nota de rodapé.
[^2]: Segunda nota de rodapé.
[^3]: Terceira nota de rodapé.
```

## Solução

A solução mais simples para essa dificuldade seria converter todas as notas para o formato *inline*.

```
# Título

Parágrafo A[^Primeira nota de rodapé.]

Parágrafo B[^Segunda nota de rodapé.]

Parágrafo C[^Terceira nota de rodapé.]
```

Isso pode ser feito utilizando o script abaixo. Para utiliza-lo, você precisará ter instalado o [Python 3](https://www.python.org/downloads/).

Salve o código como um arquivo de texto com a extensão `py` (e.g. `inliner.py`)[^2]. Abra o shell/terminal e navegue até a pasta do script. Dê o seguinte comando:

```bash
python inliner.py [input.markdown] [output.markdown]
```

Faça isso substituindo [input.markdown] pelo caminho até o arquivo que deve ser modificado e [output.markdown] pelo caminho e pelo nome do novo arquivo que deve ser gerado. 

### E.g.:

```bash
python inliner.py "~/Dropbox/Markdown/Arquivo1.md" "~/Dropbox/Markdown/Arquivo1Modificado.md"
```

## Script

```
#!/usr/bin/env python
# inliner - converts reference-style Markdown endnotes to
# Pandoc Markdown's inline footnotes
# by Louis Goddard <louisgoddard@gmail.com>
# Usage: python inliner.py [input.markdown] [output.markdown]

import sys

with open(sys.argv[1], "r") as input:
    text = input.read()

counter = 0

while True:
    try:

        counter = counter + 1

        ref = "[^" + str(counter) + "]:"
        nextRef = "[^" + str(counter + 1) + "]:"
        cite = "[^" + str(counter) + "]"

        refStart = text.index(ref)
        refEnd = text.index(nextRef) - 2
   
        offset = len(str(counter)) + 5

        note = "[^" + text[refStart+offset:refEnd] + "]"
        text = text.replace(cite, note)

    except ValueError:


        break

if counter > 1:

    note = "[^" + text[refStart+offset:len(text)-1] + "]"
    text = text.replace(cite, note)
    text = text.replace("\n    ", " ")
    cutPoint = text.index("\n[")
    text = text[0:cutPoint]
    print(str(counter) + " notes replaced.")

else:

    print("0 notes replaced.")

with open(sys.argv[2], "w") as output:
    output.write(text)
```

[^1]: Utilizando a linha vazia entre os parágrafos como delimitador.  
[^2]: Você pode simplesmente salvar o arquivo como `.txt` e depois mudar para `.py` manualmente.