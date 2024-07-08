---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/js-e-html-logica-de-programacao-parte-4/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# JS e HTML - LOGICA DE PROGRAMAÇÃO - parte 4

## criado em: 
-  29-03-2023 - 10:57

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/para saber - javascript e teclas para animar\|para saber - javascript e teclas para animar]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/js e html - colirio no olho\|js e html - colirio no olho]]
- tags: #ANELO 
- Fontes & Links: https://cursos.alura.com.br/course/logica-programacao-pratica-com-desenho-animacoes-em-jogo/task/21887

---

## Movendo elementos: animações simples

Nesta aula, daremos início ao `programa4.html`. Nele, temos um código na linha dos que já utilizamos em aulas anteriores:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');
    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

</script>
```

Aplicaremos nossos conhecimentos de lógica de programação para animarmos uma esfera na tela, e termos ferramentas para conseguirmos criar um jogo simples.

A primeira coisa a fazer é criar uma esfera na tela.

Inverteremos um pouco a ordem, e chamaremos primeiro a função, para analisarmos o que ela precisará receber como parâmetro:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');
    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    desenhaCirculo();
</script>
```

Passaremos as coordenadas X e Y, e o tamanho do raio, que será `10`:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');
    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    desenhaCirculo(20, 20, 10);

</script>
```

Como ainda não definimos a função, ela não poderá ser executada. Começaremos a construção dela passando os parâmetros, que serão `x, y, raio` - de acordo com o tipo de valor que cada um receberá -, em seu bloco, incluiremos `fillStyle` na cor azul, o `beginPath`, e o `arc`, que receberá o ponto onde queremos plotar a esfera no `<canvas>`:

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
        pincel.arc(x, y, raio, 0, 2 * 3.14);
    }

    desenhaCirculo(20, 20, 10);

</script>
```

Como sabemos, na matemática, o valor de Pi é equivalente a `3.14`. Como sabemos, no JS temos algumas funções que iniciam com `Math.` e nos dão funcionalidades básicas, justamente, temos o `Math.PI`, que é o que utilizaremos em nosso código:

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

    }

    desenhaCirculo(20, 20, 10);

</script>
```

Para preenchermos o círculo, utilizaremos o `pincel.fill`:

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

    desenhaCirculo(20, 20, 10);

</script>
```

Salvaremos e recarregaremos o programa, temos um círculo azul no canto superior esquerdo da tela. Para desenharmos outra esfera, basta repetirmos o chamado à função, com novos parâmetros, que sejam diferentes dos primeiros.

---

Para chegarmos a este resultado, faremos com que a esfera saía de um ponto nas coordenadas iniciais, e chegue em um novo, que definiremos com novas coordenadas. Para movimentarmos nossa esfera horizontalmente, manipularemos o valor da coordenada X.

Como vimos, há o método `for` para fazermos este tipo de alteração reiterada de uma única propriedade. Criaremos nele uma variável `x`, que receberá `20`, uma condição `x < 600`, e incremento de `x = x + 1`, que, como sabemos, pode ser feito com o `x++`:

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

        for(var x = 20; x < 600; x++) {

        }

    desenhaCirculo(20, 20, 10);

</script>
```

Colocaremos a função `desenhaCirculo()` dentro do `for()`, substituiremos o parâmetro `20` pelo `x` e manteremos os demais, pois queremos que a esfera se mova somente no eixo X:

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

        for(var x = 20; x < 600; x++) {
            desenhaCirculo(x, 20, 10);
        }
</script>
```

Salvaremos e recarregaremos o programa. Em vez da animação temos a imagem de uma linha em azul. Isso aconteceu porque demos o espaçamento de apenas `1` pixel entre as esferas, assim, quase todas ficaram umas sobre as outras, dando a ilusão de formarem uma única linha.

Para resolvermos isso, utilizaremos o `pincel.clearRect()`, o que indicará ao JS que ele deve limpar o retângulo:

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

             for(var x = 20; x < 600; x++) {
            pincel.clearRect(0, 0, 600, 400);
            desenhaCirculo(x, 20, 10);

        }

</script>
```

Após salvarmos e recarregarmos, veremos que o fundo de `<canvas>` ficou completamente branco, e visualizamos apenas uma esfera, no canto superior direito.

Por que ela ainda não está animada? Isso ocorre porque a nossa CPU faz este processo muito rapidamente, antes que possamos visualizar o processo, conseguimos ver apenas o resultado final.

A ideia é podermos esperar alguns segundos entre o surgimento das esferas.

Além disso, para esclarecer a função do `clearRect`, criaremos a função `limpaTela`, que receberá nossa função. Assim, chamaremos o `limpaTela()` já dentro do nosso `for()`:

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

        for(var x = 20; x < 600; x++) {
            limpaTela();
            desenhaCirculo(x, 20, 10);

        }
</script>
```

Assim as funcionalidades ficam mais evidentes para quem lê nosso código. Vimos que o `for` é uma solução ruim, porque fará com que o processo de animação ocorra rápido demais para que sejamos capazes de perceber.

---

Removeremos o `for`:

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

Primeiro, trabalharemos com o conceito de como podemos chamar um código com intervalos de tempo.

Em seguida, criaremos a função `exibeMensagemNoConsole()` que terá um `console.log()` com a mensagem "Chamei função", e chamaremos em seguida:

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

    function exibeMensagemNoConsole() {

        console.log('Chamei função');

    }

    exibeMensagemNoConsole();

</script>
```

Salvaremos a página e recarregaremos. Em seguida, abriremos o console e leremos:

```kotlin
Chamei função
```

Faremos com que esta mensagem seja exibida com intervalos de tempo. Para isso, utilizaremos a função `setInterval`. Ela aceita receber, como parâmetro, a função que você deseja chamar e, depois, a quantidade de tempo que desejamos dar de intervalo em milissegundos. Utilizaremos `1000` milissegundos, que equivalem a 1 segundo:

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

    function exibeMensagemNoConsole() {
    console.log('Chamei função');
    }

    setInterval(exibeMensagemNoConsole, 1000);

</script>
```

Após recarregarmos a página, observe que o console exibe a mensagem, assim como anteriormente, e que surge um contador ao lado esquerdo da frase "Chamei função". Este contador se refere ao número de vezes em que ele está realizando a impressão, o JavaScript faz uso de um recurso mais elegante, em vez de gerar isto visualmente.

Escolhemos o tempo de `1` segundo mas poderíamos ter delimitado qualquer outro intervalo, isso dependerá do projeto e exigências específicas.

Entretanto, nosso objetivo não é imprimir a mensagem, e sim realizar a função `atualizaTela`, que criaremos agora:

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

    function atualizaTela() {
    }
</script>
```

Sua funcionalidade será atualizar a tela em determinados intervalos de tempo. Ela chamará a função `desenhaCirculo()`, que terá como parâmetros as posições X, Y, e o raio da circunferência:

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

    function atualizaTela() {
        desenhaCirculo(20, 20, 10);
    }

    setInterval(atualizaTela, 20);

</script>
```

Lembre-se de salvar a página. Após recarregá-la, temos a exibição da esfera azul no canto superior esquerdo da tela. Ela não está animada, isso significa que não deu certo?

A nossa função está correta, entretanto, como passamos o mesmo valor de `x`, estão sendo desenhadas várias esferas sobrepostas. Para consertar isso, a cada chamada de tela, precisamos passar um novo valor de `x`, ou seja, incrementar `x` (lembrando de declarar a variável `x` com valor `20` antes):

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

    var x = 20;

    function atualizaTela() {

    desenhaCirculo(x, 20, 10);
    x++;

    }

    setInterval(atualizaTela, 20);

</script>
```

Para que não tenhamos o problema de esferas sobrepostas, precisamos inserir, antes de `desenhaCirculo()`, o `limpaTela()`:

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

    var x = 20;

    function atualizaTela() {

    limpaTela();
    desenhaCirculo(x, 20, 10);
    x++;
    }

    setInterval(atualizaTela, 20);

</script>
```

Salvaremos e recarregaremos a tela. Funcionou! Temos nossa esfera viajando do canto superior esquerdo da tela, até o canto superior direito. Para que a animação fique mais rápida, basta alterar o segundo parâmetro de `setInterval`, deixaremos como `10`:

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

    var x = 20;

    function atualizaTela() {

    limpaTela();
    desenhaCirculo(x, 20, 10);
    x++;
    }

    setInterval(atualizaTela, 10);

</script>
```

Recapitulando:

-   O método `setInterval()` chama `atualizaTela()`;
-   Este, quando executado, faz o `limpaTela()`, `desenhaCirculo()` e incrementa o valor de `x`;
-   O `setInterval()` aguarda `20` milisegundos, para repetir o processo, sempre incrementando o valor de `x`, o que faz com que nossa esfera "se mova" para a direita.

Esta lógica é fundamental quando pensamos em animações, ou mesmo em criar jogos. Vamos para os exercícios!