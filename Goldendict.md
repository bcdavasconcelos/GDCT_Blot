permalink: /goldendict
tags: Ferramentas filológicas, Dicionários, Apps
hashtags: #Ferramentas-filológicas, #Dicionários, #Apps

# Goldendict

O Goldendict é um software livre de código-aberto e que funciona em todos os sistemas operacionais para consultar dicionários e glossários em diversos formatos (e.g. dict, idx, dsl, lsd, bgl). Ele **não é** um dicionário, apenas oferece um ambiente para consulta-los e navegar por eles. A tarefa de encontrar, adquirir ou produzir o material é do usuário.

Para instalar o Goldendict, visite a página do projeto no [SourceForge](https://sourceforge.net/projects/goldendict/). Ao clicar em download, ele automaticamente direcionará para a versão apropriada para o seu sistema operacional. Caso isso não aconteça, selecione a aba `Files`, abra a pasta `early access builds` e escolha a versão apropriada. Ou seja, se você usa Windows, baixe o arquivo com a extensão `.exe`; se usa linux, baixe o arquivo `.7z` e, se usa mac, o arquivo `.dmg`.

A instalação é simples e varia conforme o sistema operacional.

Uma vez instalado, há duas tarefas importantes:

1. Configurar a tecla de atalho para acessar o programa.
2. Configurar os [dicionários](https://www.dropbox.com/sh/2x4agj4qflcvdge/AAAMrwPne_vgmT6sdSgLwijfa?dl=0) a serem utilizados.

Para configurar a tecla de atalho, abra as preferências/configurações do programa (Mac: `⌘,`| Win: `Arquivo>Configurações`) e selecione a aba `Hotkeys`. Você verá duas opções, uma para trazer o programa para o primeiro plano ou para esconde-lo (eu utilizo `⇧⌘D`), e outra para traduzir a palavra que estiver na área de transferência (utilizo `⇧⌘C`, de modo que eu posso selecionar uma palavra, copia-la utilizando `⌘C` e traduzi-la utilizando `⇧⌘C`). Selecione `OK` para salvar suas configurações.

Para configurar os dicionários, procure `Edit` > `Dictionaries` na barra de menu. A primeira tela que você verá será para configurar a pasta onde estão armazenados os dicionários. Selecione `Add`, escolha a pasta onde estão os arquivos e abra. Para que o programa sempre confira se há arquivos novos, marque o quadrinho da opção `Recursive` ao lado do nome da pasta. Pressione `Apply` para salvar as modificações.

Nesse momento, ele dará início a uma varredura da pasta para buscar os arquivos de dicionários. Dependendo do número de arquivos, isso pode levar um certo tempo. Depois dessa varredura inicial, já poderemos seguir para a aba `Groups` e configurar os nossos grupos de dicionários. Assim que for possível, faça isso. O Goldendict seguirá indexando o conteúdo dos dicionários por mais alguns minutos ou horas. 

Os grupos de dicionários são um bom modo de se organizar para facilitar as buscas. Você pode organizar os dicionários por línguas, por tarefas ou qualquer outro critério apropriado. Não há limite para o número de grupos e há uma opção de `Auto groups` que realiza essa tarefa por você utilizando as línguas dos dicionários como critério. 

Em minhas configurações pessoais, eu utilizo apenas um grupo com a seguinte ordem/estrutura:

1. Glossários feitos por mim 
2. Dicts morfológicos (grc)
3. Dicts etimológicos (grc e pt)
4. Dicts de Português (pt-pt)
5. Dicts de Grego moderno e antigo (grc-eng, grc-ell, grc-de, grc-fr, ell-eng, ell-de)
6. Dicts de Inglês (eng-eng, eng-pt, eng-de, eng-fr)
7. Dicts de Alemão (de-eng, de-de)
8. Dicts de Francês (fr-eng, fr-pt)
9. Dicts de Italiano (it-eng, eng-it, de-it, it-de)
10. Dicts de Latim (la-eng, la-de)
11. Wikitionary (diversos)



Na seção de dicionários, há uma aba chamada `Websites` para acrescentar páginas da internet. Se você quiser consultar o Linguee ou algum outro dicionário online, por exemplo, é preciso apenas conferir como o site estrutura o seu endereço. 

Para isso, basta fazer uma busca qualquer e observar no link onde a palavra buscada aparece. 

**EXEMPLO** 

Buscando por `car` eu vejo na minha barra de endereços:

```
https://www.linguee.pt/portugues-ingles/search?source=auto&query=car
````

O que precisamos fazer é apenas substituir `car` por `%GDWORD%`. 
De modo que o link adaptado para o Goldendict seria: 

```
https://www.linguee.pt/portugues-ingles/search?source=auto&query=%GDWORD%
```

Para fazer com que o Goldendict passe a buscar também nesse endereço,  selecione `Add` e procure pelo item vazio nas lista de sites. Acrescente o endereço adaptado, selecione o checkbox na coluna `enabled` e adicione esse 'dicionário' a algum dos seus grupos.

(*Continua*...)