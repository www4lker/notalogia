---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/nossa-primeira-obra-de-arte/","tags":["javascript","HTML","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# nossa primeira obra de arte

## criado em: 
-  28-03-2023 - 13:51

### Conteúdo Relacionado
- notas: [[ agora, um triangulo\| agora, um triangulo]]
- tags: #javascript #HTML #ANELO 
- Fontes & Links:  https://cursos.alura.com.br/course/logica-programacao-pratica-com-desenho-animacoes-em-jogo/task/21879

---
Nesta aula, daremos continuidade ao projeto da aula anterior, onde fizemos nosso primeiro desenho.

Nossa visualização será, no lado esquerdo, do `<canvas>` em sua totalidade, e, no lado direito, veremos nosso código.

Criaremos um novo retângulo, que terá `200` de largura e `400` de altura, na cor verde. Primeiro, selecionaremos a nova cor, utilizando o `fillStyle`:

```
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgrey';
    pincel.fillRect(0, 0, 600, 400);

    pincel.fillStyle = 'green';
</script>
```

Em seguida, pediremos ao `pincel` que se movimente em nossa tela, por meio do `fillRect` na posição `(0, 0, 200, 400)`:

```
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.fillStyle = 'lightgrey';
    pincel.fillRect(0, 0, 600, 400);

    pincel.fillStyle = 'green';
    pincel.fillRect(0, 0, 200, 400);
</script>
```

Salvaremos e recarregaremos a página. Temos em nossa tela a exibição de um retângulo menor, ao lado esquerdo, na cor verde, e o resto do `<canvas>` preenchido em cinza, algo análogo à representação abaixo:

![navegador web com representação da tag canvas, onde parte dele está na cor verde, especificamente o retangulo esquerdo, enquanto o restante permanece em cinza](https://s3.amazonaws.com/caelum-online-public/logica-2/01.04_001_navegador-web-com.png)

O próximo passo será criar um novo retângulo, de mesmo tamanho, no lado direito, na cor vermelha. Para isso, criaremos um novo `pincel.fillStyle` e um novo `pincel.fillRect`.

Como queremos que ele comece em determinado ponto do retângulo, ou seja, do eixo x, precisamos representar isso no `fillRect`. Já que este lado mede `600`, e teremos três formas, cada uma delas terá `200` de largura, sendo assim, a terceira forma iniciará a partir do ponto `400`:

```
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
</script>
```

Salvaremos e recarregaremos, teremos na tela um retângulo verde, como na imagem anterior, mas agora temos também um retângulo cinza ao seu lado direito, de mesmo tamanho e, a sua direita, um retângulo vermelho com as mesmas dimensões.

Comentaremos o bloco que contém as informações com a cor cinza do `<canvas>`, em JavaScript isso pode ser feito utilizando o comando `/*` indicando o ponto inicial do comentário, seguido do `*/` para finalizá-lo:

```
<canvas width="600" height="400"></canvas>

<script>

    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    /*
    pincel.fillStyle = 'lightgrey';
    pincel.fillRect(0, 0, 600, 400);
    */
    pincel.fillStyle = 'green';
    pincel.fillRect(0, 0, 200, 400);

    pincel.fillStyle = 'red';
    pincel.fillRect(400, 0, 200, 400);
</script>
```

Salvaremos e recarregaremos a página. Como podemos observar, não há mais a área cinza do `<canvas>`. Temos portanto a bandeira da Itália. Retornaremos com o código, para termos tudo funcionando:

```
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
</script>
```

Salvaremos e recarregaremos.

Nosso próximo objetivo será desenhar um triângulo no centro do retângulo cinza, é o que veremos adiante
