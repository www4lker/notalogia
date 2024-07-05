---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-2/versao-final-pong-com-placar-e-som/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# versão final PONG com Placar e SOM

## criado em: 
-  27-03-2023 - 14:36

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 2/Usando ia para estudar mais a fundo\|Usando ia para estudar mais a fundo]]
- tags: 
- Fontes & Links: 

---
>seguem algumas sugestões para melhorar a legibilidade do código, como você mencionou:

1.  Utilize constantes para valores que não serão alterados, como você já fez com `xOponente`, `xRaquete`, etc.
2.  Separe o código em funções menores, responsáveis por tarefas específicas, como você já fez com funções como `moverBolinha()`, `mostraRaquete()`, etc.
3.  Utilize nomes de variáveis mais descritivos que indiquem claramente sua finalidade. Por exemplo, em vez de usar `x` e `y` como argumentos para a função `mostraRaquete(x, y)`, você pode usar `xRaquete` e `yRaquete`.

Você já aplicou essas dicas em grande parte do seu código, o que o torna bastante legível. Removendo a linha problemática mencionada acima, o código deve funcionar corretamente.


```js
// dicas para melhor legibilidade: 1 use contantes, 2 crie funções separadas, 3 use nome de variáveis mais descritivos


// variáveis da bolinha

const xBolinhaInicial = 350;
const yBolinhaInicial = 200;
const diametroBolinha = 25;
const raio = diametroBolinha / 2;

// velocidade da bolinha

let xBolinhaVel = 8;
let yBolinhaVel = 8;

// variáveis da raquete 

const xRaquete = 5;
const yRaqueteInicial = 150;
const raqueteAltura = 90;
const raqueteComprimento = 10;


// variáveis do oponente

const xOponente = 700;
const yOponenteInicial = 150;

let xBolinha = xBolinhaInicial;
let yBolinha = xBolinhaInicial;
let yRaquete = yRaqueteInicial;
let yOponente = yOponenteInicial;
let velocidadeOponente;

// placar do jogo
let meusPontos = 0;
let pontosDoOponente = 0;

// sons do jogo

let raquetada;
let ponto;

function preload() {
    ponto = loadSound("ponto.mp3");
    raquetada = loadSound("raquetada.mp3");
}

// funções iniciais: canvas e draw (se houvesse um so de fundo em loop ia aqui também)

function setup() {
  createCanvas(720, 400);
}

// Função Desenhar

function draw() {
  background(0);
  
  mostraRaquete(xRaquete, yRaquete);
  mostraRaquete(xOponente, yOponente);
  incluiPlacar();
  marcaPonto();
  moverRaquete();
  moverOponente();

  checarColisãoRaquete(xRaquete, yRaquete);
  checarColisãoRaquete(xOponente, yOponente);

  moverBolinha();

  circle(xBolinha, yBolinha, diametroBolinha);

}

function moverBolinha() {
  xBolinha += xBolinhaVel;
  yBolinha += yBolinhaVel;

  if (xBolinha + raio > width || xBolinha - raio < 0){

    xBolinhaVel *= -1;
  }
  if (yBolinha + raio > height || yBolinha - raio < 0){
    yBolinhaVel *= -1;
  }
}

function moverRaquete(){

  if (keyIsDown(UP_ARROW)) {

    yRaquete -= 10;
  }

  if (keyIsDown(DOWN_ARROW)) {

    yRaquete += 10;
  }
}

function marcaPonto() {
    if (xBolinha > 705) {
        meusPontos += 1;
      ponto.play();
    }
    if (xBolinha < 10) {
        pontosDoOponente += 1;
      ponto.play();
    }
}

function incluiPlacar() {
    stroke(255);
    textAlign(CENTER);
    textSize(16);
    fill(color(255, 140, 0));
    rect(150, 10, 40, 20);
    fill(255);
    text(meusPontos, 170, 26);
    fill(color(255, 140, 0));
    rect(450, 10, 40, 20);
    fill(255);
    text(pontosDoOponente, 470, 26);
}

function moverOponente(){
  
  velocidadeOponente = yBolinha - yOponente - raqueteComprimento / 2 - 30;
  yOponente += velocidadeOponente;

}
function mostraRaquete(x, y){

    rect(x, y, raqueteComprimento, raqueteAltura);
}

function checarColisãoRaquete(x, y){
  if (

    xBolinha - raio < x + raqueteComprimento &&
    xBolinha + raio > x &&
    yBolinha - raio < y + raqueteAltura &&
    yBolinha + raio > y 
  ) {
    xBolinhaVel *= -1;
    raquetada.play();
  }
} 
```