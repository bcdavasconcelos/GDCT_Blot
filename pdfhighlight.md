tags: Automação, Python, PDFs
hashtags: #Automação, #Python, #PDFs
permalink: /pdf-highlight


# Script para realce de palavras em arquivo PDF

Para esse script, você vai precisar do [Python 3](https://www.python.org/downloads/) instalado e da biblioteca [PyMuPdf](https://pypi.org/project/PyMuPDF/). Se você já tiver o python3 instalado, basta dar o seguinte comando no terminal/shell:


```bash
pip install PyMuPdf
```

Para usar o script, salve o código abaixo em um arquivo de texto com o nome `pdfhigh.py` e a lista de palavras que devem ser realçadas no PDF em um arquivo chamado `Lista.txt` na mesma pasta. Você pode corrigir o endereço para o arquivo pdf no script, ou colocar o arquivo na mesma pasta com o nome `File.pdf`. 

Para rodar o script, abra o shell/terminal e navegue até a pasta com os arquivos. Dê o seguinte comando:

```bash
python3 pdfhigh.py
```

## Script

```python
# Fonte: https://github.com/isitan/PDF-dictionary-highlighter

import fitz
import re

# splits the words from special characters and checks if those subwords are in the dictionary.
def wordListProcessor(wordList, page):
    word = wordList[4]
    split_word = re.split(r'[`\-=~!@#$%^&*()_+\[\]{};\'\\:"|<,./<>?]', word)
    for subword in split_word:
        stripped = subword.strip()
        if(stripped in lookup_set or stripped[:-1] in lookup_set or stripped[:-2] in lookup_set):
            highlight = page.addHighlightAnnot(fitz.Rect(wordList[0], wordList[1], wordList[2], wordList[3]))

lookup_set = set()
# reads dictionary into set to accelarate the process
def setMaker(file_name):
    _file = open(file_name, "r")
    for entry in _file:
        lookup_set.add(entry[:-1].strip())

# Lista de palavras pode ficar na mesma pasta desse script com em um arquivo com o nome Lista.txt
dictionary_file_names = ["./Lista.txt"]

for dictionary_file in dictionary_file_names:
    setMaker(dictionary_file)

### Ler pdf
doc = fitz.open("./File.pdf")

for page in doc:
    page_text = page.getText("words",flags=None)
    for wordList in page_text:
        #wordList is a list which first 4 elements are location and the 5th is the word itself
        wordListProcessor(wordList, page)

### OUTPUT
doc.save("./File.pdf", garbage=4, deflate=True, clean=True)
```

