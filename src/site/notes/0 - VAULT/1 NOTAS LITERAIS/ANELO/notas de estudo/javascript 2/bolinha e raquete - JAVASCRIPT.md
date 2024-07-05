---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-2/bolinha-e-raquete-javascript/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# bolinha e raquete - JAVASCRIPT

## criado em: 
-  25-03-2023 - 14:27

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 2/p5, do que se trata\|p5, do que se trata]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 2/Logica de programação - comece com o jogo pong no js\|Logica de programação - comece com o jogo pong no js]]
- tags: 
- Fontes & Links: 

---
Desenvolvemos nosso jogo e consolidamos a lógica de programação! Agora, vamos desenvolvê-lo em outra linguagem de programação, o JavaScript. Mas onde iremos fazer isso, e como iremos visualizá-lo?

Utilizaremos um serviço Web chamado [p5.js](http://editor.p5js.org), que exige cadastro de uma conta para podermos salvar os nossos projetos. Iremos manter o Scratch aberto, também, para fazermos algumas comparações. Nele, temos o ícone de bandeira verde, enquanto no p5 temos um botão de play que, ao ser pressionado, habilita um quadrado de "Preview"; na área de código, há algumas linhas preexistentes.

O fundo cinza em "Preview" é criado a partir da função `createCanvas()`, que possui dois valores, ambos `400`. Vamos testar alterando somente o primeiro para `800`. Isto fará com que a largura do retângulo cinza, que é onde será exibido nosso jogo, aumente. As alterações feitas no código se refletem ao seu lado conforme são feitas.

Também temos a função `background()`, cujo valor _default_ é `220`. Trocaremos para `260`, e o fundo ficará todo branco, em vez de cinza. Quanto menor este valor, mais escuro fica o fundo do retângulo que antes era cinza. Por isto, deixaremos `0` para que o fundo do nosso jogo fique preto.

Há um problema: no Scratch, todo o código fica visível e é intuitivo montá-los, bastando buscá-los de acordo com o que queremos fazer dentre as opções disponibilizadas. Começaremos desenhando uma bolinha, tal como fizemos no Scratch. Simplesmente escrever `circulo` dentro do bloco de código de `draw()` não nos traz nenhum retorno, e ainda dá erro — "circulo is not defined", ou "circulo não está definido".

Para buscarmos pelos códigos necessários, clicaremos em "Help & Feedback" e em "Reference", o que abrirá uma nova aba. Em _Shape_, dentre as funções listadas, está `circle()` que, após clicarmos, exibirá um exemplo: `circle(30, 30, 20)`. Descendo um pouco a página, temos a explicação da sua sintaxe, `circle(x, y, d)`, cujos parâmetros são, respectivamente, a coordenada no eixo X, no eixo Y e o diâmetro do círculo.

> Lembrando que o diâmetro é o dobro do raio de uma circunferência, que é a linha que liga o centro da mesma à sua borda.

O trecho de código ficará, portanto, assim:

```scss
function setup() {
    createCanvas(600, 400);
}

function draw() {
    background(0);
    circle(0, 0, 50);
}
```

Ao pressionarmos o botão de play, teremos cerca de 1/4 do círculo posicionado no canto superior esquerdo da tela. Por quê será que isso acontece? No Scratch, definimos como posição inicial da bolinha a coordenada (0, 0), a partir do centro, enquanto aqui o plano cartesiano, isto é, a movimentação nos eixos X e Y será um pouco diferente: o (0, 0) da nossa tela passa a ser o extremo canto superior esquerdo, exatamente onde se encontra a bolinha no momento.

Será necessário, portanto, aumentar os valores deles para que a bolinha fique visível e localizada no centro da tela. E para que o código fique ainda mais claro e legível, armazenaremos tais valores em variáveis, usando a palavra `let`:

```csharp
let xBolinha = 300;
let yBolinha = 200;
let diametro = 15;

function setup() {
    createCanvas(600, 400);
}

function draw() {
    background(0);
    circle(xBolinha, yBolinha, diametro);
}
```

> As nomenclaturas de variáveis seguem a convenção de terem a primeira letra da primeira palavra em minúscula, e as primeiras letras das demais palavras, se houver, em maiúscula. Esta convenção se denomina **Camel Case**.

Agora, precisaremos fazer com que ela se movimente, em ambos os eixos. Para isso, indicaremos na função `draw()` que `xBolinha` sempre terá acréscimo de `1`, o que fará com que a bolinha se movimente para a direita, em linha reta.

```csharp
function draw() {
    background(0);
    circle(xBolinha, yBolinha, diametro);
    xBolinha = xBolinha + 1;
}
```

O `1`, então, seria a velocidade com que a bolinha se movimenta, porém isto não fica claro em nosso código. Criaremos a variável `velocidadeXBolinha`, para a qual atribuiremos o valor `6`, para testarmos, e teremos `xBolinha = xBolinha + velocidadeXBolinha`. Com isto, a bolinha se locomove para a direita até sumir da tela.

Uma forma mais elegante de escrevermos esta mesma linha é `xBolinha += velocidadeXBolinha`, ou seja, o X da bolinha será seu valor acrescido de sua velocidade. Como queremos que a bolinha se movimente para direções distintas, criaremos `yBolinha`, e a variável `velocidadeYBolinha`, com valor `6`.

```csharp
let xBolinha = 300;
let yBolinha = 200;
let diametro = 15;

let velocidadeXBolinha = 6;
let velocidadeYBolinha = 6;

function setup() {
    createCanvas(600, 400);
}

function draw() {
    background(0);
    circle(xBolinha, yBolinha, diametro);
    xBolinha += velocidadeXBolinha;
    yBolinha += velocidadeYBolinha;
}
```

Assim, sempre que iniciarmos o jogo, a bolinha surgirá do centro, indo para baixo diagonalmente até desaparecer na tela. Não é bem isso que queremos, e sim que ela permaneça dentro das bordas da tela. Faremos isso a seguir!

A bolinha está se movendo para além das bordas do nosso jogo, e não é este o comportamento que queremos. Queremos que, assim que ela toque uma das bordas, ela inverta a posição, assim como fizemos no Scratch. Para isto, precisamos verificar se ela está tocando a borda em algum momento, dentro da função que está desenhando o nosso jogo (`draw()`).

Na programação, esta verificação, o "se", é escrito com `if`, e usaremos uma variável que o próprio p5 disponibiliza. Além disso, comentaremos a linha contendo `yBolinha`. Se `xBolinha` for maior que a largura (`width`) da tela, queremos fazer algo, que por sua vez estará entre chaves (ou "bigodes"). No caso, iremos multiplicar `velocidadeXBolinha` por `-1`, para que ela se movimente no sentido oposto.

```csharp
function draw() {
    background(0);
    circle(xBolinha, yBolinha, diametro);
    xBolinha += velocidadeXBolinha;
    //yBolinha += velocidadeYBolinha;

    if (xBolinha > width) {
        velocidadeXBolinha *= -1;
    }
}
```

Ao testarmos este código, a bolinha parte da área central da tela, colide com a lateral direita da tela, inverte o sentido, e desaparece quando ultrapassa a lateral esquerda da tela. Sabemos que esta lateral esquerda é o X = 0, portanto acrescentaremos outra condição no código, por meio de duas barras verticais, o que quer dizer "ou":

```undefined
if (xBolinha > width || xBolinha < 0) {
    velocidadeXBolinha *= -1;
}
```

Desta vez, temos a bolinha reconhecendo tanto o limite lateral direito quanto o esquerdo. Para lidarmos com os movimentos verticais, descomentaremos a linha com `yBolinha` e comentaremos a linha com `xBolinha`, para melhor entendimento. Faremos algo bem similar ao que fizemos anteriormente, em relação a X, mas desta vez lidaremos com a altura (`height`) da tela.

```csharp
function draw() {
    background(0);
    circle(xBolinha, yBolinha, diametro);
    //xBolinha += velocidadeXBolinha;
    yBolinha += velocidadeYBolinha;

    if (xBolinha > width || xBolinha < 0) {
        velocidadeXBolinha *= -1;
    }
    if (yBolinha > height || yBolinha < 0) {
        velocidadeYBolinha *= -1;
    }
}
```

Descomentaremos a linha com `xBolinha` e verificaremos que as bordas estão sendo reconhecidas, como gostaríamos.

---

Alteraremos as velocidades relativas tanto ao eixo X quanto ao eixo Y para `2` para deixar a bolinha mais lenta e assim conseguirmos observar melhor estes movimentos. Uma parte da bolinha ainda ultrapassa os limites das bordas, e não queremos que isso aconteça. Vamos voltar às velocidades originais, `6`, e pensar no porquê disso estar acontecendo.

Na documentação do `circle()`, é indicado que o X é o centro do círculo, o que será levado em consideração para que se reconheça que houve uma colisão da bolinha com alguma das bordas. No entanto, queremos que isto se dê a partir do raio, isto é, das extremidades da bolinha. Uma vez que o diâmetro é 2x o valor do raio, criaremos a variável `raio`, que receberá `diametro / 2`.

Com isso, diminuiremos as velocidades da bolinha novamente (para `2`), para enxergarmos melhor os movimentos, e comentaremos a linha com `yBolinha` para testar primeiro no eixo X, em que somaremos o valor do raio para o lado direito, e subtrairemos o mesmo valor do lado esquerdo:

```undefined
if (xBolinha + raio > width || xBolinha - raio < 0) {
    velocidadeXBolinha *= -1;
}
```

Em seguida, descomentaremos a linha com `yBolinha` e comentaremos a linha com `xBolinha`. Da mesma forma como fizemos em relação ao eixo X, para o eixo vertical teremos:

```undefined
if (yBolinha + raio > height || yBolinha - raio < 0) {
    velocidadeYBolinha *= -1;
}
```

Voltaremos a velocidade da bolinha para `6` e testaremos mais uma vez, agora sem nenhum trecho comentado. Nossa bolinha está reconhecendo todas as bordas da tela do jogo!

---

Em nosso jogo, criamos uma bolinha e verificamos suas colisões com as bordas e, para que pudéssemos ter este resultado, criamos variáveis para a bolinha, melhorando a legibilidade do código. Na função `draw()` fazemos várias ações: desenhamos e movimentamos a bolinha dentro de uma determinada área, e verificamos se a bolinha está de fato colidindo ou não com as bordas.

Será que existe uma maneira de deixarmos nosso código ainda melhor?

Poderemos fazê-lo sem alterar seu comportamento por meio da **refatoração** e o uso de funções para melhor identificarmos cada trecho de código. Fora do escopo de `draw()`, criaremos a função `mostraBolinha()`, mas isto não será o suficiente, pois é necessário chamá-la em `draw()`. Do mesmo modo, criaremos `movimentaBolinha()` e `verificaColisaoBorda()`

```csharp
function draw() {
    background(0);
    mostraBolinha();
    movimentaBolinha();
    verificaColisaoBorda();
}

function mostraBolinha() {
    circle(xBolinha, yBolinha, diametro)
}

function movimentaBolinha() {
    xBolinha += velocidadeXBolinha;
    yBolinha += velocidadeYBolinha;
}

function verificaColisaoBorda() {
    if (xBolinha + raio > width || xBolinha - raio < 0) {
        velocidadeXBolinha *= -1;
    }
    if (yBolinha + raio > height || yBolinha - raio < 0) {
        velocidadeYBolinha *= -1;
    }
}
```

Continuando, as variáveis `xBolinha`, `yBolinha`, `diametro` e `raio` se referem à bolinha, portanto poderemos adicionar um comentário `//variáveis da bolinha`, assim como um `//variáveis da velocidade da bolinha` logo acima das linhas que contém `velocidadeXBolinha` e `velocidadeYBolinha`.

```bash
//variáveis da bolinha
let xBolinha = 300;
let yBolinha = 200;
let diametro = 15;
let raio = diametro / 2;

//velocidade da bolinha
let velocidadeXBolinha = 6;
let velocidadeYBolinha = 6;
```

Esta é uma das formas de melhorarmos nosso código, deixando-o mais compreensível e organizado, sem modificar o comportamento final.