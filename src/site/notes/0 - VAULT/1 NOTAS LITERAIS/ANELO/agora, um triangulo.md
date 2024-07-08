---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/agora-um-triangulo/","tags":["javascript","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# agora, um triangulo

## criado em: 
-  28-03-2023 - 15:59

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/nossa primeira obra de arte\|nossa primeira obra de arte]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/JS e HTML - LOGICA DE PROGRAMAÇÃO - parte dois de cinco\|JS e HTML - LOGICA DE PROGRAMAÇÃO - parte dois de cinco]]
- tags: #javascript #ANELO
- Fontes & Links: 

---

Para a criação desta forma geométrica, não utilizaremos o `fillRect`, em vez disso, queremos começar um caminho. O que é isso?

Começar, em inglês, é _begin_, e caminho é _path_. Portanto, utilizaremos um _begin path_ para dizermos qual será a direção seguida por nosso pincel. O primeiro passo é utilizar o `fillStyle`, com a cor amarela:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgrey';
    pincel.fillRect(0, 0, 600, 400);

    pincel.fillStyle = 'green';
    pincel.fillRect(0, 0, 200, 400);

    pincel.fillStyle = 'red';
    pincel.fillRect(400, 0, 200, 400);

    pincel.fillStyle = 'yellow';

</script>
```

Com isso, indicaremos que nosso pincel iniciará seu caminho com o `pincel.beginPath()`:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgrey';
    pincel.fillRect(0, 0, 600, 400);

    pincel.fillStyle = 'green';
    pincel.fillRect(0, 0, 200, 400);

    pincel.fillStyle = 'red';
    pincel.fillRect(400, 0, 200, 400);

    pincel.fillStyle = 'yellow';
    pincel.beginPath();

</script>
```

Para começarmos a escrever, indicaremos onde está o ponto inicial do nosso triângulo. Nossa primeira coordenada será centralizada na tela, para fazermos isso, utilizaremos a função `moveTo`:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgrey';
    pincel.fillRect(0, 0, 600, 400);

    pincel.fillStyle = 'green';
    pincel.fillRect(0, 0, 200, 400);

    pincel.fillStyle = 'red';
    pincel.fillRect(400, 0, 200, 400);

    pincel.fillStyle = 'yellow';
    pincel.beginPath();
    pincel.moveTo();

</script>
```

Pensando em nossas coordenadas, temos que posicionar nosso pincel exatamente no ponto 300, da coordenada X (que mede 600), e 200 na Y (que mede 400):

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgrey';
    pincel.fillRect(0, 0, 600, 400);

    pincel.fillStyle = 'green';
    pincel.fillRect(0, 0, 200, 400);

    pincel.fillStyle = 'red';
    pincel.fillRect(400, 0, 200, 400);

    pincel.fillStyle = 'yellow';
    pincel.beginPath();
    pincel.moveTo(300, 200);

</script>
```

Em seguida, moveremos o pincel para uma nova posição, com a função `lineTo()`. Esta posição será o ponto de encontro entre o verde e o cinza, e a linha inferior de nosso `<canvas>`, portanto, `200` no eixo X, e `400` no eixo Y:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgrey';
    pincel.fillRect(0, 0, 600, 400);

    pincel.fillStyle = 'green';
    pincel.fillRect(0, 0, 200, 400);

    pincel.fillStyle = 'red';
    pincel.fillRect(400, 0, 200, 400);

    pincel.fillStyle = 'yellow';
    pincel.beginPath();
    pincel.moveTo(300, 200);
    pincel.lineTo(200, 400);

</script>
```

O próximo movimento criará uma linha horizontal, do ponto que acabamos de criar até o ponto em que o cinza encontra o vermelho, de coordenadas 400 (X), e 400 (Y):

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgrey';
    pincel.fillRect(0, 0, 600, 400);

    pincel.fillStyle = 'green';
    pincel.fillRect(0, 0, 200, 400);

    pincel.fillStyle = 'red';
    pincel.fillRect(400, 0, 200, 400);

    pincel.fillStyle = 'yellow';
    pincel.beginPath();
    pincel.moveTo(300, 200);
    pincel.lineTo(200, 400);
    pincel.lineTo(400, 400);

</script>
```

Por fim, basta inserirmos um comando para que o programa preencha esta forma, que é o `pincel.fill()`:

```xml
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgrey';
    pincel.fillRect(0, 0, 600, 400);

    pincel.fillStyle = 'green';
    pincel.fillRect(0, 0, 200, 400);

    pincel.fillStyle = 'red';
    pincel.fillRect(400, 0, 200, 400);

    pincel.fillStyle = 'yellow';
    pincel.beginPath();
    pincel.moveTo(300, 200);
    pincel.lineTo(200, 400);
    pincel.lineTo(400, 400);
    pincel.fill();

</script>
```

Salvaremos e recarregaremos a página. Temos nossa imagem, assim como antes, só que agora há um triângulo de cor cinza (apenas para ilustrar), com sua base no final do `<canvas>` e pico centralizado em relação a forma como um todo:

![retângulos verde, cinza e vermelho ao fundo, com um triângulo amarelo inserido no retângulo cinza](http://s3.amazonaws.com/caelum-online-public/logica-2/triangulo2.png)

Como vimos, a construção do triângulo foi trabalhada a partir de um caminho, criamos o primeiro ponto, ou vértice, e em seguida os demais. Por último, fazemos com que o programa preencha esta forma com a cor que já escolhemos.

Nosso próximo desafio será criar uma esfera.