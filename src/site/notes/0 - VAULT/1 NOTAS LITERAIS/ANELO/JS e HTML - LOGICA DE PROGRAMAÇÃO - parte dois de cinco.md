---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/js-e-html-logica-de-programacao-parte-dois-de-cinco/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# JS e HTML - LOGICA DE PROGRAMAÇÃO - parte dois de cinco

## criado em: 
-  28-03-2023 - 17:19

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/proficiencia em vs code\|proficiencia em vs code]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/interação com o canvas\|interação com o canvas]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/JS e HTML - LOGICA DE PROGRAMAÇÃO - parte 4\|JS e HTML - LOGICA DE PROGRAMAÇÃO - parte 4]]
- tags: #ANELO 
- Fontes & Links:  https://cursos.alura.com.br/course/logica-programacao-pratica-com-desenho-animacoes-em-jogo/task/21882

---

Dando continuidade ao nosso trabalho com formas, criaremos um novo programa. Podemos salvá-lo como `programa2.html`.

Primeiramente, ele terá nossas tags `<script>` e `<canvas>`:

```xml
<canvas width="600" height="400"></canvas>

<script>

</script>
```

Como sabemos, temos que transportar o `<canvas>` para o JavaScript, e faremos isso por meio do `document.querySelector()`:

```xml
<canvas width="600" height="400"></canvas>

<script>

var tela = document.querySelector('canvas');

</script>
```

Importante ressaltar que estamos utilizando as "aspas simples" (apóstrofo) para escrevermos menos, e que isso **só pode acontecer no mundo JavaScript**, que aceita tanto as aspas simples quanto as duplas (`"`).

Para podermos escrever na tela, precisaremos da variável `pincel`, que receberá um `getContext` para nos fornecer um pincel 2D:

```xml
<canvas width="600" height="400"></canvas>

<script>

var tela = document.querySelector('canvas');
var pincel = tela.getContext('2d');

</script>
```

Nosso próximo objetivo será imprimir um quadrado pequeno.

O primeiro passo é determinar a cor, com o `fillStyle`, que será verde:

```xml
<canvas width="600" height="400"></canvas>

<script>

var tela = document.querySelector('canvas');
var pincel = tela.getContext('2d');

pincel.fillStyle = 'green';
</script>
```

O segundo passo será indicar **o que** será preenchido em verde, ou seja, nosso quadrado. Para isso, utilizaremos o`fillRect` e passaremos as coordenadas da forma como **parâmetros**:

```xml
<canvas width="600" height="400"></canvas>

<script>

var tela = document.querySelector('canvas');
var pincel = tela.getContext('2d');

pincel.fillStyle = 'green';
pincel.fillRect(0, 0, 50, 50);

</script>
```

Salvaremos nosso programa. Abriremos o navegador e selecionaremos nosso arquivo, a partir do menu "Arquivo > Abrir arquivo...". Ao fazermos isso, temos a imagem do nosso quadrado.

E se quisermos colocar um outro quadrado ao lado deste que já existe? Podemos utilizar a mesma fórmula, mas precisamos ter cuidado com seu posicionamento no eixo X, para que não coincida com o que já temos.

Se nosso quadrado tem `50` de largura, isso significa que ele ocupa 50 pixels no eixo X, assim, nosso novo quadrado deve começar a partir do ponto 50 no eixo X:

```xml
<canvas width="600" height="400"></canvas>

<script>

var tela = document.querySelector('canvas');
var pincel = tela.getContext('2d');

pincel.fillStyle = 'green';
pincel.fillRect(0, 0, 50, 50);

pincel.fillRect(50, 0, 50, 50);

</script>
```

Criaremos, ainda, um terceiro, que iniciará no ponto 100 do eixo X:

```xml
<canvas width="600" height="400"></canvas>

<script>

var tela = document.querySelector('canvas');
var pincel = tela.getContext('2d');

pincel.fillStyle = 'green';
pincel.fillRect(0, 0, 50, 50);

pincel.fillRect(50, 0, 50, 50);
pincel.fillRect(100, 0, 50, 50);

</script>
```

Salvaremos e recarregaremos a página, e o que temos são os três quadrados, verdes, um ao lado do outros. Entretanto, para quem vê, parece ser um único retângulo posicionado horizontalmente. Colocaremos as bordas, para separar cada um dos quadrados.

Após fazermos o `fillRect`, podemos indicar ao `pincel` o tipo de `strokeStyle`, qual será a cor da borda, que no caso definiremos como preta:

```xml
<canvas width="600" height="400"></canvas>

<script>

var tela = document.querySelector('canvas');
var pincel = tela.getContext('2d');

pincel.fillStyle = 'green';
pincel.fillRect(0, 0, 50, 50);
pincel.strokeStyle = 'black';

pincel.fillRect(50, 0, 50, 50);
pincel.fillRect(100, 0, 50, 50);

</script>
```

Em seguida, indicaremos ao `pincel` que ele deve desenhar a borda, utilizando o `strokeRect()`. A borda deve ser inserida na mesma posição do quadrado:

```xml
<canvas width="600" height="400"></canvas>

<script>

var tela = document.querySelector('canvas');
var pincel = tela.getContext('2d');

pincel.fillStyle = 'green';
pincel.fillRect(0, 0, 50, 50);
pincel.strokeStyle = 'black';
pincel.strokeRect(0, 0, 50, 50);

pincel.fillRect(50, 0, 50, 50);
pincel.fillRect(100, 0, 50, 50);

</script>
```

Salvaremos o programa e recarregaremos a página. O primeiro quadrado agora tem borda, enquanto os outros dois permanecem sem divisões ou delimitações. Repetiremos o `strokeRect` para os demais quadrados, lembrando que devemos replicar as respectivas posições:

```xml
<canvas width="600" height="400"></canvas>

<script>

var tela = document.querySelector('canvas');
var pincel = tela.getContext('2d');

pincel.fillStyle = 'green';
pincel.fillRect(0, 0, 50, 50);
pincel.strokeStyle = 'black';
pincel.strokeRect(0, 0, 50, 50);

pincel.fillRect(50, 0, 50, 50);
pincel.strokeRect(50, 0, 50, 50);

pincel.fillRect(100, 0, 50, 50);
pincel.strokeRect(100, 0, 50, 50);
</script>
```

Salvaremos e recarregaremos o programa. Temos a imagem de três quadrados verdes, com bordas pretas, um ao lado do outro.

Vamos imaginar que nossa intenção fosse criar apenas um quadrado, nosso código ficaria então da seguinte forma:

```xml
<canvas width="600" height="400"></canvas>

<script>

var tela = document.querySelector('canvas');
var pincel = tela.getContext('2d');

pincel.fillStyle = 'green';
pincel.fillRect(0, 0, 50, 50);
pincel.strokeStyle = 'black';
pincel.strokeRect(0, 0, 50, 50);

</script>
```

É bastante código para desenhar apenas uma forma simples. Um iniciante em programação nem seria capaz de identificar, com facilidade, a finalidade deste código.

Idealmente, seria interessante se pudéssemos, com apenas uma linha de código, atingir esta mesma funcionalidade, por exemplo:

```xml
<script>
//outras propriedades...

desenhaQuadradoVerde();
</script>
```

Qualquer um que analisasse nosso código, saberia identificar o que esta linha faz - ela **desenha um quadrado verde**. Como aprendemos no módulo anterior, é possível fazermos isso por meio do uso de **funções**.

A **função** é um código que foi guardado para ser chamado posteriormente. Criaremos portanto a função `desenhaQuadradoVerde()`:

```xml
<canvas width="600" height="400"></canvas>

<script>

function desenhaQuadradoVerde() {

}

var tela = document.querySelector('canvas');
var pincel = tela.getContext('2d');

pincel.fillStyle = 'green';
pincel.fillRect(0, 0, 50, 50);
pincel.strokeStyle = 'black';
pincel.strokeRect(0, 0, 50, 50);

desenhaQuadradoVerde();

</script>
```

O conteúdo da nossa função será todo o bloco que cria nosso quadrado:

```xml
<canvas width="600" height="400"></canvas>

<script>

    function desenhaQuadradoVerde() {

        var tela = document.querySelector('canvas');
        var pincel = tela.getContext('2d');

        pincel.fillStyle = 'green';
        pincel.fillRect(0, 0, 50, 50);
        pincel.strokeStyle = 'black';
        pincel.strokeRect(0, 0, 50, 50);

}

desenhaQuadradoVerde();

</script>
```

Como já havíamos pré-definido, chamamos a função, sem esquecer dos parênteses (`()`).

Salvaremos e recarregaremos o programa. Ele continua funcionando, ainda temos nosso quadrado verde com borda preta. Entretanto, se agora quisermos criar um novo quadrado basta chamarmos a função novamente, e assim por diante, para quantos quadrados quisermos criar.

Por exemplo, para criarmos três quadrados chamaremos a função três vezes:

```xml
<canvas width="600" height="400"></canvas>

<script>

    function desenhaQuadradoVerde() {

        var tela = document.querySelector('canvas');
        var pincel = tela.getContext('2d');

        pincel.fillStyle = 'green';
        pincel.fillRect(0, 0, 50, 50);
        pincel.strokeStyle = 'black';
        pincel.strokeRect(0, 0, 50, 50);

}

desenhaQuadradoVerde();
desenhaQuadradoVerde();
desenhaQuadradoVerde();

</script>
```

Salvaremos e recarregaremos o programa. Entretanto, continuamos vendo apenas um quadrado! Por que isso aconteceu?

Isso ocorre porque todas as vezes que chamamos a mesma função, teremos os mesmos parâmetros, assim, os quadrados serão criados exatamente no mesmo lugar! Não é essa a intenção, queremos desenhar os quadrados lado a lado. É o que veremos adiante.