---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/interacao-com-o-canvas/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# interação com o canvas

## criado em: 
-  28-03-2023 - 21:40

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/JS e HTML - LOGICA DE PROGRAMAÇÃO - parte 4\|JS e HTML - LOGICA DE PROGRAMAÇÃO - parte 4]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/nossa primeira obra de arte\|nossa primeira obra de arte]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/agora, um triangulo\|agora, um triangulo]]
- tags: #ANELO 
- Fontes & Links: https://cursos.alura.com.br/course/logica-programacao-pratica-com-desenho-animacoes-em-jogo/task/21885

---

# # Nossa tela está viva, ela responde!

Nesta aula, iniciaremos um novo programa, ao qual demos o título `programa3.html`. É um `<canvas>`, de dimensão `600x400`, no qual utilizamos o `pincel` e preenchemos em cinza:

```xml
<canvas width="600"  height="400"></canvas>

<script>
    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'grey';
    pincel.fillRect(0, 0, 600, 400);
</script>
```

Até então, nós havíamos trabalhado com formas geométricas, como esferas e quadrados, pensando também na organização de nosso código. Nosso objetivo a partir de agora será fazer com que o nosso `<canvas>` interaja com o usuário.

Se você pensa em seguir e construir jogos, temos que ter uma maneira de interagir com o usuário. Ele deve ser capaz de clicar no `<canvas>` e isso dar início a alguma funcionalidade.

De início, faremos com que, ao clicar no `<canvas>`, seja exibido um alerta.

Para começar, criaremos uma função chamada `exibeAlerta()`, que exibirá a mensagem `Cliquei`:

```xml
<canvas width="600"  height="400"></canvas>

<script>
    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'grey';
    pincel.fillRect(0, 0, 600, 400);

    function exibeAlerta() {

       alert('Cliquei');

    }
</script>
```

Salvaremos e recarregaremos a página, porém, nada acontecerá se clicarmos nela. Para que o alerta seja exibido, temos que chamar a função:

```xml
<canvas width="600"  height="400"></canvas>

<script>
    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'grey';
    pincel.fillRect(0, 0, 600, 400);

    function exibeAlerta() {

       alert('Cliquei');
    }

    exibeAlerta();
</script>
```

Se recarregarmos a página agora, o `exibeAlerta` é exibido automaticamente. Não é este o objetivo, queremos que o alerta seja exibido somente quando a página for clicada.

Como vimos, o JavaScript nos permite trabalhar com **eventos**. No caso, utilizaremos a propriedade `onclick`, tudo que atribuirmos a ela - se for uma função - esta será chamada pelo clique. Assim, conectaremos o `exibeAlerta` ao `onClick`:

```xml
<canvas width="600"  height="400"></canvas>

<script>
    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'grey';
    pincel.fillRect(0, 0, 600, 400);

    function exibeAlerta() {

        alert('Cliquei');

    }

    tela.onclick = exibeAlerta;

</script>
```

Lembrando que não podemos utilizar os parênteses neste último caso pois, assim executaríamos a função automaticamente, em vez de guardá-la para ser executada ao clique.

Salvaremos o programa e recarregaremos a página. Ao clicarmos na tela, é exibido um alerta com a mensagem "Cliquei". Funcionou!

Neste caso, quem chama a função `exibeAlerta`? O próprio navegador, ao clicarmos sobre o `<canvas>`. Além de exibirmos um alerta, é importante que nosso programa seja capaz, também, de identificar em qual posição a tela foi clicada.

Como podemos fazer isso?

Ao clicarmos na tela, como dito anteriormente, o próprio navegador é quem chama a função `exibeAlerta`. Toda vez que faz isso, ele passa um parâmetro especial para a função - até então, não havíamos feito isso em nosso código.

Nós criaremos este parâmetro, que chamaremos de `evento`, e utilizaremos o `console.log(evento)` para que ele seja exibido no navegador:

```xml
<canvas width="600"  height="400"></canvas>

<script>
    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'grey';
    pincel.fillRect(0, 0, 600, 400);

    function exibeAlerta(evento) {

        alert('Cliquei');
        console.log(evento);

    }

    tela.onclick = exibeAlerta;

</script>
```

Isso fará com que tenhamos acesso a este parâmetro passado pelo navegador, e assim poderemos descobrir a posição exata do clique.

Após recarregarmos o programa, clicaremos na tela, onde será exibido o alerta. Em seguida, abriremos o console - utilizando o atalho "F12" -, e teremos o `MouseEvent`, com todos os detalhes do evento.

O nome do parâmetro que nós passamos poderia ser qualquer um, o importante é **haver um parâmetro**.

Se expandirmos o `MouseEvent`, clicando na seta antes de seu nome, há diversos detalhes sobre ele, inclusive a posição do mouse dentro do `<canvas>`.

Antes de aprendermos a obter estas informações, vamos recapitular:

-   Criamos uma função chama `exibeAlerta`;
-   Ela recebe como parâmetro um `evento`;
-   Em seu bloco, ela exibe o alerta `'Cliquei`' apenas, e faz um `console.log(evento)`;

Se chamarmos o `exibeAlerta`, temos que passar um parâmetro, mas não temos como saber de antemão qual ponto da tela será clicado. Assim, quem chama essa função é, exclusivamente, o navegador, ele quem tem o parâmetro que trará para nós as coordenadas da posição do cursor no momento do clique.

---

O que fizemos aqui foi definir uma função que será chamada quando um determinado evento ocorrer. Já vimos isso anteriormente, quando pegamos o clique do mouse em um botão do nosso HTML, para dentro do JavaScript! Esse tipo de função é o que chamamos de _callback_. No nosso caso, definimos que, quando alguém clicar na tela (`tela.onclick`), vamos chamar uma função que por sua vez chama o `alert`.

Podemos descobrir a coordenada em que o usuário clicou. Muitas vezes, quando uma função de _callback_ é chamada, são passados argumentos descrevendo o evento que acabou de acontecer. Neste caso é passado um evento chamado `MouseEvent`, com o qual podemos descobrir a posição _x,y_ do clique através de variáveis de dentro desse evento. Altere seu código da seguinte forma:

```javascript
// código anterior omitido 

function exibeAlerta(evento) {
    var x = evento.pageX;
    var y = evento.pageY;
    alert("posição do clique : " + x + ", " + y);
}

// código posterior omitido
```

Repare que agora estamos recebendo como parâmetro uma variável a que demos o nome de `evento`. É comum dar o nome a ela de `mouseEvent` ou até mesmo um simples `e`. Abra o seu HTML e clique em algum lugar da tela, qual é o resultado?

Isso mesmo! Ele te dá a posição do seu clique. Mesmo assim, perceba que há algo estranho. Tente, por exemplo, clicar no canto superior esquerdo da sua imagem. Observe o resultado abaixo:

![](http://s3.amazonaws.com/caelum-online-public/logica-2/clique-canvas.png)

No nosso caso, mesmo clicando bem no canto superior esquerdo do nosso canvas cinza, obtivemos _11, 11_. Algumas vezes, com mais precisão, obtivemos _10,10_. Por que o resultado não foi _0,0_? Isso ocorre pois, como as próprias variáveis _evento.pageX. evento.pageY_ nos dizem, essa é a posição do clique em relação à página! Se quisermos as coordenadas relativas ao canvas, basta subtrairmos a posição em que o canvas (nossa _tela_) foi desenhado na página:

```javascript
// código anterior omitido 

function exibeAlerta(evento) {
    var x = evento.pageX - tela.offsetLeft;
    var y = evento.pageY - tela.offsetTop;
    alert("posição do clique : " + x + ", " + y);
}

// código posterior omitido
```

Ler apenas essa informação não é tão interessante. Que tal desenhar um círculo azul em cada ponto que o usuário clicar? Basta, dentro dessa função, fazer uso aquela função `arc`, que já conhecemos:

```javascript
// código anterior omitido

function exibeAlerta(evento) {
    var x = evento.pageX - tela.offsetLeft;
    var y = evento.pageY - tela.offsetTop;

    pincel.fillStyle="blue";
    pincel.beginPath();
    pincel.arc(x, y, 10, 0, 2*3.14);
    pincel.fill();

    console.log("posição do clique : " + x + ", " + y);
}
// código posterior omitido
```

Recarregue seu arquivo no navegador. Clique em alguns pontos na tela e veja o resultado que obtemos!

Veja que, além de desenhar o círculo onde você clica, estamos colocando a informação das coordenadas no console do navegador. Vimos esse recurso no começo. É muito mais prático utilizá-lo do que imprimir valores com `document.write` ou o inoportuno `alert`. Para ver as posições onde estamos clicando, basta abrir o _Console JavaScript_ do Chrome. Relembrando: clique no ícone de menus/ferramentas, depois acesse o menu _Ferramentas_ (_Tools_) e por último _Console JavaScript_.

Após alguns cliques, você obterá um resultado como o seguinte:

![](http://s3.amazonaws.com/caelum-online-public/logica-2/clique-canvas-log.png)

Já podemos fazer um software parecido com o Paint, não? Ou como o Photoshop, para os mais ousados!

Veja que o nome da função não reflete mais sua funcionalidade. Ela não exibe mais um alerta, pelo contrário, ela agora desenha um círculo. Sendo assim, para que nosso código fique mais fácil de ler, vamos trocar o nome da função para `desenhaCirculo`. Só não podemos esquecer de mudar também na linha que atribui essa função ao evento `tela.onclick`:

```javascript
// código anterior omitido

function desenhaCirculo(evento) {
    var x = evento.pageX - tela.offsetLeft;
    var y = evento.pageY - tela.offsetTop;

    pincel.fillStyle="blue";
    pincel.beginPath();
    pincel.arc(x, y, 10, 0, 2*3.14);
    pincel.fill();

    console.log("posição do clique : " + x + ", " + y);
}

// não esqueça de mudar aqui
tela.onclick = desenhaCirculo;
```

[](https://cursos.alura.com.br/forum/curso-logica-programacao-pratica-com-desenho-animacoes-em-jogo/exercicio-mouse-diga-me-em-que-posicao-estas/21886/novo)