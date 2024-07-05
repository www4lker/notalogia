---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-2/lp-03-criando-minha-raquete/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# LP 03 Criando minha raquete

## criado em: 
-  26-03-2023 - 14:09

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 2/a logica por tras da função verificaColisaoRaquete\|a logica por tras da função verificaColisaoRaquete]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 2/importando biblioteca p5\|importando biblioteca p5]]
- tags: 
- Fontes & Links: 

---

Em nosso jogo, atualmente temos a bolinha reconhecendo as bordas, mas ainda faltam componentes extremamente importantes: as raquetes. Para a criação da bolinha temos a função `mostraBolinha()` com `circle()`, uma palavra reservada do p5. Não adianta criarmos uma função `raquete()`, pois obteremos um erro indicando que este nome não está definido.

Vamos consultar a documentação acessando "Help & Feedback > Reference", no menu superior do p5. Dentre as funções listadas em _Shape_, está `rect()`, que se refere à forma retangular. Ao ser clicado, teremos alguns exemplos e os parâmetros necessários para seu uso. O X e o Y, que são os primeiros parâmetros, se relacionam à posição do retângulo, enquanto o terceiro e o quarto, W e H, respectivamente, são a largura e a altura.

```css
rect(x, y, w, h, [tl], [tr], [br], [bl])
```

Acrescentaremos a função ao nosso código, passando parâmetros com valores arbitrários para testarmos:

```scss
function draw() {
    background(0);
    mostraBolinha();
    movimentaBolinha();
    verificaColisaoBorda();
    rect(5, 150, 10, 90);
}
```

Já que neste momento iremos lidar apenas com a raquete, podemos comentar a linha `movimentaBolinha()` para testarmos melhor. E assim como fizemos para a bolinha, criaremos variáveis para armazenar os valores relacionados à raquete — não podemos nos esquecer de substituir os valores antes definidos na função `rect()` por estas variáveis!

```bash
//variáveis da raquete
let xRaquete = 5;
let yRaquete = 150;
let raqueteComprimento = 10;
let raqueteAltura = 90;
```

Por fim, colocaremos todo o código de `rect()` para uma função, visando melhor organização e legibilidade:

```scss
function mostraRaquete() {
    rect(xRaquete, yRaquete, raqueteComprimento, raqueteAltura);
}
```

E então precisaremos executar esta função dentro do `draw()`:

```scss
function draw() {
    background(0);
    mostraBolinha();
    movimentaBolinha();
    verificaColisaoBorda();
    mostraRaquete();
}
```

Em seguida movimentaremos nossa raquete!

---

Nossa raquete ficou bem legal no nosso jogo — seu posicionamento e tamanhos estão da maneira como gostaríamos. No entanto, ela ainda não se movimenta como no Scratch, em que verificávamos se a seta para cima ou para baixo estava pressionada, e para cada um destes casos executávamos uma ação correspondente.

O JavaScript está em inglês, e não em português como no Scratch; ao modificarmos o idioma no Scratch, verificamos como estre trecho fica após a tradução. Será que se escrevermos desta forma no p5 conseguimos o resultado desejado?

Para garantirmos isto, vamos acessar a documentação mais uma vez e buscar por "events". Estão listados eventos de aceleração, teclado, mouse, toque, dentre os quais optaremos por `keyPressed()`. No exemplo dado pela documentação, a cor do retângulo é alterada depois de se pressionar a tecla.

Porém, queremos criar um movimento por meio do uso das setas do teclado, e não mudar a cor da raquete. Voltando à documentação, poderíamos testar cada uma das funções relativas ao _Keyboard_, mas como não há tempo, ficaremos com `keyIsDown()`. Vamos criar uma função para de fato movimentarmos a raquete.

Assim, se a tecla da seta para cima for pressionada, queremos que a raquete se movimente para cima, e para isto é necessário subtrairmos a posição de Y. Faremos algo muito similar para quando a tecla da seta para baixo for pressionada, e teremos o seguinte código:

```csharp
function movimentaMinhaRaquete() {
    if (keyIsDown(UP_ARROW)) {
        yRaquete -= 10;
    }
    if (keyIsDown(DOWN_ARROW)) {
        yRaquete += 10;
    }
}
```

Para que esta função seja executada no bloco `draw()`, incluiremos-na junto às demais:

```scss
function draw() {
    background(0);
    mostraBolinha();
    //movimentaBolinha();
    verificaColisaoBorda();
    mostraRaquete();
    movimentaMinhaRaquete();
}
```

Testaremos pressionando as teclas de seta para cima e para baixo, e repararemos que há um som vinculado a estes movimentos, colocado pelo p5 por questões de **acessibilidade**. Podemos ativá-lo ou desativá-lo clicando no ícone de engrenagem no canto superior direito da tela, na aba "Accessibility". Por ora, desmarcaremos as _checkboxes_ de "Plain-text", "Table-text" e "Sound".

> Para que possamos testar o jogo no p5, é necessário dar ênfase à tela do jogo, isto é, clicar nela após pressionarmos o ícone de play.

Já fizemos com que a raquete se movimente por meio das setas do teclado! E para que o jogo funcione, descomentaremos `movimentaBolinha()` e testaremos novamente. A bolinha parece ultrapassar a raquete, ignorando sua existência, o que pode ser percebido com maior clareza se diminuirmos a velocidade da bolinha. Além disso, poderemos comentar a linha `yBolinha += velocidadeYBolinha`, para que o movimento só aconteça no eixo X.

Assim como no Scratch, queremos criar uma colisão entre a raquete e a bolinha, portanto criaremos a função `verificaColisaoRaquete()`, que chamaremos dentro de `draw()` e será bem parecida com o que temos em `verificaColisaoBorda()`.

```csharp
function verificaColisaoRaquete() {
    if (xBolinha - raio < xRaquete + raqueteComprimento) {
        velocidadeXBolinha *= -1;
    }
}
```

A colisão funciona bem, então testaremos posicionar a raquete para cima do nível em que a bolinha se locomove horizontalmente. Mesmo sem tocar a raquete, ela deixa de tocar a borda lateral esquerda. O mesmo acontece se mantivermos a raquete abaixo do nível de locomoção horizontal da bolinha.

Isto acontece pois definimos que se `xBolinha - raio < xRaquete + raqueteComprimento`, a bolinha deverá mudar de direção. Não especificamos a posição de Y da bolinha em relação à posição de Y da nossa raquete. Para isso, não precisaremos criar um `if` para verificar se a bolinha está acima, ou abaixo da raquete.

Queremos inverter a velocidade de X caso haja colisão, portanto incluiremos mais duas verificações:

```csharp
function verificaColisaoRaquete() {
    if (xBolinha - raio < xRaquete + raqueteComprimento
        && yBolinha - raio < yRaquete + raqueteAltura
        && yBolinha + raio > yRaquete) {
        velocidadeXBolinha *= -1;
    }
}
```

Agora que conseguimos corrigir isso, voltaremos a velocidade da bolinha para `6` e descomentaremos todos os trechos de código que estavam comentados.