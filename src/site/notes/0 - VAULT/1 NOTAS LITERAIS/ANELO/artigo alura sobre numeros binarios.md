---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/artigo-alura-sobre-numeros-binarios/","tags":["python","teoria","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# artigo alura sobre numeros binarios

## criado em: 
-  06-05-2023 - 19:24

### Conteúdo Relacionado
- notas: 
- tags: #python #teoria #ANELO
- Fontes & Links: https://www.alura.com.br/artigos/sistema-codigo-binario

---

# Entenda o sistema de Código Binário

Alura

>O artigo aborda o sistema binário, fundamental para a compreensão da forma como os computadores processam informações. O autor explica que, embora os seres humanos usem o sistema decimal, as máquinas usam o binário, que tem apenas dois algarismos: 0 e 1. Ele fornece uma explicação visual para ajudar o leitor a entender como o sistema binário funciona e como é possível converter números entre decimal e binário. O autor também enfatiza a importância do sistema binário para a programação e para a compreensão da arquitetura do computador.

---

## Introdução

Logo que comecei a estudar programação, algumas das minhas principais dúvidas eram: “como a máquina consegue entender as instruções de uma linguagem?” Ou então, ficava imaginando, “como os circuitos, processador, memória conseguem transformar algumas linhas de código em um programa ou aplicativo de celular”. E você, também já se perguntou sobre isso?

Para entender um pouco melhor, pesquisei sobre o assunto e já nas primeiras aulas da faculdade me deparei com o estudo sobre o chamado **sistema binário**. Aí você deve pensar: “Ah, então foi aí que as coisas começaram a fazer mais sentido”. A resposta é **“NÃO!”**

![Imagem de um gato branco, com manchas pretas com olhos marejados, dando a ideia de tristeza.](https://www.alura.com.br/artigos/assets/sistema-codigo-binario/imagem1.png)

Oi, como assim? Pois é, eu explico… não fez sentido, porque na verdade tudo ficou muito confuso e minha cabeça quase explode tentando calcular conversão de número binário no papel. Diante dessa situação, fiz o que qualquer pessoa faria: pesquisei no google e estudei pela Alura xD.

**Vem comigo pra entender DE VEZ o que são números binários. Vamos lá!**

## Eu vejo Números... todo o tempo

Sabemos que os números fazem parte do nosso dia a dia e a gente lida com eles no momento em que acorda até o sono chegar. O preço do feijão com arroz , os cálculos para a feira do mês caber no orçamento, ou mesmo a quantidade de horas que você fica em frente ao seu computador naquela partida _online_.

Com os números é possível representar muita coisa e também transformar essas representações numéricas em informações - ou até mesmo constituir uma forma de comunicação (pode ser um número de telefone, endereço, conta de banco, dentre outros exemplos).

Pensa comigo: “se nós, seres humanos, utilizamos os números para diversas abstrações do mundo real, por que com as máquinas seria diferente?”

![O vídeo em loop mostra um homem negro, sorrindo e apontando para a sua cabeça, em diração a fonte. A intenção é sugerir que está “usando a cabeça”.](https://www.alura.com.br/artigos/assets/sistema-codigo-binario/imagem2.gif)

Fonte: [tenor.com](https://tenor.com/view/feel-me-think-about-it-meme-gif-7715402)

Faz sentido então construir máquinas ou soluções de acordo com nossa compreensão da realidade, ou seja, que tenha alguma conexão com a nossa forma de organização do mundo real, e por isso utilizamos também _números_ para dar instruções aos computadores.

Ok, agora entendi que nos comunicamos com as máquinas através de números. **Mas... as máquinas calculam números da mesma forma que a gente aprendeu na escola?**

Agora você deve ter percebido um detalhe muito importante. Nós utilizamos 10 algarismos, os números 0 ,1,2,3,4,5,6,7,8,9 para criar, quantificar ou mesmo organizar qualquer coisa. É o chamado **sistema decimal, são números que possuem base 10 e sua classificação está relacionada a posição que ocupa**.

Agora parece que complicou? Vamos ver de outra forma.

Vejamos o número 12 em decimal:

![Imagem em fundo branco demonstrando que o número 12  é igual a soma dos fatores de 1x10¹ e 2x10º.](https://www.alura.com.br/artigos/assets/sistema-codigo-binario/imagem3.png)

Para formar o decimal 12, é preciso multiplicar os algarismos por 10 elevados a sua posição (o 2 está na posição 0 e o 1 está na posição 1). Depois disso nós fazemos a soma dos fatores e confirmamos o seu valor decimal!

![O vídeo em loop mostra um homem caucasiano, por volta dos 40 anos, olhando para um ponto fixo como se estivesse concentrado, em volta dele há várias equações matemáticas e números flutuando, o que sugere que ele está calculando algo. Depois disso a câmera fecha nos olhos dele.](https://www.alura.com.br/artigos/assets/sistema-codigo-binario/imagem4.gif)

Fonte: [giphy.com](https://giphy.com/gifs/maths-DHqth0hVQoIzS)

Quando olhamos apenas para os números, às vezes o cálculo não parece fazer muito sentido, vamos olhar de outra forma então:

![Imagem organizada em organograma cascata mostrando que o expoente da base 10 é equivalente a posição em que o número 12 se encontra. Nesse caso, contamos da esquerda para a direita e a partir do algarismo 0, e para 12, o número 2 está na posição 0 e o número 1 está na posição 1.](https://www.alura.com.br/artigos/assets/sistema-codigo-binario/imagem5.jpg)

Acho que agora conseguimos visualizar melhor. certo?

Para os computadores a formação do padrão numérico é muito semelhante. Todavia, as máquinas compreendem os números em um **sistema binário**.

**O sistema binário funciona da mesma maneira que o decimal. Porém, o decimal tem 10 algarismos como base, e o binário tem apenas dois algarismos.** A regra de formação é a mesma, cada dígito é o seu valor multiplicado por 2, elevado ao valor da sua posição no número total menos um. Depois de calcular o valor de cada dígito, basta somá-los para ter o valor final em decimal. Vamos ver na prática?

Já temos o número 12 em decimal, mas há uma representação dele em binário, e conseguimos ter essa informação por meio da conversão de valores decimais para o código binário. Veja o esquema abaixo para entender como funciona:

![Imagem organizada em organograma cascata mostrando a conversão do decimal 12 em binário. Dividimos 12 por 2 até permanecer no número indivisível, o resto de todas as divisões é o número binário lido da esquerda para a direita. 12/2 = 6 , 6/2 = 3, 3/2 = 1 ; o resto da divisão é 0011, depois basta posicioná-los em 1100 que teremos o binário de 12.](https://www.alura.com.br/artigos/assets/sistema-codigo-binario/imagem6.jpg)

Então temos inicialmente o decimal 12 dividido por 2, e seu resultado é 6. Correto? **”Tá certo, mas e esse 0 aí embaixo?”**. O número 0 é o resto da divisão, é o que sobra. Dessa forma, precisamos dividir todo o número até não existir mais unidade divisível. O resto da divisão é o que corresponde ao número binário, nós apenas precisamos inverter a ordem e 12 em binário é igual a **1100**

![O vídeo em loop mostra o personagem Elliot , da série Mr.Robot, comemorando com um grito “whoo!”.](https://www.alura.com.br/artigos/assets/sistema-codigo-binario/imagem7.gif)

Fonte: [gfycat.com](https://gfycat.com/backpitifulcrow-mr-robot-series-show)

## E por que as máquinas utilizam o binário e não o decimal?

Para a gente entender melhor esse ponto, precisamos voltar nosso olhar um pouco para a história da computação. Nos computadores de uso geral, que são os mais próximos dos computadores atuais (podemos dizer que são como o tataravô do seu notebook ou celular), a programação era realizada com a conexão direta entre unidades físicas que enviavam os sinais elétricos, eram **válvulas** que você precisava trabalhar manualmente para poder enviar as instruções, você ligava e desligava para enviar as informações!

O ENIAC (Electronic Numerical Integrator and Computer ou, em português, computador integrador numérico eletrônico) é um desses exemplos de computadores de uso geral que precisavam ser ligados e desligados manualmente para ser programado.

No entanto, o ENIAC era uma **máquina decimal** e funcionava com uma memória de 20 “acumuladores” que mantinham um número decimal de 10 dígitos em cada unidade. Havia um anel de 10 válvulas que representava cada dígito e quando uma válvula estava no estado LIGADO, representava um desses 10 dígitos. Assim os cálculos eram feitos, em meio a conexão ou desconexão de cabos e um emaranhado de ligações entre chaves.

![O vídeo em loop mostra três mulheres programando manualmente o ENIAC por volta dos anos 40, ligando cabos e acionando chaves, em seguida adentra um homem na sala”.](https://www.alura.com.br/artigos/assets/sistema-codigo-binario/imagem8.gif)

Fonte: [ufrgs.br](https://www.ufrgs.br/enigma/as-mulheres-do-eniac/)

A gente consegue perceber que programar não era tão fácil, demandava esforço físico além de mental ! Já pensou: você? Programador bodybuilder?

![O gif mostra um homem musculoso e praticando o exercício supino com uma mesa e um computador em cima”.](https://www.alura.com.br/artigos/assets/sistema-codigo-binario/imagem9.gif)

Fonte: [Bodybuilding by Guilherme Mota on Dribbble](https://dribbble.com/shots/9518062-Bodybuilding)

Por conta dessas características, era difícil trabalhar e encontrar mão-de-obra para operar computadores como o ENIAC. Pensando nisso. Um dos consultores no projeto ENIAC foi o matemático Von Neumann, imaginou uma forma de facilitar o processo de programação com a proposta de um novo computador de programa armazenado em meados de 1940. O EDVAC (Electronic Discrete Variable Automatic Computer, em tradução livre, calculadora eletrônica automática de variável discreta) e posteriormente o IAS (a sigla vem do nome do instituto de Princeton, Institute for Advanced Study - Instituto de estudos avançados) combinavam uma arquitetura que otimizava também o processamento de dados.

E qual a relação disso com o código binário? Como as informações do sistema binário são transferidas para a máquina, ou melhor, **como os computadores conseguem entender o sistema binário?**

![A imagem mostra as fotos de Alan Turing, Von Neumann, George Boole e Leibniz.](https://www.alura.com.br/artigos/assets/sistema-codigo-binario/imagem10.png)

Matemáticos como Von Neumann e [**Alan Turing**](https://www.alura.com.br/artigos/decifrando-alan-turing-vida-trajetoria-tecnologia) se apropriaram de conceitos de Leibniz (sistema binário de numeração), George Boole (álgebra booleana) e aplicaram em seus estudos sobre arquitetura de computadores e criptografia, trabalhos que são a base da computação atual. Dessa forma, perceba que o sistema binário não foi inventado para os computadores ou é algo exclusivo à computação, mas sua aplicação no contexto dos computadores, a conversão de binário para decimal realizada pelas máquinas, e a codificação é uma combinação entre arquitetura computacional e lógica matemática.

Nesse sentido, é muito importante entender que as instruções precisam ser processadas por uma máquina que é constituída por circuitos e componentes eletrônicos (bem diferente dos seres humanos, que podem receber estímulos diferentes e processam informações de forma complexa), e mesmo com a segunda geração de computadores e os transistores (adeus, válvulas!) isso gera algumas “limitações” pois as máquinas identificam dois estados de acordo com os sinais elétricos, que são o desligado e ligado, o nosso 0 e 1, ou simplesmente o **sistema binário** (ta-da!).

![Personagem da série The office, Michael Scott, com uma roupa de mágico. No vídeo em repetição,  Michael faz uma mágica e sai um pouco de fogo de sua mão, depois disso aparecem os números 01 e, após o Michael abrir as mãos com um olhar de surpresa, aparecem as palavras “Ta-da” no canto inferior da tela.](https://www.alura.com.br/artigos/assets/sistema-codigo-binario/imagem11.gif)

Fonte: [tenor.com](https://tenor.com/view/steve-carrell-magic-tada-magician-trick-gif-15099383)

Então as máquinas funcionam apenas com sistema binário , é só 01, ligado ou desligado? A resposta é “sim” e “não”, vamos focar agora no **código binário**...

Como vimos, o decimal possui 10 símbolos para representar infinitos números, os números binários possuem base 2, ou seja, dois algarismos que também fazem combinações infinitas e podem representar um sem fim de coisas apenas com o 0 e 1. Cada letra deste artigo, todos os pixels dos gifs e imagens estáticas que escolhi, arquivos de texto lidos, vídeos, áudio, tudo é construído com o **código binário**!

Na computação, toda a informação é processada pela máquina através do código binário, que usa como base o sistema binário para converter os valores 0 e 1 dos pulsos elétricos em informações. Observe a imagem abaixo, nela nós temos a representação de 1 bit como ligado (ON) e abaixo nós temos 8 dígitos que representam 1 Byte formado pelos bits 10101100 (acho que agora foi, não é?).

![A imagem mostra duas fileiras, a primeira simboliza um bit e apresenta duas bolinhas, uma pintada na cor preta e simboliza ligado e a outra transparente que simboliza o desligado. Logo abaixo há uma fileira de oito bolinhas, que por sua vez representam um byte, as bolinhas estão preto é igual a ligado, que é a mesma coisa que um bit e representa o número 1 e o desligado é o número zero. Dessa forma, na sequência 10101100.](https://www.alura.com.br/artigos/assets/sistema-codigo-binario/imagem12.png)

Fonte: [computerhope.com](https://www.computerhope.com/jargon/b/bit.htm)

Certo, essa parte já entendemos, **mas o que é e como se constrói um código binário?**

O código binário é compostos por algumas combinações de 0 e 1. O “alfabeto” binário apresenta algumas formas de organização de informações, podemos observar na tabela abaixo:

Nome da unidade

Base Dois

Número de bits

bit

2¹

1

Byte

2⁸

8

Kilobyte

2¹⁸

8.192

megabyte

2²⁸

8.388.608

gigabyte

2³⁸

8.589.934.592

terabyte

2⁴⁸

8.796.093.022.208

**1 bit** é o _binary digit_, que em tradução livre é o dígito binário. Essa é a menor unidade de informação do computador , você pode desejar compartilhá-la ou armazená-la com seus dois valores: 0 ou 1.

Por sua vez o **Byte**, a partir do agrupamento de 8 bits (arquitetura popularizada pela IBM nos anos 60), é uma unidade de informação digital para representar letras, símbolos ou números, por exemplo, e facilita o processo das informações enviadas ao computador.

De forma simples, 1 Byte é a soma de 8 bits

**bit + bit + bit + bit + bit + bit +bit + bit = 1 byte** ou **1 byte = 8 bits**

Trabalhar com textos também é outra forma de codificação, utilizamos amplamente o código ASCII e o UTF-8, vamos conhecer um pouco mais?

## Códigos ASCII, UNICODE e UTF-8

**O Código ASC II, American Standard Code for Information Interchange - Código Padrão Americano para o Intercâmbio de Informação**, é um esquema de codificação de caracteres alfanuméricos. Podemos representar letras, símbolos, números , espaço, aspas, dentre outros. Há vários tipos de esquemas e é até comum nós, brasileiros, termos certos problemas no momento de acentuar palavras, por exemplo, por isso precisamos selecionar o padrão correto e evitar essas ocorrências.

O UNICODE é o padrão de codificação de caracteres da internet, foi baseado no [ISO/IEC 10646](https://en.wikipedia.org/wiki/Universal_Coded_Character_Set), e foi pensando para tratar os milhares sistemas de codificação que surgiram. Por isso incorpora os padrões UTF, UTF-12, UTF-32 e UTF-8.

Já o UTF-8 é largamente consumido na web e o padrão estava presente em 95% de todos os sites em 2020. Cada caractere é representado por 1 a 4 bytes e uma de suas vantagens é ser compatível com versões antigas do ASCII . Além disso, cada byte reserva alguns bits para codificação, o que é diferente do ASCII, e por isso há menor possibilidade de bytes serem corrompidos no momento de conversão do UTF-8.

Eu estava curiosa e fui testar para ver se funcionava, você quer tentar também? Desafio você a converter o binário em texto, vamos tentar com o código abaixo:

|**01000001 01101100 01110101 01110010 01100001**|

Você pode usar a [tabela ASCII](https://www.ime.usp.br/~pf/algoritmos/apend/ascii.html) e converter bit a bit ou pode usar um conversor aqui neste link [Conversor online de binário para UTF8](https://onlineutf8tools.com/convert-binary-to-utf8).

E aí? O que apareceu para você? Compartilhe em suas redes e marca a gente 😊

## Conclusão

Talvez realizar conversão de decimal para binário e vice-versa não tenha muito sentido na rotina de desenvolvimento, mas certamente me ajudou muito a visualizar o funcionamento do sistema binário e como a relação de posicionamento e deslocamento dos algarismos está diretamente conectada com o funcionamento da memória e processamento de informações. Entender um pouco mais sobre as ferramentas que a gente utiliza é um passo fundamental para aproveitar melhor os recursos disponíveis e evitar até mesmo eventuais bugs em nosso código. Afinal… quem nunca se deparou com o problema de ponto flutuante causado pela conversão de decimal para binário?