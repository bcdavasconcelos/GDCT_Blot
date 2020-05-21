tags: CSS, Modo Escuro, Diogenes
permalink: /dark-diogenes

# Dark Mode - Diogenes  
[Github Gist](https://gist.github.com/eb763f8d2704b262fbb1e1111b8ac2c9#file-diogenes-css)  
  
Praticamente todos os aplicativos hoje tem a opção de um modo escuro que emite menos luz e preserva a visão.  
  
O Diogenes infelizmente não tem.  
  
Melhor dizendo, não tinha…  
  
  
![Diogenes](/Imagens/Diog.png)  
  
  
  
## Para ativarmos o nosso modo escuro, primeiro precisamos encontrar e abrir o arquivo de estilo do programa  
  
No MacOS, abra o terminal e dê o seguinte comando:  
  
```  
open /Applications/Diogenes.app/Contents/server/diogenes.css  
```  
  
*Como não tenho o Windows instalado, não tenho como dar uma instrução precisa para encontrar e abrir o arquivo. Procure por* `*diogenes.css*` *em meio aos arquivos do programa. É ele que precisamos editar.*  
  
  
## Assim que abrir o arquivo…  
  
Por via das dúvidas, faça um backup criando uma cópia dele em outro lugar, ou copiando e colando o conteúdo em outro arquivo de texto.  
  
## Em seguida, apague o conteúdo do arquivo, então copie e cole o código abaixo  
  
Obs.: Você pode precisar reiniciar o sistema para que as mudanças tenham efeito.  

```
    html {
      height: 100%;
      margin: 0;
    }
    body {
      background-color:, 434140;
      color:, ffffff;
      font-family: 'Gentium Plus';
      font-synthesis: weight;
      height: 100%;
      margin: 0px;
    }
    body.waiting, body.waiting *{
        cursor: wait !important;
    }
    .wrapper {
        min-height: 100%;
        margin-right: 10px;
        margin-left: 10px;
        /* Equal to height of footer */
        /* But also accounting for potential margin-bottom of last child */
        margin-bottom: -50px;
    }
    .push {
      height: 50px;
    }
    .footer {
             font-size: 60%;
             text-align: center;
             color:, 434140;
             font: caption;
             -webkit-user-select: none;
             height: 50px;
             margin-block-start: 0px;
             margin-block-end: 0px;
    }
    
    /* Navbar */
    .navbar-area {
        text-align: center;
    }
    nav ul ul {
        display: none;
    }
    /*
    nav ul li:hover > ul {
        display: block;
    }
    */
    nav ul {
    
        background:, 434140; /* Old browsers */
        background: -moz-linear-gradient(top,, 434140 0%,, 545251 100%); /* FF3.6-15 */
        background: -webkit-linear-gradient(top,, 434140 0%,#545251 100%); /* Chrome10-25,Safari5.1-6 */
        background: linear-gradient(to bottom,, 434140 0%,#545251 100%); /* W3C, IE10, FF16, Chrome26, Opera12, Safari7 */
    
        box-shadow: 0px 0px 10px 3px rgba(0,0,0,0.10);
        padding: 0 20px;
        border-radius: 10px;
        list-style: none;
        position: relative;
        display: inline-table;
        font-size: 20px;
    }
    nav ul:after {
        content: ""; clear: both; display: block;
    }
    nav ul li {
            float: left;
    }
    nav ul li:hover {
        background:, 236d98;
        background: linear-gradient(top,, 236d98 0%,, 2c6484 40%);
        background: -moz-linear-gradient(top,, 236d98 0%,, 2c6484 40%);
        background: -webkit-linear-gradient(top,, 236d98 0%,, 2c6484 40%);
    }
    nav ul li:hover a {
        color:, 434140;
        text-decoration: none;
    }
    nav ul li a {
        display: block; padding: 10px 20px;
        color:, 236d98; text-decoration: none;
    }
    nav ul ul {
        background:, 236d98;
        background: linear-gradient(top,, 236d98 0%,, 2c6484 40%);
        background: -moz-linear-gradient(top,, 236d98 0%,, 2c6484 40%);
        background: -webkit-linear-gradient(top,, 236d98 0%,, 2c6484 40%);
    
        border-radius: 0px; padding: 0;
        position: absolute; top: 100%;
    }
    nav ul ul li {
        float: none;
        border-top: 1px solid, 236d98;
        position: relative;
    }
    nav ul ul li a {
        padding: 15px 30px;
        color:, ffffff;
    }
    nav ul ul li a:hover {
        background:, 236d98;
    }
    nav ul ul ul {
        position: absolute; left: 100%; top:0;
    }
    
    /* End navbar */
    
   , corpora-list1 {
        display: none;
    }
   , corpora-list2 {
        display: none;
    }
    
    .info-area {
        width: 450px;
        margin:auto;
    }
    .info-h2 {
        color:, 236d98;
    }
    .info-text {
        text-align: left;
    /*    font-size: 90%; */
        font-size: 20px;
    }
    .info-field {
        text-align: left;
        font-size: 100%;
    }
    .info-button {
        color:, 236d98;
        background:, 434140;
        box-shadow: 0px 0px 5px 2px rgba(0,0,0,0.10);
        font-size: 20px;
    }
    
    @font-face {
      font-family: 'Gentium Plus';
      src: url('/fonts/GentiumPlus-I.woff');
      font-weight: normal;
      font-style: italic;
    }
    @font-face {
      font-family: 'Gentium Plus';
      src: url('/fonts/GentiumPlus-R.woff');
      font-weight: normal;
      font-style: normal;
    }
    
    /* Use OS fonts for UI elements */
    .gotocontext, .homesearch {
      font: caption;
      -webkit-user-select: none;
    }
    
    .homewelcome {
        text-align: center;
        font-size: 20px;
    }
    
    .header_logo {
        text-align: center;
        padding-top: 15px;
    }
    .header_back {
        float:left;
        padding-top: 20px;
        background-color:, 434140;
        color:, 236d98;
    }
   , header_restore {
        float:right;
        padding-top: 0px;
        background-color:, 434140;
        color:, 236d98;
    }
    .restore_text {
        padding-right:6px;
    }
    .back_button {
        border-width: 0px;
        padding: 0px;
        margin: 0px;
        color:, 236d98;
        background-color:, 434140;
        text-align: center;
        align-items: center;
        vertical-align: middle;
    }
    .back_button_text {
        vertical-align: middle;
        color:, 236d98;
        display: inline;
        position: relative;
        top: -7px;
    }
    .dismiss_button_text {
        vertical-align: middle;
        color:, 236d98;
        display: inline;
        position: relative;
        top: -9px;
    }
    
    
    h1 {
        color:, 236d98;
    }
    h2 {
        color:, 236d98;
    }
    h3 {
        color:, 236d98;
    }
    
    
    /* Fix problem where sub/super-scripts increases the line spacing for
    text, but not for the citations, so they no longer align properly */
    
    sup { vertical-align: baseline; font-size: 90%; position: relative;
    top: -.4em; }
    
    sub { vertical-align: baseline; font-size: 90%; position: relative; top:
    .3em; }
    
    a:link {
      text-decoration:none;
    }
    a:visited {
      text-decoration: none;
    }
    a:active {
      text-decoration:none;
    }
    a:hover {
      text-decoration: underline;
    }
    
    a.perseus:link {
      color:, ffffff;
    }
    a.perseus:visited {
      color:, 404040;
    }
    
   , logo a:hover {
      text-decoration: none;
     }
    
    .text {
       text-indent: 8em;
    }
    
    .text-noindent {
       text-indent: 0in;
    }
    
    .citation {
      float: left;
      width: 8em;
      text-align: left;
      vertical-align: bottom;
    }
    
   , hit {
      background:, 514f4e;
     }
    
   , sidebar h1 {
             font-size: 150%;
    }
    
   , sidebar h2 {
             font-size: 120%;
    }
    
    .sidebar-split,
    .sidebar-full {
             display: block;
             top: 0px;
             right: 0px;
             overflow: auto;
             max-height: 99%; /* ensures scrollbar will appear */
    }
    .sidebar-split {
             width: 45%;
             background-color:, 434140;
             position: fixed;
             border-left: 1px solid grey;
             padding: 0em 1em;
    }
    .sidebar-full {
             width: 96%;
             background-color:, 434140;
             position: absolute;
             padding: 0em 2%;
    }
    .sidebar-hidden,
    .sidebar-newpage {
             display: none;
    }
    .dismiss-text {
        position: relative;
        top: -6px;
        display: inline;
        padding-right: 2px;
        padding-left: 10px;
    }
    .main-full {
             width: 100%;
    /*         padding-right: 4px; */
             display: block;
             height: 100%;
    }
    .main-hidden {
             display: none;
    }
    
   , sidebar-control {
             display: block;
             float: right;
             padding-left: 20px;
    }
    .back-padding {
        padding-top: 10px;
    }
    .invisible {
             display: none;
    }
    
    .visible {
             display: block;
    }
    
    .lemma_span_invisible {
             display: none;
    }
    
    .lemma_span_visible {
             display:block;
    }
    
    .form_span_invisible {
             display: none;
    }
    
    .form_span_visible {
             display: inline;
    }
    
    img.next {
             float: right;
    }
    img.prev {
             float: left;
    }
```    


