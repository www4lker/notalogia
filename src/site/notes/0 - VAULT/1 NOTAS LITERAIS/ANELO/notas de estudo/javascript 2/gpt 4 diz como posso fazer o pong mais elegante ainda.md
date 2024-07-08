---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-2/gpt-4-diz-como-posso-fazer-o-pong-mais-elegante-ainda/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# gpt 4 diz como posso fazer o pong mais elegante ainda

## criado em: 
-  27-03-2023 - 12:06

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 2/versão final PONG com Placar e SOM\|versão final PONG com Placar e SOM]]
- tags: 
- Fontes & Links: 

---

>Analise meu código erm javascript de um simples jogo chamado pong: gostaria de saber como posso simplificar ainda mais este codigo tornado-o até mesmo "belo": 

Parabéns pelo seu código! Para tornar seu código ainda mais simples e elegante, aqui estão algumas sugestões:

1.  Use constantes para valores que não mudam: isso torna seu código mais fácil de ler e entender. Por exemplo, use `const` para definir largura, altura e outros valores que não mudam.
    
2.  Crie funções separadas para lidar com colisões e movimento da bola: isso torna seu código mais modular e fácil de entender.
    
3.  Use nomes de variáveis mais descritivos em inglês para facilitar a leitura por outros desenvolvedores.

```js

// Ball variables
const ballXStart = 350;
const ballYStart = 200;
const ballDiameter = 25;
const ballRadius = ballDiameter / 2;

// Ball speed
let ballSpeedX = 8;
let ballSpeedY = 8;

// Paddle variables
const paddleX = 5;
const paddleYStart = 150;
const paddleHeight = 90;
const paddleWidth = 10;

// Opponent variables
const opponentX = 700;
const opponentYStart = 150;

let ballX = ballXStart;
let ballY = ballYStart;
let paddleY = paddleYStart;
let opponentY = opponentYStart;
let opponentSpeedY;

function setup() {
  createCanvas(720, 400);
}

function draw() {
  background(0);

  displayPaddle(paddleX, paddleY);
  displayPaddle(opponentX, opponentY);
  movePaddle();
  moveOpponent();

  checkPaddleCollision(paddleX, paddleY);
  checkPaddleCollision(opponentX, opponentY);

  moveBall();

  circle(ballX, ballY, ballDiameter);
}

function moveBall() {
  ballX += ballSpeedX;
  ballY += ballSpeedY;

  if (ballX + ballRadius > width || ballX - ballRadius < 0) {
    ballSpeedX *= -1;
  }

  if (ballY + ballRadius > height || ballY - ballRadius < 0) {
    ballSpeedY *= -1;
  }
}

function movePaddle() {
  if (keyIsDown(UP_ARROW)) {
    paddleY -= 10;
  }
  if (keyIsDown(DOWN_ARROW)) {
    paddleY += 10;
  }
}

function moveOpponent() {
  opponentSpeedY = ballY - opponentY - paddleWidth / 2 - 30;
  opponentY += opponentSpeedY;
}

function displayPaddle(x, y) {
  rect(x, y, paddleWidth, paddleHeight);
}

function checkPaddleCollision(x, y) {
  if (
    ballX - ballRadius < x + paddleWidth &&
    ballX + ballRadius > x &&
    ballY - ballRadius < y + paddleHeight &&
    ballY + ballRadius > y
  ) {
    ballSpeedX *= -1;
  }
}
