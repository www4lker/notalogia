---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-2/implementando-o-codigo-com-ajuda-do-chatgpt/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# criando a raquete do oponente

## criado em: 
-  27-03-2023 - 11:14

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 2/gpt 4 diz como posso fazer o pong mais elegante ainda\|gpt 4 diz como posso fazer o pong mais elegante ainda]]
- tags: 
- Fontes & Links: 

---


````js
// variáveis da bolinha
let xBolinha = 350;
let yBolinha = 200;
let dBolinha = 25;
let raio = dBolinha / 2;

//velocidade da bolinha
let velocidadeXbolinha = 8;
let velocidadeYbolinha = 8;


//variáveis da raquete
let xRaquete = 5
let yRaquete = 150
//let raqueteLar = 150
let raqueteAlt = 90;
let raqueteComp = 10;

//var raquete oponente
let xOponente = 700;
let yOponente = 150;
let velocidadeYoponente;


function setup() {
  createCanvas(720, 400);
}
// FUNÇÃO PRINCIPAL: DESENHO
function draw() {
  background(0);
    
  //bolinha
  circle(xBolinha, yBolinha, dBolinha);
  //raquete
  mostraRaquete(xRaquete, yRaquete)
  mostraRaquete(xOponente, yOponente)
  movimentaRaquete();
  movimentaOponente();
 
  verificaColisaoRaquete();
  verificaColisaoOponente()
  
  xBolinha += velocidadeXbolinha;
  yBolinha += velocidadeYbolinha;
  
  // verifica colisao com a borda
  if(xBolinha + raio > width || xBolinha - raio < 0){
    velocidadeXbolinha *= -1;
  }
    
  if(yBolinha + raio > height || yBolinha - raio < 0){
    velocidadeYbolinha *= -1;
  }
}

function movimentaRaquete(){
  if(keyIsDown(UP_ARROW)) {
    yRaquete -= 10;
  } 
  if(keyIsDown(DOWN_ARROW)) {
    yRaquete += 10;
  } 
}


function movimentaOponente(){
    velocidadeYoponente = yBolinha - yOponente - raqueteComp / 2 - 30;

    yOponente += velocidadeYoponente
    
    }

function mostraRaquete(x, y){
    //raquete (x, y, w, h, [detailX], [detailY])
  rect(x, y, raqueteComp, raqueteAlt); 
  
}

  
function verificaColisaoRaquete(){
  
  if (xBolinha - raio < xRaquete + raqueteComp &&
      xBolinha + raio > xRaquete &&
      yBolinha - raio < yRaquete + raqueteAlt &&
      yBolinha + raio > yRaquete &&
      !(yBolinha + raio > height || yBolinha - raio < 0)
      ){
    velocidadeXbolinha *= -1;
  }
}
  
function verificaColisaoOponente(){
  
  if (xBolinha - raio < xOponente + raqueteComp &&
      xBolinha + raio > xOponente &&
      yBolinha - raio < yOponente + raqueteAlt &&
      yBolinha + raio > yOponente &&
      !(yBolinha + raio > height || yBolinha - raio < 0)
      ){
    velocidadeXbolinha *= -1;
  }  
}

// 1/Separe as funções de movimento e colisão da bola em funções distintas. 2/Use constantes para valores que não mudam, como a largura e altura do paddle.
````

Para separar as funções de movimento e colisão da bola em funções distintas, você pode criar funções separadas para movimentar a bola e verificar a colisão da bola com os limites do campo e com as raquetes.

Para usar constantes para valores que não mudam, você pode definir constantes para a largura e altura das raquetes, bem como para a velocidade máxima da bola e a largura e altura da bola. Isso pode ajudar a tornar o código mais legível e facilitar a manutenção.

Aqui está um exemplo de como essas melhorias podem ser implementadas no código:
````js
// constantes const RAQUETE_ALTURA = 90; const RAQUETE_COMPRIMENTO = 10; const VELOCIDADE_MAXIMA_BOLA = 8; const BOLA_DIAMETRO = 25;

// variáveis da bolinha let xBolinha = 350; let yBolinha = 200; let raioBola = BOLA_DIAMETRO / 2;

// velocidade da bolinha let velocidadeXbolinha = VELOCIDADE_MAXIMA_BOLA; let velocidadeYbolinha = VELOCIDADE_MAXIMA_BOLA;

// variáveis da raquete let xRaquete = 5; let yRaquete = 150; let xOponente = 700; let yOponente = 150;

function setup() { createCanvas(720, 400); }

// FUNÇÃO PRINCIPAL: DESENHO function draw() { background(0);

// bolinha desenhaBola(xBolinha, yBolinha); movimentaBola(); verificaColisaoBolaComBordas(); verificaColisaoBolaComRaquete(xRaquete, yRaquete); verificaColisaoBolaComRaquete(xOponente, yOponente);

// raquetes mostraRaquete(xRaquete, yRaquete); mostraRaquete(xOponente, yOponente); movimentaRaquete(); movimentaOponente(); }

function desenhaBola(x, y) { circle(x, y, BOLA_DIAMETRO); }

function movimentaBola() { xBolinha += velocidadeXbolinha; yBolinha += velocidadeYbolinha; }

function verificaColisaoBolaComBordas() { if (xBolinha + raioBola > width || xBolinha - raioBola < 0) { velocidadeXbolinha *= -1; } if (yBolinha + raioBola > height || yBolinha - raioBola < 0) { velocidadeYbolinha *= -1; } }

function verificaColisaoBolaComRaquete(xRaquete, yRaquete) { if ( xBolinha - raioBola < xRaquete + RAQUETE_COMPRIMENTO && xBolinha + raioBola > xRaquete && yBolinha - raioBola < yRaquete + RAQUETE_ALTURA && yBolinha + raioBola > yRaquete && !(yBolinha + raioBola > height || yBolinha - raioBola < 0) ) { velocidadeXbolinha *= -1; } }
`
```