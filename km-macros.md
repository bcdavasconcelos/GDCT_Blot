tags: Aristóteles, Automação, macOS  
hashags: #Aristóteles, #Automação, #macOS  
permalink: /km-macros

# Macro para citar Aristóteles  
  
  
Para o Keyboard Maestro não há propriamente uma galeria online de macros nos moldes do [Packal](http://www.packal.org)[^1]. Os principais recursos são o [fórum](https://forum.keyboardmaestro.com) e o [github](https://github.com), onde você encontra vários exemplos úteis para criar seus próprios macros. Recomendo buscar esses exemplos, pois é mais fácil adaptar um macro existente do que criar um novo a partir do zero. Atualmente, entre macros criados e adaptados, eu tenho cerca de 780 ativos e um total de 1516 (entre ativos e inativos). Esse é um software incrivelmente versátil e com diversas possibilidades de automatizar tarefas repetitivas.  
  
Um tipo de macro que eu acho particularmente útil e que uso com bastante frequência são macros para manipular texto. Via de regra, mantenho os textos gregos em formato de texto plano (.txt/.md) e com toda a numeração de referência da edição crítica em cada linha. Isso é muito útil para referenciar com precisão, mas não é um bom formato para citar no corpo do texto de um trabalho acadêmico. Veja um exemplo do *De Anima:*  
  
> 431a08 τὸ μὲν οὖν αἰσθάνεσθαι ὅμοιον τῷ φάναι μόνον καὶ νοεῖν·  
> 431a09 ὅταν δὲ ἡδὺ ἢ λυπηρόν, οἷον καταφᾶσα ἢ ἀποφᾶσα διώκει  
> 431a10 ἢ φεύγει· καὶ ἔστι τὸ ἥδεσθαι καὶ λυπεῖσθαι τὸ ἐνεργεῖν  
> 431a11 τῇ αἰσθητικῇ μεσότητι πρὸς τὸ ἀγαθὸν ἢ κακόν, ᾗ τοιαῦτα.  
> 431a12 καὶ ἡ φυγὴ δὲ καὶ ἡ ὄρεξις ταὐτό, ἡ κατ ἐνέργειαν, καὶ  
> 431a13 οὐχ ἕτερον τὸ ὀρεκτικὸν καὶ τὸ φευκτικόν, οὔτ ἀλλήλων οὔτε  
> 431a14 τοῦ αἰσθητικοῦ· ἀλλὰ τὸ εἶναι ἄλλο.  
  
Para citar no corpo do texto, criei [um macro](https://github.com/bcdavasconcelos/mykmmlibrary/tree/master/Text%20Manipulation#normalize-greek-text) que remove a numeração do texto grego, elimina as quebras de linha e a hifenização e adiciona a numeração Bekker formatada depois da citação. Para fazer isso, eu apenas seleciono o texto e ativo o macro. Com apenas um clique o trecho acima está pronto para ser citado:  
  
> τὸ μὲν οὖν αἰσθάνεσθαι ὅμοιον τῷ φάναι μόνον καὶ νοεῖν· ὅταν δὲ ἡδὺ ἢ λυπηρόν, οἷον καταφᾶσα ἢ ἀποφᾶσα διώκει ἢ φεύγει· καὶ ἔστι τὸ ἥδεσθαι καὶ λυπεῖσθαι τὸ ἐνεργεῖν τῇ αἰσθητικῇ μεσότητι πρὸς τὸ ἀγαθὸν ἢ κακόν, ᾗ τοιαῦτα. καὶ ἡ φυγὴ δὲ καὶ ἡ ὄρεξις ταὐτό, ἡ κατ ἐνέργειαν, καὶ οὐχ ἕτερον τὸ ὀρεκτικὸν καὶ τὸ φευκτικόν, οὔτ ἀλλήλων οὔτε τοῦ αἰσθητικοῦ· ἀλλὰ τὸ εἶναι ἄλλο. (431a08 - 431a14)  
  
Pode parece algo bobo, mas quando você precisa citar 100, 200 trechos, isso representa uma economia de cerca de 4-8 mil teclas pressionadas.  
  
Meus dedos agradecem.  
  
[^1]: Packal é um repositório online de workflows para o Alfred, outro excelente software para o MacOS.  
  
