---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/input-focus/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# input focus

## criado em: 
-  23-03-2023 - 17:12

### Conteúdo Relacionado
- notas: 
- tags: 
- Fontes & Links: 

---

A próxima melhoria que faremos em nosso programa implica em fazermos com que o campo de texto seja esvaziado quando o usuário errar uma tentativa. Para isso, após a função `verifica()`, declararemos que o `input.value` receberá uma string em branco:

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

                input.value = "";

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Da mesma forma como conseguimos pegar o `<input>` do mundo HTML, também conseguimos lhe conferir um valor a partir do JavaScript. Salvaremos o programa e recarregaremos a página. Inseriremos `4` e clicaremos no botão, e surgirá um pop up informando que o número está incorreto. Ao clicarmos no botão Ok", veremos que o campo para digitação de texto foi limpo.

Em seguida, daremos um foco no campo de texto sempre que o usuário errar o número utilizando a função `input.focus()`:

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

                input.value = "";
                input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Salvaremos e recarregaremos a página. Assim, ao digitarmos um palpite incorreto, e após o surgimento do pop up, a caixa de texto ficará em foco, ganhando uma moldura colorida, indicando que pode ser feita mais uma tentativa. Isso melhora a experiência do usuário.

Nosso objetivo neste curso é aprender a lógica de programação, com noções básicas de HTML e JavaScript. Conseguimos aprender como este interage de forma dinâmica com o HTML, deixando nosso programa com aspecto profissional.

Até agora trabalhamos com um segredo fixo, em seguida, faremos com que ele seja mutável, utilizando o `Math.random()` e o `Math.round()`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    var segredo = Math.round(Math.random() * 10);

    var input = document.querySelector("input");

    function verifica() {

        if(input.value == segredo) {

        alert("Você ACERTOU!");
        } else {

        alert("Você ERROU!!!!!!!!");
        }

                input.value = "";
                input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Salvaremos o programa e recarregaremos a página. Podemos digitar diversos números para realizar testes. Para aprimorá-lo, faremos com que a caixa de texto ganhe foco sempre que recarregarmos a página, com o `input.focus()` logo após chamarmos o `input` para o mundo JavaScript:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    var segredo = Math.round(Math.random() * 10);

    var input = document.querySelector("input");
        input.focus();

    function verifica() {

        if(input.value == segredo) {

        alert("Você ACERTOU!");
        } else {

        alert("Você ERROU!!!!!!!!");
        }

                input.value = "";
                input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Salvaremos e recarregaremos a página, e desta vez o campo de texto está em foco e com a borda colorida. Neste capítulo criamos um ambiente mais agradável para captação dos dados do usuário.