---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/js-e-html-logica-de-programacao-final/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# JS e HTML - LOGICA DE PROGRAMAÇÃO -  FINAL

## criado em: 
-  29-03-2023 - 14:54

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/js e html - colirio no olho\|js e html - colirio no olho]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/cheat sheet de operadores logicos\|cheat sheet de operadores logicos]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Lógica de programação - 36 horas\|Lógica de programação - 36 horas]]
- tags: #ANELO 
- Fontes & Links: https://cursos.alura.com.br/course/logica-programacao-pratica-com-desenho-animacoes-em-jogo/task/21890

---

Este objeto é construído pela função `desenhaCirculo()`, que já temos em nosso código:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    function desenhaCirculo(x, y, raio) {

        pincel.fillStyle = 'blue';
        pincel.beginPath();
        pincel.arc(x, y, raio, 0, 2 * Math.PI);
        pincel.fill();

    }

    function limpaTela() {

        pincel.clearRect(0, 0, 600, 400);
    }
</script>
```

Ela deverá receber mais um parâmetro (a `cor`) e será utilizado no `fillStyle`. Temos isso porque haverá círculos na cor branca e vermelha:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    function desenhaCirculo(x, y, raio, cor) {

        pincel.fillStyle = cor;
        pincel.beginPath();
        pincel.arc(x, y, raio, 0, 2 * Math.PI);
        pincel.fill();
    }

    function limpaTela() {

        pincel.clearRect(0, 0, 600, 400);

    }

</script>
```

Além disso, temos que saber que nosso raio padrão terá o valor inicial de `10`, os demais serão maiores, para criar a imagem de um alvo.

Para efetivamente desenharmos o círculos, temos que chamar a função `desenhaCirculo()`, com os parâmetros `x` e `y` ambos com valor `100`, raio `10` e a cor vermelha (`red`), já que estamos lidando com o círculo central:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    function desenhaCirculo(x, y, raio, cor) {

        pincel.fillStyle = cor;
        pincel.beginPath();
        pincel.arc(x, y, raio, 0, 2 * Math.PI);
        pincel.fill();

    }

    function limpaTela() {

        pincel.clearRect(0, 0, 600, 400);

    }

    desenhaCirculo(100, 100, 10, 'red');

</script>
```

O próximo círculo será construído na mesma posição, entretanto, o seu raio será maior, equivalente a `30`, e sua cor será branca (`white`):

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    function desenhaCirculo(x, y, raio, cor) {

        pincel.fillStyle = cor;
            pincel.beginPath();
        pincel.arc(x, y, raio, 0, 2 * Math.PI);
        pincel.fill();

    }

    function limpaTela() {

        pincel.clearRect(0, 0, 600, 400);

    }

    desenhaCirculo(100, 100, 10, 'red');
    desenhaCirculo(100, 100, 30, 'white');

</script>
```

Por fim, desenharemos um círculo ainda maior, com raio `40`, e novamente na cor vermelha (`red`):

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    function desenhaCirculo(x, y, raio, cor) {

        pincel.fillStyle = cor;
        pincel.beginPath();
        pincel.arc(x, y, raio, 0, 2 * Math.PI);
        pincel.fill();

    }

    function limpaTela() {

        pincel.clearRect(0, 0, 600, 400);

    }

    desenhaCirculo(100, 100, 10, 'red');
    desenhaCirculo(100, 100, 30, 'white');
    desenhaCirculo(100, 100, 40, 'red');

</script>
```

Salvaremos e recarregaremos a página. Por que será exibido somente um círculo vermelho? Porque a última função que passamos foi para a criação de um círculo maior que todos os demais, assim, ela cobriu todas as outras. Como consertaremos isso?

Basta invertermos a ordem de chamamento das funções, se chamarmos o círculo vermelho maior primeiro, e o círculo vermelho menor por último, da seguinte forma:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    function desenhaCirculo(x, y, raio, cor) {
    pincel.fillStyle = cor;
    pincel.beginPath();
    pincel.arc(x, y, raio, 0, 2 * Math.PI);
    pincel.fill();

    }

    function limpaTela() {

    pincel.clearRect(0, 0, 600, 400);
    }

    desenhaCirculo(100, 100, 40, 'red');
    desenhaCirculo(100, 100, 30, 'white');
    desenhaCirculo(100, 100, 10, 'red');

</script>
```

Aprimoraremos nosso código, usando o raio inicial de `10` como parâmetro, guardando-o em uma variável. Em seguida, acrescentaremos os valores necessários para compor os raios das demais circunferências. Criaremos a variável `raio = 10` a seguir:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;

    function desenhaCirculo(x, y, raio, cor) {

        pincel.fillStyle = cor;
        pincel.beginPath();
        pincel.arc(x, y, raio, 0, 2 * Math.PI);
        pincel.fill();

    }

    function limpaTela() {

       pincel.clearRect(0, 0, 600, 400);
    }

    desenhaCirculo(100, 100, 40, 'red');
    desenhaCirculo(100, 100, 30, 'white');
    desenhaCirculo(100, 100, 10, 'red');

</script>
```

Nos chamamentos das funções, trocaremos os valores pela variável:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;

    function desenhaCirculo(x, y, raio, cor) {
        pincel.fillStyle = cor;
    pincel.beginPath();
    pincel.arc(x, y, raio, 0, 2 * Math.PI);
    pincel.fill();

    }

    function limpaTela() {

    pincel.clearRect(0, 0, 600, 400);
    }

    desenhaCirculo(100, 100, raio+20, 'red');
    desenhaCirculo(100, 100, raio+10, 'white');
    desenhaCirculo(100, 100, raio, 'red');

</script>
```

Salvaremos e recarregaremos a página. Pronto! Temos nosso alvo.

Com o alvo criado, precisamos fazer com que seu aparecimento seja aleatório, ou seja, que sejam criadas coordenadas arbitrárias. Para isso, vamos inserir as instruções para a criação do alvo dentro de uma nova função chamada `desenhaAlvo()`, e a chamaremos logo em seguida:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;

    function desenhaCirculo(x, y, raio, cor) {

        pincel.fillStyle = cor;
        pincel.beginPath();
        pincel.arc(x, y, raio, 0, 2 * Math.PI);
        pincel.fill();

    }

    function limpaTela() {

        pincel.clearRect(0, 0, 600, 400);
    }

    function desenhaAlvo() {

        desenhaCirculo(100, 100, raio+20, 'red');
        desenhaCirculo(100, 100, raio+10, 'white');
        desenhaCirculo(100, 100, raio, 'red');

    }

    desenhaAlvo();

</script>
```

Salvaremos e recarregaremos e podemos ver que o alvo permanece inalterado.

Como queremos que o alvo seja aleatório, a função `desenhaAlvo()` receberá parâmetros referentes às coordenadas X (até o limite de 600) e Y (até o limite de 400), com relação ao `desenhaCirculo()`, elas receberão estes parâmetros, respectivamente:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;

    function desenhaCirculo(x, y, raio, cor) {

    pincel.fillStyle = cor;
    pincel.beginPath();
    pincel.arc(x, y, raio, 0, 2 * Math.PI);
    pincel.fill();

    }

    function limpaTela() {
    pincel.clearRect(0, 0, 600, 400);

    }

    function desenhaAlvo(x, y) {
    desenhaCirculo(x, y, raio+20, 'red');
    desenhaCirculo(x, y, raio+10, 'white');
    desenhaCirculo(x, y, raio, 'red');

    }

    desenhaAlvo();

</script>
```

Para chamar o `desenhaAlvo()`, passaremos os parâmetros `(200, 200)`:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;

    function desenhaCirculo(x, y, raio, cor) {

    pincel.fillStyle = cor;
    pincel.beginPath();
    pincel.arc(x, y, raio, 0, 2 * Math.PI);
    pincel.fill();

    }

    function limpaTela() {

    pincel.clearRect(0, 0, 600, 400);
    }

    function desenhaAlvo(x, y) {

    desenhaCirculo(x, y, raio+20, 'red');
    desenhaCirculo(x, y, raio+10, 'white');
    desenhaCirculo(x, y, raio, 'red');

    }

    desenhaAlvo(200, 200);

</script>
```

A posição do alvo variará de acordo com os valores que passarmos como parâmetros em `desenhaAlvo()`, passaremos, por exemplo `(50, 200)`, e teremos uma posição diferente.

O próximo passo será fazer com que os valores das coordenadas sejam gerados aleatoriamente.

Criaremos uma função chamada `sorteiaPosicao()`, que receberá um valor `maximo` que pode sortear entre 0 a 600 (para o eixo X), e 0 a 400 (para o eixo Y):

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;

    function desenhaCirculo(x, y, raio, cor) {

        pincel.fillStyle = cor;
        pincel.beginPath();
        pincel.arc(x, y, raio, 0, 2 * Math.PI);
        pincel.fill();

    }

    function limpaTela() {

        pincel.clearRect(0, 0, 600, 400);
    }

    function desenhaAlvo(x, y) {

        desenhaCirculo(x, y, raio+20, 'red');
        desenhaCirculo(x, y, raio+10, 'white');
        desenhaCirculo(x, y, raio, 'red');
    }

    function sorteiaPosicao(maximo) {

    }

    desenhaAlvo(50, 200);

</script>
```

Criaremos uma variável `xAleatorio` que recebe `sorteiaPosicao`, já que estamos trabalhando com a variável X, então o valor máximo será `600`. Do mesmo modo, criaremos uma variável `yAleatorio` que receberá `sorteiaPosicao`, cujo máximo será `400`:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;

    function desenhaCirculo(x, y, raio, cor) {
    pincel.fillStyle = cor;
    pincel.beginPath();
    pincel.arc(x, y, raio, 0, 2 * Math.PI);
    pincel.fill();

    }

    function limpaTela() {
    pincel.clearRect(0, 0, 600, 400);

    }

    function desenhaAlvo(x, y) {
    desenhaCirculo(x, y, raio+20, 'red');
    desenhaCirculo(x, y, raio+10, 'white');
    desenhaCirculo(x, y, raio, 'red');

}
    function sorteiaPosicao(maximo) {
    }

    var xAleatorio = sorteiaPosicao(600);
    var yAleatorio = sorteiaPosicao(400);

    desenhaAlvo(50, 200);

</script>
```

O próximo passo é passarmos estes valores para a função `desenhaAlvo()`:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;

    function desenhaCirculo(x, y, raio, cor) {
        pincel.fillStyle = cor;
    pincel.beginPath();
    pincel.arc(x, y, raio, 0, 2 * Math.PI);
    pincel.fill();
    }

    function limpaTela() {
    pincel.clearRect(0, 0, 600, 400);

    }

    function desenhaAlvo(x, y) {

    desenhaCirculo(x, y, raio+20, 'red');
    desenhaCirculo(x, y, raio+10, 'white');
    desenhaCirculo(x, y, raio, 'red');
    }

     function sorteiaPosicao(maximo) {

     }

    var xAleatorio = sorteiaPosicao(600);
    var yAleatorio = sorteiaPosicao(400);

    desenhaAlvo(xAleatorio, yAleatorio);

</script>
```

Ainda precisamos programar a função `sorteiaPosicao()`. Ela nos dará um retorno - `return` - de `Math.floor`, que arredonda o número para baixo, diferente do `Math.round`, que o arredonda para cima. Em seguida temos `Math.random() * maximo):

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;

    function desenhaCirculo(x, y, raio, cor) {

        pincel.fillStyle = cor;
    pincel.beginPath();
    pincel.arc(x, y, raio, 0, 2 * Math.PI);
    pincel.fill();

    }

    function limpaTela() {
        pincel.clearRect(0, 0, 600, 400);
    }

    function desenhaAlvo(x, y) {

    desenhaCirculo(x, y, raio+20, 'red');
    desenhaCirculo(x, y, raio+10, 'white');
    desenhaCirculo(x, y, raio, 'red');

    }

    function sorteiaPosicao(maximo) {

    return Math.floor(Math.random() * maximo);

    }

    var xAleatorio = sorteiaPosicao(600);
    var yAleatorio = sorteiaPosicao(400);

    desenhaAlvo(xAleatorio, yAleatorio);

</script>
```

Sempre que salvarmos e recarregaremos a página, o alvo aparecerá em um novo ponto do nosso `<canvas>`.

Nosso próximo objetivo será fazer com que o alvo seja redesenhado em certos intervalos de tempo, pré-determinados.

Para isso, criaremos uma função `atualizaTela()`, que receberá as variáveis referentes ao X e Y aleatórios, bem como o chamamento de `desenhaAlvo`, da seguinte forma:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;

    function desenhaCirculo(x, y, raio, cor) {

    pincel.fillStyle = cor;
    pincel.beginPath();
    pincel.arc(x, y, raio, 0, 2 * Math.PI);
    pincel.fill();

    }

    function limpaTela() {
        pincel.clearRect(0, 0, 600, 400);
    }

    function desenhaAlvo(x, y) {

    desenhaCirculo(x, y, raio+20, 'red');
    desenhaCirculo(x, y, raio+10, 'white');
    desenhaCirculo(x, y, raio, 'red');

    }

    function sorteiaPosicao(maximo) {
    return Math.floor(Math.random() * maximo);
    }

    function atualizaTela() {

    var xAleatorio = sorteiaPosicao(600);
    var yAleatorio = sorteiaPosicao(400);
    desenhaAlvo(xAleatorio, yAleatorio);

    }

</script>
```

Em seguida, utilizaremos o `setInterval()`, com os parâmetros `atualizaTela` e o intervalo de tempo `500`, sem esquecer de incluir na função o `limpaTela`:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;

    function desenhaCirculo(x, y, raio, cor) {

    pincel.fillStyle = cor;
    pincel.beginPath();
    pincel.arc(x, y, raio, 0, 2 * Math.PI);
    pincel.fill();

    }

    function limpaTela() {
        pincel.clearRect(0, 0, 600, 400);

    }

    function desenhaAlvo(x, y) {
        desenhaCirculo(x, y, raio+20, 'red');
    desenhaCirculo(x, y, raio+10, 'white');
    desenhaCirculo(x, y, raio, 'red');

   }

    function sorteiaPosicao(maximo) {

    return Math.floor(Math.random() * maximo);
    }

    function atualizaTela() {
    limpaTela();

        var xAleatorio = sorteiaPosicao(600);
    var yAleatorio = sorteiaPosicao(400);
    desenhaAlvo(xAleatorio, yAleatorio);

    }

    setInterval(atualizaTela, 500);

</script>
```

Salvaremos e recarregaremos. Pronto! Temos nosso alvo viajando pela tela, em pontos aleatórios. Como ainda está rápido, trocaremos o intervalo de tempo para `1000`:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;

    function desenhaCirculo(x, y, raio, cor) {

        pincel.fillStyle = cor;
        pincel.beginPath();
        pincel.arc(x, y, raio, 0, 2 * Math.PI);
        pincel.fill();

   }

    function limpaTela() {
    pincel.clearRect(0, 0, 600, 400);

    }

    function desenhaAlvo(x, y) {

    desenhaCirculo(x, y, raio+20, 'red');
    desenhaCirculo(x, y, raio+10, 'white');
    desenhaCirculo(x, y, raio, 'red');

    }

    function sorteiaPosicao(maximo) {

        return Math.floor(Math.random() * maximo);

    }

    function atualizaTela() {
    limpaTela();
    var xAleatorio = sorteiaPosicao(600);
    var yAleatorio = sorteiaPosicao(400);
    desenhaAlvo(xAleatorio, yAleatorio);
    }

    setInterval(atualizaTela, 1000);

</script>
```

Nosso próximo objetivo é tornar o objeto responsivo ao clique, com o alerta de que o usuário acertou ao clicar sobre o alvo.

### ultima parte
Criaremos uma função chamada `dispara`, que será executada ao clique de um botão, ou seja, ela pode receber o `evento` como parâmetro, para sabermos qual é a posição do mouse:

```javascript
// parte de cima do código omitida

function atualizaTela() {
    limpaTela();
    var xAleatorio = sorteiaPosicao(600);
    var yAleatorio = sorteiaPosicao(400);
    desenhaAlvo(xAleatorio, yAleatorio);
}

setInterval(atualizaTela, 1000);

function dispara(evento) {

}

</script>
```

Queremos disparar ao clicar no `<canvas>`, para isso, temos que fazer com que o `tela.onclick` receba `dispara`, assim, todas as vezes em que o `<canvas>` for clicado o código da função `dispara` será executado:

```javascript
// parte de cima do código omitida

function atualizaTela() {
    limpaTela();
    var xAleatorio = sorteiaPosicao(600);
    var yAleatorio = sorteiaPosicao(400);
    desenhaAlvo(xAleatorio, yAleatorio);
}

setInterval(atualizaTela, 1000);

function dispara(evento) {

}

tela.onclick = dispara;

</script>
```

Precisamos saber, também, onde o usuário clicou, para determinar se foi ou não sobre o alvo. Para isso, teremos - dentro da função `dispara`, uma variável `x` que recebe `evento.pageX` e outra `y` que recebe `evento.pageY`. Além disso, precisaremos remover o `tela.offsetLeft`, para o eixo X, e o `tela.offsetTop` para o eixo Y:

```javascript
// parte de cima do código omitida

function atualizaTela() {
    limpaTela();
    var xAleatorio = sorteiaPosicao(600);
    var yAleatorio = sorteiaPosicao(400);
    desenhaAlvo(xAleatorio, yAleatorio);
}

setInterval(atualizaTela, 1000);

function dispara(evento) {

    var x = evento.pageX - tela.offsetLeft;
    var y = evento.pageY - tela.offsetTop;

}

tela.onclick = dispara;

</script>
```

Faremos então a lógica de detecção. Criaremos um `if`, com um `alert` contendo a mensagem `Acertou!`. Precisamos nos certificar de que as coordenas X e Y estão dentro do escopo do alvo, entretanto, temos de saber também o X aleatório e o Y aleatório do alvo. Só que estas variáveis foram declaradas dentro do `atualizaTela`:

```javascript
// parte de cima do código omitida

function atualizaTela() {
    limpaTela();
    var xAleatorio = sorteiaPosicao(600);
    var yAleatorio = sorteiaPosicao(400);
    desenhaAlvo(xAleatorio, yAleatorio);
}

setInterval(atualizaTela, 1000);

function dispara(evento) {

    var x = evento.pageX - tela.offsetLeft;
    var y = evento.pageY - tela.offsetTop;

    if() {

        alert('Acertou!');

    }

}

tela.onclick = dispara;

</script>
```

E uma variável declarada com `var`, dentro de uma função, existe **somente** dentro desta, só pode ser acessada neste contexto, portanto, se tentarmos acessar o `xAleatorio` fora da função `atualizaTela`, o programa informará que `xAleatorio` não foi definido.

Como podemos então ter acesso a estas variáveis, para que possamos executar nossa lógica?

Primeiro, removeremos o `var` de dentro da função `atualizaTela`, e as inicializaremos logo abaixo de `var raio = 10`, e elas serão iniciadas sem valor nenhum:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;
        var xAleatorio = sorteiaPosicao;
        var yAleatorio = sorteiaPosicao;

    function desenhaCirculo(x, y, raio, cor) {

        pincel.fillStyle = cor;
        pincel.beginPath();
        pincel.arc(x, y, raio, 0, 2 * Math.PI);
        pincel.fill();

    }

    function limpaTela() {

        pincel.clearRect(0, 0, 600, 400);

    }

    function desenhaAlvo() {

        desenhaCirculo(x, y, raio+20, 'red');
        desenhaCirculo(x, y, raio+10, 'white');
        desenhaCirculo(x, y, raio, 'red');

    }

    function sorteiaPosicao(maximo) {

        return Math.floor(Math.random() * maximo);

    }

function atualizaTela() {x
    limpaTela();
    xAleatorio = sorteiaPosicao(600);
    yAleatorio = sorteiaPosicao(400);
    desenhaAlvo(xAleatorio, yAleatorio);
}

setInterval(atualizaTela, 1000);

function dispara(evento) {

    var x = evento.pageX - tela.offsetLeft;
    var y = evento.pageY - tela.offsetTop;

    if() {

        alert('Acertou!');

    }

}

tela.onclick = dispara;

</script>
```

Como agora as variáveis foram inicializadas fora da função, elas podem ser lidas e inicializadas por quaisquer uma das funções presentes. Agora, podemos acessar o `xAleatorio` e o `yAleatorio` dentro da função `dispara`. Por enquanto, deixaremos o `if` em comentários:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;
        var xAleatorio = sorteiaPosicao;
        var yAleatorio = sorteiaPosicao;

    function desenhaCirculo(x, y, raio, cor) {

        pincel.fillStyle = cor;
        pincel.beginPath();
        pincel.arc(x, y, raio, 0, 2 * Math.PI);
        pincel.fill();

    }

    function limpaTela() {

        pincel.clearRect(0, 0, 600, 400);

    }

    function desenhaAlvo() {

        desenhaCirculo(x, y, raio+20, 'red');
        desenhaCirculo(x, y, raio+10, 'white');
        desenhaCirculo(x, y, raio, 'red');

    }

    function sorteiaPosicao(maximo) {

        return Math.floor(Math.random() * maximo);

    }

function atualizaTela() {
    limpaTela();
    xAleatorio = sorteiaPosicao(600);
    yAleatorio = sorteiaPosicao(400);
    desenhaAlvo(xAleatorio, yAleatorio);
}

setInterval(atualizaTela, 1000);

function dispara(evento) {

    var x = evento.pageX - tela.offsetLeft;
    var y = evento.pageY - tela.offsetTop;
    alert(xAleatorio);
    alert(yAleatorio);
    /*
    if() {

        alert('Acertou!');

    }
    */

}

tela.onclick = dispara;

</script>
```

Salvaremos e recarregaremos. Ao clicarmos no alvo, recebemos um alerta com a mensagem "574". Este é o valor de X, e se pressionarmos "Ok", temos o valor de Y, que é "227".

Agora que temos acesso às posições aleatórias, podemos fazer testes.

Usaremos o `if` para ver se `x` é maior que `xAleatorio` subtraído do raio, e, utilizando o `&&`, se `x` é menor que `xAleatorio` somado ao raio. Além disso, teremos as mesmas condições, replicadas para o `y`:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var raio = 10;
    var xAleatorio;
    var yAleatorio;

    function desenhaCirculo(x, y, raio, cor) {

        pincel.fillStyle = cor;
        pincel.beginPath();
        pincel.arc(x, y, raio, 0, 2 * Math.PI);
        pincel.fill();

    }

    function limpaTela() {

        pincel.clearRect(0, 0, 600, 400);

    }

    function desenhaAlvo(x,y) {

        desenhaCirculo(x, y, raio+20, 'red');
        desenhaCirculo(x, y, raio+10, 'white');
        desenhaCirculo(x, y, raio, 'red');

    }

    function sorteiaPosicao(maximo) {

        return Math.floor(Math.random() * maximo);

    }

function atualizaTela() {
    limpaTela();
    xAleatorio = sorteiaPosicao(600);
    yAleatorio = sorteiaPosicao(400);
    desenhaAlvo(xAleatorio, yAleatorio);
}

setInterval(atualizaTela, 1000);

function dispara(evento) {

    var x = evento.pageX - tela.offsetLeft;
    var y = evento.pageY - tela.offsetTop;

    if((x > xAleatorio - raio)
    && (x < xAleatorio + raio)
    && (y > yAleatorio - raio)
    && (y < yAleatorio + raio)) {

        alert('Acertou!');

    }


}

tela.onclick = dispara;

</script>
```

Salvaremos e recarregaremos a página. Temos nosso alvo pulando entre pontos aleatórios na página e, ao clicarmos sobre ele, surge uma alerta com a mensagem "Acertou!". Se clicarmos em qualquer outro ponto, nada acontece.

Com isso, concluímos a implementação de nosso primeiro jogo!
