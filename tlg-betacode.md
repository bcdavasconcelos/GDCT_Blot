tags: Fontes primárias, TLG  
hashtags: #Fontes-primárias, #TLG  
permalink: /tlg-betacode

# Convertendo para unicode textos do TLG em betacode

Se você já teve a curiosidade de conferir os arquivos do banco de dados do TLG[^1], deve ter percebido que são apenas arquivos de texto plano numerados sequencialmente e com conteúdo praticamente ilegível.  

O número de quatro dígitos no nome de cada arquivo é, na verdade, o código do autor do texto (*cf.* [Códigos do TLG](tlg-ref)). Esse código aparece no Diogenes em alguns lugares diferentes, por exemplo, quando você faz uma busca simples pelo nome do autor em **Read>Author>Go.**  

![TLG 1](./img/tlg/__tlg2.png)  

![TLG3](./img/tlg/__tlg3.png)  

Já o formato de texto que você encontra dentro do arquivo — e que o Diogenes converte por nós em unicode — é o chamado *[betacode](https://en.wikipedia.org/wiki/Beta_Code)*. Esse formato foi criado especificamente para tornar possível grafar o grego politônico com caracteres ASCII no TLG e, infelizmente, tornou-se padrão em algumas domínios dos estudos clássicos.  

Para quem nunca abriu um arquivo do banco de dados do TLG, eis um exemplo retirado do arquivo contendo o Corpus Aristotelicum. Trata-se do início dos *Primeiros Analíticos* em *betacode*.  

> ÔÄ∞∞∏∂ˇÔÅ∞∞±ˇÔÇ¡–Úˇôò·èÙˇ@@@@{1$20*A*N*A*L*U*T*I*K*W*N *P*R*O*T*E*R*W*N *A.$}1 àä@*PRW=TON EI)PEI=N PERI\ TI/ KAI\ TI/NOS E)STI\N H( SKE/YIS, O(/TI PERI\ ÄA)PO/DEICIN KAI\ E)PISTH/MHS A)PODEIKTIKH=S: EI)=TA DIORI/SAI TI/ ÄE)STI PRO/TASIS KAI\ TI/ O(/ROS KAI\ TI/ SULLOGISMO/S, KAI\ POI=OS ÄTE/LEIOS KAI\ POI=OS A)TELH/S, META\ DE\ TAU=TA TI/ TO\ E)N O(/LW| EI)=-ÄNAI H)\ MH\ EI)=NAI TO/DE TW=|DE, KAI\ TI/ LE/GOMEN TO\ KATA\ PANTO\S ÄH)\ MHDENO\S KATHGOREI=SQAI. Ä  

Agora que já sabemos que os textos de cada autor estão no arquivo contendo o seu código correspondente e que o texto está em betacode, tudo que precisamos fazer é encontrar um meio de converter o arquivo em *unicode*.  

Há mais de um modo para realizar essa tarefa.  

## Método 1: Beta2Uni na UC Louvain  
Visitando o site da [Université catholique de Louvain](https://cental.uclouvain.be/beta2uni) temos duas opções.  
- Uma conversão básica, que apenas transforma o arquivo **.txt** do betacode para unicode, sem preservar qualquer dado adicional do texto.  
- Uma conversão estendida, que utiliza os arquivos **.txt** e **.idt** para produzir uma versão do texto com a numeração da edição crítica de referência (**Recomendado**).  

![TLG4](./img/tlg/__tlg4.png)  

![TLG5](./img/tlg/__tlg5.png)  

## Método 2: Diogenes  
No menu das versões mais recentes do [Diogenes](https://d.iogen.es), há uma opção “Export” que pode converter todo o banco de dados, ou parte dele, em arquivos XML[^2] contendo o texto unicode. Essa opção de conversão carrega várias informações adicionais no processo e produz um texto com diversas tags de marcação, que podem ser uma vantagem ou desvantagem dependendo do seu propósito. Utilizar esse método para removê-las manualmente em seguida definitivamente não é algo desejável.  

## Trabalhando com o arquivo gerado  
Independente do método utilizado, o processo provavelmente levará alguns minutos. O resultado da conversão será um arquivo de texto **muito** grande, por isso, a menos que você esteja usando um dos novos computadores quânticos, NÃO tente copiar e colar o texto no Microsoft Word. Use o **bloco de notas** ou um **[processador de texto](processadores-de-texto)** como o Visual Studio Code ou o Sublime Text (ambos funcionam no Windows e no Mac).  

A remoção da numeração das linhas gerada no processo de conversão (que nada tem a ver com a numeração utilizada para referenciar o texto), e outras transformações e marcações no texto, podem facilmente serem feitas utilizando ferramentas básicas de [expressões regulares (RegEx)](RegEx).  


[^1]: O nome da pasta provavelmente será **TLG-E (Greek Texts)**.  
[^2]: XML é o mesmo que um arquivo de texto plano, de modo que a extensão pode ser apagada e substituída por TXT sem prejuízo ao conteúdo do arquivo. A extensão XML apenas indica a alguns programas a presença de uma linguagem de marcação genérica no conteúdo.  
