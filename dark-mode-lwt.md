tags: CSS, Modo Escuro  
hashtags: #CSS, #Modo-Escuro  
permalink: /dark-mode-lwt

# Modo escuro para o Learning with Texts  
<script src="prism.js"></script>

[Github Gist](https://gist.github.com/f16551a2c479cb7d43bdfc2fdd568d34#file-styles-css)  

[Learning with texts](http://lwt.sourceforge.net) é um excelente programa para praticar línguas estrangeiras.  
Esse é um CSS com um modo escuro para o programa.

```language-css
    body {
        background-color:, 434140;
        color:, FFFFFF;
        font: 100%/1.25 'EB Garamond', serif;
        margin: 20px;
        padding: 0px;
    }
    input[type=text] {
        font: 85% 'EB Garamond', serif;
        border: 1px solid, 434140;
        padding: 3px;
    }
    p {
        margin: 5px 0 5px 0;
        padding: 0;
    }
    h3 {
        margin: 0px 0 0px 0;
        padding: 0;
    }
    h4 {
        margin: 5px 0 10px 0;
        padding: 0;
    }
    span.status0 {
        background-color: rgb(254, 100, 61);
        color:, FFFFFF;
    }
    span.status1 {
        background-color: rgb(253, 127, 95);
        color:, FFFFFF;
    }
    span.status2 {
        background-color: rgb(253, 175, 108);
        color:, FFFFFF;
    }
    span.status3 {
        background-color: rgb(255, 199, 70);
        color:, FFFFFF;
    }
    span.status4 {
        background-color: rgb(205, 188, 0);
        color:, FFFFFF;
    }
    span.status5 {
        background-color: rgb(11, 159, 1);
        color:, FFFFFF;
    }
    span.status99 {
        background-color:, 434140;
        border-bottom: solid 2px, 434140;  
        color:, FFFFFF;
    }
    span.status98 {
        background-color:, 434140;
        border-bottom: dashed 1px, 434140;
        color:, FFFFFF;
    }
    span.mwsty {
        margin-right: 2px;
        font-size: 60%;
        font-weight: bold;
        color:, FFFFFF;
        vertical-align: top;
    }
    span.wsty {
        margin-right: 2px;
        color:, FFFFFF;
    }
    span.todosty {
        background-color: rgb(251, 214, 111);
    }
    span.doneoksty {
        background-color: rgb(129, 255, 129);
    }
    span.donewrongsty {
        background-color: rgb(253, 166, 145);
    }
    span.status5stat {
        background-color: rgb(131, 255, 131);
        color:, FFFFFF;
    }
    textarea {
        font: 85% 'EB Garamond', serif;
        <link href="https://fonts.googleapis.com/css?family=EBGaramond&display=swap" rel="stylesheet">
        border: 1px solid, 434140;
        padding: 3px;
    }
    table.tab1 {
        background-color:, 434140;
        margin-bottom: 10px;
        margin-top: 10px;
        border-top: 1px solid, 545454;
        border-left: 1px solid, 545454;
        width: 850px;
    }
    table.tab2 {
        background-color:, 434140;
        margin-bottom: 10px;
        margin-top: 10px;
        border-top: 1px solid, 545454;
        border-left: 1px solid, 545454;
        width: 100%;
    }
    table.tab3 {
        background-color:, 434140;
        margin-bottom: 10px;
        margin-top: 10px;
        border-top: 1px solid, 545454;
        border-left: 1px solid, 545454;
        width: auto;
    }
    td.td1 {
        border-bottom: 1px solid, 545454;
        border-right: 1px solid, 545454;
        vertical-align: top;
    }
    td.td1bot {
        border-bottom: 1px solid, 545454;
        border-right: 1px solid, 545454;
        vertical-align: bottom;
    }
    th.th1 {
        border-bottom: 1px solid, 545454;
        border-right: 1px solid, 545454;
        background-color:, 434140;
        vertical-align: top;
    }
    th.clickable {
        cursor: pointer;
    }
    .click {
        cursor: pointer;
        color: rgb(229, 4, 4);
    }
    .clickedit {
        cursor: pointer;
    }
    .hide {
        display: none;
    }
    a {
        text-decoration: none;
    }
    a:link {
        color: rgb(229, 4, 4);
    }
    a:visited {
        color: rgb(229, 4, 4);
    }
    a:active {
        color: rgb(229, 4, 4);
    }
    a:focus {
        color: rgb(229, 4, 4);
    }
    a:hover {
        color: rgb(229, 4, 4);
    }
    img {
        border: 0pt none;
    }
    .red {
        color:, FF0000;
        font-weight: bold;
        background-color:, 434140;
        text-align: center;
        font-size: 120%;
    }
    .msgblue {
        color:, 0000FF;
        font-weight: bold;
        background-color:, 434140;
        text-align: center;
        font-size: 120%;
    }
    .red2 {
        color:, FF0000;
        font-weight: bold;
    }
    .red3 {
        color:, FF0000;
    }
    .scorered {
        font-weight: bold;
        color:, FF0000;
    }
    .scoregreen {
        color:, 006400;
    }
    .left {
        text-align: left;
    }
    .right {
        text-align: right;
    }
    .center {
        text-align: center;
    }
    .bigger {
        font-size: 130%;
    }
    .smaller {
        font-size: 80%;
    }
    .backgray {
        background-color:, 434140;
    }
    .backlightyellow {
        background-color:, FFFACD;
    }
    .small {
        color: black;
        font-size:60%;
    }
    .smallgray {
        color: gray;
        font-size:60%;
    }
    .smallgray2 {
        color: gray;
        font-size:80%;
    }
    .smallgray3 {
        color: gray;
        font-size:70%;
        width: 850px;
        margin-bottom: 20px;
    }
   , learnstatus {
        color:, FFFFFF;
        font-size: 120%;
        font-weight: bold;
    }
   , iknowall {
        background-color:, 434140;
        cursor: pointer;
        color: rgb(229, 4, 4);
        padding: 5px;
        border: 1px solid, FFFFFF;
         text-align: center;
    }
    img.lwtlogo {
        margin-right: 15px;
        float: left;
    }
    img.lwtlogoright {
        margin-left: 30px;
        float: right;
    }
    .inline {
        display: inline;
    }
    .grayborder {
        border: 1pt solid, 545454;
    }
    .graydotted {
        margin-top: 30px;
        padding-top: 5px;
        border-top: 1px dotted, 545454;
    }
   , printoptions {
        margin-bottom: 15px;
        padding-bottom: 15px;
        border-bottom: 1px dotted, 545454;
        line-height: 1.8;
        margin-top: 20px;
    }
    .width50px {
        width: 50px;
    }
    .width99pc {
        width: 99%;
    }
    .width45pc {
        width: 45%;
    }
    dd {
        margin-top: 10pt;
    }
    dt {
        margin-top: 10pt;
    }
    .annterm {
        font-weight: bold;
        border-bottom: 2px solid, CCCCCC;
    }
    .anntermruby {
        font-weight: normal;
        border-bottom: 2px solid, 434140;
    }
    .annrom {
        color:, 999999;
        font-size: 60%;
        font-style: italic;
    }
    .annromruby {
        color:, FFFFFF;
        font-size: 100%;
        font-style: italic;
    }
    .annromrubysolo {
        color:, FFFFFF;
        font-size: 100%;
        font-style: normal;
    }
    .anntrans {
        color:, 0099CC;
        font-size: 60%;
        font-style: normal;
    }
    .anntransruby {
        color:, 0099CC;
        font-size: 100%;
        font-style: normal;
    }
    .anntransruby2 {
        color:, 006699;
        font-size: 125%;
        font-style: normal;
    }
   , footer {
        bottom: 0;
        position: absolute;
        width: 100%;
        height: 45px;
        line-height:30px;
        background:, 434140;
        font-size: 14px;
        text-align: center;
        border-top: 1px solid, FFFFFF;
    }
    .borderl {
        border-left: 1px solid, FFFFFF;
        border-top: 1px solid, FFFFFF;
        border-bottom: 1px solid, FFFFFF;
    }
    .borderr {
        border-top: 1px solid, FFFFFF;
        border-bottom: 1px solid, FFFFFF;
        border-right: 1px solid, FFFFFF;
    }
    .uwordmarked {
        font-weight: bold;
        border-top: 3px solid red;
        border-bottom: 3px solid red;
        border-right: 3px solid red;
        border-left: 3px solid red;
    }
    .kwordmarked {
        font-weight: bold;
        border-top: 3px solid black;
        border-bottom: 3px solid black;
        border-left: 3px solid black;
        border-right: 3px solid black;
    }
   , termtags {
        width: 340px;
        margin-top: 0px;
        margin-bottom: 0px;
        margin-left: 2px;
    }
   , texttags {
        width: 340px;
        margin-top: 0px;
        margin-bottom: 0px;
        margin-left: 2px;
    }
    .editable_textarea {
        display: inline;
    }
    .nowrap {
        white-space: nowrap;
        margin-left: 20pt;
    }
    .borderleft {
        border-left: 1px solid black;
        border-top: 1px solid black;
        border-bottom: 1px solid black;
        background-color:, EEEEEE;
    }
    .bordermiddle {
        border-top: 1px solid black;
        border-bottom: 1px solid black;
        background-color:, EEEEEE;
    }
    .borderright {
        border-right: 1px solid black;
        border-top: 1px solid black;
        border-bottom: 1px solid black;
        background-color:, EEEEEE;
    }
    .wizard {
        margin: 20px 0 5px 0;
    }
    /**************************************************************
    Additional styles for printing
    ***************************************************************/
    @media print
    {
        .noprint {
            display: none;
        }
       , print {
            font-size: 75%;
        }
    }
```
