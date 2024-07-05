---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/para-saber-javascript-e-teclas-para-animar/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# para saber - javascript e teclas para animar

## criado em: 
-  29-03-2023 - 12:57

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/JS e HTML - LOGICA DE PROGRAMAÇÃO - parte 4\|JS e HTML - LOGICA DE PROGRAMAÇÃO - parte 4]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/js e html - colirio no olho\|js e html - colirio no olho]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/oito - interaja de maneira diferente com os usuários\|oito - interaja de maneira diferente com os usuários]]
- tags: #ANELO 
- Fontes & Links: 

---

# Para saber mais - Movendo a bolinha pelo teclado

#### versao resumida

Neste treinamento, você aprenderá a mover uma bolinha na tela usando o teclado, dividindo o aprendizado em duas partes. Primeiro, você aprenderá a capturar as setas do teclado e, depois, implementará a lógica para movimentar a bolinha.

O código inicial cria um círculo que é desenhado a cada 20 milissegundos na mesma posição. A ideia é mudar os valores de x e y pelo teclado, fazendo o círculo mudar de posição. Para isso, você usará o evento "onkeydown" do JavaScript para identificar qual tecla foi pressionada.

A função "leDoTeclado" será chamada toda vez que uma tecla for pressionada. Primeiro, declare variáveis para os códigos das setas do teclado e para a taxa de incremento dos eixos. Em seguida, finalize a função "leDoTeclado" com condições que testam qual tecla foi pressionada e atualizam x e y conforme a tecla.

O código final permite mover a bolinha pela tela usando as setas do teclado. Continue praticando para melhorar suas habilidades de programação e lógica!

---

#### versao completa

O foco deste treinamento é na lógica de programação, mais do que trabalhar com o `canvas` em si. A ideia sempre foi fazer com que o aluno aplicasse seu conhecimento para fazer algo um pouco diferente do que calcular IMC ou pontos de vitória de um time. A parte de animação é muito mais complexa do que estamos vendo nesse treinamento, contudo acredito que você ficaria muito feliz se aprendesse a movimentar uma bolinha na tela com o teclado, não?

Vamos então dividir esse aprendizado em duas partes. A primeira eu lhe ensinarei como capturar as _arrow keys_, ou seja, aquelas teclas que são setas, geralmente usadas em joguinhos para andar com algo pela tela. Na segunda parte, vem o desafio de lógica que você deve implementar. Preparado?

Primeiro, vemos o seguinte trecho de código:

```html
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');
    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var x = 20;
    var y = 20;

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

        limpaTela();
        desenhaCirculo(x, y, 10);
    }

    setInterval(atualizaTela, 20);

</script>
```

É um código que não é nenhuma novidade para nós. A cada 20 milissegundos a função `atualizaTela` é chamada e desenha um círculo na tela. Veja que a posição do círculo é sempre a mesma, sendo definida nas variáveis `x` e `y`, ambas com o valor 20. Do jeito que está, a bolinha será desenhada uma vez e nada mais acontecerá, porque a função `atualizaTela` apaga a tela, desenhando a bolinha mais uma vez.

E se fôssemos capazes de mudar o valor de `x` e `y` pelo teclado? Se a cada 20 milissegundos a tela é atualizada e a função `desenhaCirculo` sempre utiliza as variáveis x e y, qualquer mudança nesses valores pelo teclado fará com que o círculo desenhado mude de posição.

## Identificando qual tecla foi pressionada

Em JavaScript, existe o evento `onkeydown`, que permite identificar qual tecla está pressionada. Esse evento é o único capaz de identificar também as setas do teclado. Contudo, até agora todos os eventos que associamos foi com nossa `tela`, mas dessa vez quem deve responder ao evento é `document`. E `document`, nosso oráculo que sabe tudo o que a página possui, é o cara que fica escutando ao teclado. Então, vou alterar o código e criar a função `leDoTeclado` e associá-la ao `document` através do evento `onkeydown`:

```html
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');
    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var x = 20;
    var y = 20;

    // códigos do teclado

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

        limpaTela();
        desenhaCirculo(x, y, 10);
    }

    setInterval(atualizaTela, 20);

    function leDoTeclado(evento) {

        // como saber qual tecla foi pressionada?
    }

   document.onkeydown = leDoTeclado;

</script>
```

A função `leDoTeclado` será chamada toda vez que uma tecla for pressionada. Mas para podermos identificar as setas do teclado, precisamos saber qual é seu código correspondente. Isso porque na função `leDoTeclado` podemos acessar `evento.keyCode`. O `evento.keyCode` traz o código da tecla que foi pressionada. Vamos declarar quatro variáveis que guardam os códigos que correspondem às nossas setinhas:

**Obs:** Cada tecla possui um KeyCode (código de tecla) respectivo e isso foi catalogado em uma tabela. Essa tabela deve ser usada pelos navegadores web para que usem os mesmos valores.

```html
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');
    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var x = 20;
    var y = 20;

    // códigos do teclado

    var esquerda = 37;
    var cima = 38;
    var direita = 39;
    var baixo = 40;

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

        limpaTela();
        desenhaCirculo(x, y, 10);
    }

    setInterval(atualizaTela, 20);

    function leDoTeclado(evento) {

        // sabemos que é através de evento.keyCode que temos acesso ao código da tecla pressionada
    }

   document.onkeydown = leDoTeclado;

</script>
```

Estamos quase lá. Outra coisa importante é que a taxa de atualização de `x` e `y` seja 10, isto é, toda vez que teclarmos com a seta esquerda, por exemplo, precisamos subtrair -10 do valor de `x` atual. Se teclarmos a seta direita, precisamos incrementar +10 com o `x` atual. A mesma lógica se aplica ao eixo `y`.

Então, vamos declarar a variável chamada `taxa`, que guarda o valor do incremento dos eixos:

```html
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');
    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var x = 20;
    var y = 20;

    // códigos do teclado

    var esquerda = 37;
    var cima = 38;
    var direita = 39;
    var baixo = 40;

    // taxa de incremento
    var taxa = 10;

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

        limpaTela();
        desenhaCirculo(x, y, 10);
    }

    setInterval(atualizaTela, 20);

    function leDoTeclado(evento) {

        // sua lógica virá aqui
    }

   document.onkeydown = leDoTeclado;

</script>
```

Agora precisamos finalizar a função `leDoTeclado`, que deve testar cada tecla pressionada e atualizar `x` e `y` de acordo com a tecla.

O código para essa funcionalidade é uma sucessão de `if`'s que identifica qual tecla foi pressionada, incrementando ora `x`, ora `y`, positivamente ou negativamente. Nessa implementação podemos andar com a bolinha até que suma da tela:

```html
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');
    pincel.fillStyle = 'lightgray';
    pincel.fillRect(0, 0, 600, 400);

    var x = 20;
    var y = 20;

    // códigos do teclado

    var esquerda = 37
    var cima = 38
    var direita = 39
    var baixo = 40

    var taxa = 10;

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

        limpaTela();
        desenhaCirculo(x, y, 10);
    }

    setInterval(atualizaTela, 20);

    function leDoTeclado(evento) {

        if(evento.keyCode == cima) {

            y = y - taxa;

        } else if (evento.keyCode == baixo) {

            y = y + taxa;

        } else if (evento.keyCode == esquerda) {

            x = x - taxa;

        } else if (evento.keyCode == direita) {

            x = x + taxa;
        }
    }

   document.onkeydown = leDoTeclado;

</script>
```

Muito interessante exercitar a lógica! Continue com os estudos!