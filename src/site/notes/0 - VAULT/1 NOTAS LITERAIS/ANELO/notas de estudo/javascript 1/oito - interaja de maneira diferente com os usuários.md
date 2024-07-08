---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/oito-interaja-de-maneira-diferente-com-os-usuarios/","tags":["javascript"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# 08 - interaja de maneira diferente com os usuários

## criado em: 
-  23-03-2023 - 16:12

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/input focus\|input focus]]
- tags: #javascript 
- Fontes & Links: 

---
## Campo de texto e botão

Nesta aula aprenderemos a capturar e executar os códigos de nossos programas de uma maneira diferente e elegante. No editor de texto, criaremos um arquivo utilizando o atalho "Ctrl + N", e o salvaremos com o nome `adivinha_mais.html`. Ele será um jogo de adivinhação diferente daquele que criamos anteriormente.

Em primeiro lugar, colocaremos no código o `meta charset="UTF-8"`:

```xml
<meta charset="UTF-8">

<script>

</script>
```

Retornaremos ao navegador e abriremos nosso programa. Nosso objetivo é exibir, no canto superior esquerdo da tela, um campo de entrada para o usuário, acompanhado de um botão. Criaremos isto em HTML, quando utilizamos o `<input/>`, fazendo com que seja aberto um campo para entrada de texto no navegador.

```xml
<meta charset="UTF-8">

<input/>

<script>

</script>
```

Ao salvarmos o programa e recarregarmos a página, veremos o seguinte:

![campo de texto no navegador em branco](https://s3.amazonaws.com/caelum-online-public/440+-+L%C3%B3gica+de+Programa%C3%A7%C3%A3o/08.01_001_campo-de-texto.png)

A palavra "_input_" vem do inglês, e sua tradução é "entrada". Em seguida, criaremos um botão, e a palavra em inglês para isso é "_button_", assim, vamos usá-la em nosso código:

```xml
<meta charset="UTF-8">

<input/>
<button></button>

<script>

</script>
```

Esta _tag_, como podemos observar, abre e fecha, diferentemente da `<input>`. Dentro da _tag_ `<button>` inseriremos a frase "Compare com o meu segredo":

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

</script>
```

Salvaremos e recarregaremos a página. Teremos na tela, no canto superior esquerdo, o campo para inserir texto e, em seu lado direito, o botão com o texto conforme configuramos. Nosso objetivo é que o usuário digite um número e, ao apertar o botão, que ele seja comparado ao `numeroPensado` para que se verifique se ele acertou ou errou. Para este novo programa, chamaremos o `numeroPensado` de `segredo`.

Neste capítulo, aprenderemos o mínimo possível para que possamos interagir com o usuário por meio da caixa de texto, e do botão. O `<input>` e o `<button>` estão inseridos em qual mundo? HTML ou JavaScript? Eles estão no mundo **HTML**, pois estão fora da tag `<script>`. Se as inserirmos na tag `<script>` o JavaScript nem seria capaz de compreender isso.

Precisaremos descobrir uma maneira de acessar estas tags do mundo HTML a partir do mundo JavaScript. Para isso, criaremos uma variável `input`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var input

</script>
```

Ela receberá a função `document.querySelector()` - atenção para o "S" maiúsculo. Utilizaremos a `querySelector()` para inserir aquilo que está no mundo HTML na variável `input`. Ela receberá como parâmetro o nome da _tag_ que desejamos utilizar:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var input = document.querySelector("input");

</script>
```

Isso permite trabalharmos com o `<input>` no universo JavaScript. O nome da variável não importa, podemos escolher qualquer um, apenas precisamos nos atentar ao nome da tag, que deve ser passado exatamente como é para o `querySelector()` poder acessá-lo. No caso, chamaremos a variável de `input` apenas por motivos didáticos.

Para sabermos qual o valor que está inserido na variável, utilizaremos o `input.value`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var input = document.querySelector("input");
    input.value

</script>
```

Podemos criar um `alert()` para imprimi-lo, mas queremos comparar se o valor do `input` é igual ao segredo. Por isso, teremos uma variável `segredo` que receberá o valor `5`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    var segredo = 5;

    var input = document.querySelector("input");
    input.value

</script>
```

Para testar se o que o usuário digitou é igual ao segredo, utilizaremos o `if()`, se este for o caso, será exibido um `alert()` com a mensagem "Você ACERTOU!", caso contrário, utilizaremos o `else` para que seja exibido `Você ERROU!!!!!!!!`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    var segredo = 5;

    var input = document.querySelector("input");

    if(input.value == segredo) {

        alert("Você ACERTOU!");
    } else {

        alert("Você ERROU!!!!!!!!");
    }

</script>
```

> Recapitulando:
> 
> -   No HTML temos um campo de _input_, utilizado para receber textos;
>     
> -   Há também um botão;
>     
> -   Nosso objetivo é, ao carregarmos a página, digitarmos um número em nosso campo, clicarmos no botão, e somente então, que o programa compare o número inserido ao segredo.
>     

Salvaremos o programa e recarregaremos a página. Surgirá um pop up com a mensagem de que erramos antes mesmo de termos clicado no botão para verificar o número. Isso acontece porque o programa está fazendo o teste com um valor vazio. Podemos confirmar que não há valor criando um `alert()` para o `input.value`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    var segredo = 5;

    var input = document.querySelector("input");
    alert(input.value);
    if(input.value == segredo) {

        alert("Você ACERTOU!");
    } else {

        alert("Você ERROU!!!!!!!!");
    }

</script>
```

Se salvarmos e recarregarmos a página, veremos que o valor de `input` não existe, pois surgirá apenas um alerta, sem nenhuma mensagem. Feito isso, poderemos remover este `alert()` de nosso código.

O problema é que precisamos sinalizar ao programa que o teste entre os números só pode ser feito a partir do momento em que o usuário clicar no botão, e não ao carregar a página. Como sabemos, é possível "guardar" um código para chamá-lo posteriormente, por meio de **funções**.

A primeira coisa a fazer é garantir que o teste **não seja executado** ao carregar a página. Criaremos uma _function_ para a verificação:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    var segredo = 5;

    var input = document.querySelector("input");

    function verifica() {

    }

    if(input.value == segredo) {

        alert("Você ACERTOU!");
    } else {

        alert("Você ERROU!!!!!!!!");
    }

</script>
```

Ela não recebe parâmetros. Em seu bloco, inseriremos todo o mecanismo de teste do número, da seguinte forma:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    var segredo = 5;

    var input = document.querySelector("input");

    function verifica() {

        if(input.value == segredo) {

        alert("Você ACERTOU!");
        } else {

        alert("Você ERROU!!!!!!!!");
        }

    }

</script>
```

Salvaremos o programa e recarregaremos a página. Não foi exibido nenhum alerta, pois o `verifica()` está guardado para ser executado posteriormente. No navegador, clicaremos na opção "Visualizar" na barra de menu superior, e selecionaremos "Desenvolvedor > Console JavaScript". No campo de _input_ digitaremos o número `4`. No console, chamaremos a função `verifica()` que acabamos de criar, digitando:

```scss
verifica()
```

Ao pressionarmos "Enter", aparecerá um pop up com a mensagem "Você errou!". Não é interessante para o usuário ter que abrir o console para fazer esta verificação, nosso objetivo é que o `verifica()` seja chamado sempre que o botão for clicado. Para isso, precisaremos trabalhar com o `<button>` do HTML no JavaScript. Isso porque queremos associar a função `verifica()` ao clique do botão.

Declararemos uma variável chamada `button` e daremos ao `document.querySelector()` o parâmetro `button` - o nome da tag:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    var segredo = 5;

    var input = document.querySelector("input");

    function verifica() {

        if(input.value == segredo) {

        alert("Você ACERTOU!");
        } else {

        alert("Você ERROU!!!!!!!!");
        }

    }

    var button = document.querySelector("button");

</script>
```

Para associar ao botão a execução do `verifica()` utilizaremos o `button.onclick()`, em português, "_on click_" significa "no clicar", ou seja, queremos que a verificação seja feita ao clique:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    var segredo = 5;

    var input = document.querySelector("input");

    function verifica() {

        if(input.value == segredo) {

        alert("Você ACERTOU!");
        } else {

        alert("Você ERROU!!!!!!!!");
        }

    }

    var button = document.querySelector("button");

    button.onclick = verifica();

</script>
```

Salvaremos o programa e recarregaremos a página. Surgirá um pop up imediatamente, o que não é o resultado desejado. Isso acontece pois, da maneira como declaramos, o `onclick` recebe `verifica()`, mas quando utilizamos os parênteses estamos chamando a função, portanto ela é que será executada ao recarregar a página.

É necessário fazer com que o `verifica()` esteja inserido no `onclick`. Retornaremos ao navegador e abriremos o console. Digitaremos:

```scss
verifica()
```

E, ao pressionarmos "Enter" veremos que a função é executada pois surge um pop up. Mas o que acontece se escrevermos somente `verifica`?

```scss
verifica()
undefined
verifica
function verifica() {
    if(input.value == segredo) {

        alert("Você ACERTOU!"});
    } else {

        alert("Você ERROU!!!!!!!!");
    }
}
```

Ao fazermos isso, é exibido o código da função. Assim, há uma grande diferença entre utilizar os parênteses, ou seja, executar a função, e não utilizá-los, situação em que teremos acesso ao código da função. Para solucionarmos isto, retornaremos ao código e, quando formos remover os parênteses do `verifica()` em `button.onclick`, teremos:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    var segredo = 5;

    var input = document.querySelector("input");

    function verifica() {

        if(input.value == segredo) {

        alert("Você ACERTOU!");
        } else {

        alert("Você ERROU!!!!!!!!");
        }

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Dessa forma, toda a informação contida em `verifica`, isto é, o código, está vinculado ao `onclick` do botão. Assim, ele estará preparado para executar a verificação sempre que o botão for clicado.

Salvaremos o programa e retornaremos ao navegador. Fecharemos o console e recarregaremos a página. Inseriremos o número `3` no _input_ e clicaremos no botão. Surgirá um pop up com a mensagem "Você errou!". Ao colocarmos o número correto, no caso `5`, e clicarmos no botão, aparecerá um pop up com a mensagem "Você acertou!".

No mundo JavaScript, conseguimos capturar os elementos do mundo HTML, verificar o valor destes elementos, e associar a execução de uma função a um clique de botão. Vimos que, ao abrirmos o console do navegador e fazermos o `verifica()`, estamos executando a função de forma manual. No entanto, se digitarmos `verifica` e pressionarmos "Enter", é impresso o código da função.

Como nosso objetivo é executar a função ao clique do botão, removemos os parênteses no código, fazendo com que ela fique inserida no `onclick` e, quando clicamos no botão do navegador, é ele quem insere os parênteses para chamar a função. Esta estratégia é mais interessante para o usuário.