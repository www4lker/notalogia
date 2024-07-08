---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/parando-a-repeticao/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# parando a repetição

## criado em: 
-  23-03-2023 - 15:49

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/oito - interaja de maneira diferente com os usuários\|oito - interaja de maneira diferente com os usuários]]
- tags: 
- Fontes & Links: 

---

## Transcrição

**Atenção**: com atualizações, o Google Chrome agora só mostra as mensagens através de `document.write()` realizadas dentro de um loop, somente quando a página for carregada completamente, isto é, quando o loop termina. Neste caso, para efeito de aprendizagem, utilizem `alert()` no lugar de `document.write()`.

O recurso de repetição que aprendemos anteriormente pode ser utilizado para melhorar nosso programa de adivinhação, por exemplo.

---

No editor de texto, abriremos novamente o programa de adivinhação, selecionando na barra de menu superior "File > Open... > jogo_advinha.html". Em seguida, o abriremos no navegador selecionando "Arquivo > Abrir arquivo... > jogo_advinha.html" Surgirá um pop up com a mensagem "Digite seu chute!". Digitaremos o número `5`, e obteremos o seguinte resultado:

```undefined
Você errou, o número pensado foi 6
```

Nosso objetivo será fornecer ao usuário três chances para descobrir o número. Retornaremos ao programa, no editor de texto. Precisamos analisar e identificar qual parte do código teremos que repetir. No caso, será a pergunta do chute, e todo o teste que verifica se é o número correto:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
}

    function mostra(frase) {

        document.write(frase);
        pulaLinha();
}

var numeroPensado = Math.round(Math.random() * 10);

var chute = parseInt(prompt("Digite seu chute!"));

if(chute == numeroPensado) {

    mostra("Você acertou!");
} else {

    mostra("Você errou, o número pensado foi " + numeroPensado);
}

</script>
```

Queremos repetir o bloco a cada chute do usuário. Para isso, criaremos um `while()`:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
}

    function mostra(frase) {

        document.write(frase);
        pulaLinha();
}

var numeroPensado = Math.round(Math.random() * 10);

while() {

    var chute = parseInt(prompt("Digite seu chute!"));

    if(chute == numeroPensado) {

        mostra("Você acertou!");
    } else {

        mostra("Você errou, o número pensado foi " + numeroPensado);
    }

}

</script>
```

Como queremos dar `3` chances, o `while()` será executado sempre que algo for menor ou igual a este número, no caso, a quantidade de tentativas. Vamos criar a variável `tentativas`:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
}

    function mostra(frase) {

        document.write(frase);
        pulaLinha();
}

var numeroPensado = Math.round(Math.random() * 10);

var tentativas = 1;

while() {

    var chute = parseInt(prompt("Digite seu chute!"));

    if(chute == numeroPensado) {

        mostra("Você acertou!");
    } else {

        mostra("Você errou, o número pensado foi " + numeroPensado);
    }

}

</script>
```

Assim, o `while()` terá como parâmetro `tentativas`, desde que esta corresponda a um número menor ou igual a `3`:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
}

    function mostra(frase) {

        document.write(frase);
        pulaLinha();
}

var numeroPensado = Math.round(Math.random() * 10);

var tentativas = 1;

while(tentativas <= 3) {

    var chute = parseInt(prompt("Digite seu chute!"));

    if(chute == numeroPensado) {

        mostra("Você acertou!");
    } else {

        mostra("Você errou, o número pensado foi " + numeroPensado);
    }

}

</script>
```

Enquanto o número de tentativas for menor ou igual a `3`, o bloco `while()` será inteiramente executado. Para que o número de tentativas seja acumulado, precisaremos incrementar a variável `tentativas`:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
}

    function mostra(frase) {

        document.write(frase);
        pulaLinha();
}

var numeroPensado = Math.round(Math.random() * 10);

var tentativas = 1;

while(tentativas <= 3) {

    var chute = parseInt(prompt("Digite seu chute!"));

    if(chute == numeroPensado) {

        mostra("Você acertou!");
    } else {

        mostra("Você errou, o número pensado foi " + numeroPensado);
    }

    tentativas++;
}

</script>
```

Salvaremos e recarregaremos a página. Aparecerá um pop up solicitando um chute. Digitaremos qualquer valor, e se o resultado for negativo, surgirá novamente um pop up. Teremos que inserir um número, em seguida surgirá mais um pop up e, ao digitarmos um número incorreto, não haverá mais tentativas, e teremos o seguinte resultado impresso:

```undefined
Você errou, o número pensado foi 6

Você errou, o número pensado foi 6

Você errou, o número pensado foi 6
```

Não faz sentido informarmos ao usuário que ele errou e, ao mesmo tempo, imprimir qual é o número pensado. Assim, alteraremos a mensagem para simplesmente "Você errou!":

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
}

    function mostra(frase) {

        document.write(frase);
        pulaLinha();
}

var numeroPensado = Math.round(Math.random() * 10);

var tentativas = 1;

while(tentativas <= 3) {

    var chute = parseInt(prompt("Digite seu chute!"));

    if(chute == numeroPensado) {

        mostra("Você acertou!");
    } else {

        mostra("Você errou!");
    }

    tentativas++;
}

</script>
```

Salvaremos e recarregaremos a página. Ao realizarmos novos testes, com valores errados em todas as tentativas, obteremos o seguinte resultado:

```undefined
Você errou!

Você errou!

Você errou!
```

O programa está funcionando como gostaríamos. Adicionaremos a função `mostra()` para que, ao final, seja impressa a mensagem `FIM`:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
}

    function mostra(frase) {

        document.write(frase);
        pulaLinha();
}

var numeroPensado = Math.round(Math.random() * 10);

var tentativas = 1;

while(tentativas <= 3) {

    var chute = parseInt(prompt("Digite seu chute!"));

    if(chute == numeroPensado) {

        mostra("Você acertou!");
    } else {

        mostra("Você errou!");
    }

    tentativas++;
}

mostra("FIM");
</script>
```

Salvaremos e retornaremos ao navegador. Recarregaremos a página e digitaremos números para realizar mais um teste. Erraremos em todas as tentativas e obteremos o seguinte resultado:

```undefined
Você errou!

Você errou!

Você errou!

FIM
```

Mas e se acertarmos, por exemplo, na segunda tentativa? Veremos que ele ainda assim insistirá em uma terceira tentativa. Por isso, faremos com que o programa pare de perguntar assim que o usuário acertar o número pensado. Vamos retornar ao código.

A primeira coisa a fazer é alterar a grafia das frases, deixando "errou" e "acertou" em letras maiúsculas, e alterando a frase para quando o usuário acerta:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
}

    function mostra(frase) {

        document.write(frase);
        pulaLinha();
}

var numeroPensado = Math.round(Math.random() * 10));

var tentativas = 1;

while(tentativas <= 3) {

    var chute = parseInt(prompt("Digite seu chute!"));

    if(chute == numeroPensado) {

        mostra("Você ACERTOU, o número pensado era " + numeroPensado);
    } else {

        mostra("Você ERROU!");
    }

    tentativas++;
}

mostra("FIM");
</script>
```

Nosso objetivo é que no caso de um acerto com uma ou duas tentativas ainda disponíveis, fazer com que o JavaScript saia do loop e, assim, pare de solicitar chutes. Para isso, podemos utilizar o comando `break`:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
}

    function mostra(frase) {

        document.write(frase);
        pulaLinha();
}

var numeroPensado = Math.round(Math.random() * 10);

var tentativas = 1;

while(tentativas <= 3) {

    var chute = parseInt(prompt("Digite seu chute!"));

    if(chute == numeroPensado) {

        mostra("Você ACERTOU, o número pensado era " + numeroPensado);
        break;

    } else {

        mostra("Você ERROU!");
    }

    tentativas++;
}

mostra("FIM");
</script>
```

Ao se deparar com o `break`, o JavaScript sai do loop e parte para a próxima instrução, que no caso é `mostra("FIM")`. Para testarmos, definiremos o `numeroPensado` como `4`:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
}

    function mostra(frase) {

        document.write(frase);
        pulaLinha();
}

var numeroPensado = 4;

var tentativas = 1;

while(tentativas <= 3) {

    var chute = parseInt(prompt("Digite seu chute!"));

    if(chute == numeroPensado) {

        mostra("Você ACERTOU, o número pensado era " + numeroPensado);
        break;

    } else {

        mostra("Você ERROU!");
    }

    tentativas++;
}

mostra("FIM");
</script>
```

Salvaremos e recarregaremos a página. Erraremos a primeira tentativa e, na segunda, digitaremos `4` - sabendo que é este o resultado correto. Ao fazermos isso, temos a seguinte mensagem:

```undefined
Você ERROU!

Você ACERTOU, o número pensado era 4

FIM
```

Poderíamos, alternativamente, inserir no loop a informação `tentativas = 4`:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
}

    function mostra(frase) {

        document.write(frase);
        pulaLinha();
}

var numeroPensado = 4;

var tentativas = 1;

while(tentativas <= 3) {

    var chute = parseInt(prompt("Digite seu chute!"));

    if(chute == numeroPensado) {

        mostra("Você ACERTOU, o número pensado era " + numeroPensado);
        tentativas=4;

    } else {

        mostra("Você ERROU!");
    }

    tentativas++;
}

mostra("FIM");
</script>
```

Desta forma, inevitavelmente o loop seria quebrado e obteríamos o mesmo resultado. Ou seja, podemos tanto utilizar o `break` quanto alterar a variável da condição, conferindo a ela um valor para o qual ela cessará de repetir. Em nosso código, manteremos o `break`:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
}

    function mostra(frase) {

        document.write(frase);
        pulaLinha();
}

var numeroPensado = 4;

var tentativas = 1;

while(tentativas <= 3) {

    var chute = parseInt(prompt("Digite seu chute!"));

    if(chute == numeroPensado) {

        mostra("Você ACERTOU, o número pensado era " + numeroPensado);
        break;

    } else {

        mostra("Você ERROU!");
    }

    tentativas++;
}

mostra("FIM");
</script>
```

Assim, temos um código inteligente, que dá mais chances ao usuário para que ele possa adivinhar o número. Retornaremos a fórmula do `numeroPensado` como estava, antes de alterarmos para `4`:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
}

    function mostra(frase) {

        document.write(frase);
        pulaLinha();
}

var numeroPensado = Math.round(Math.random() * 10);

var tentativas = 1;

while(tentativas <= 3) {

    var chute = parseInt(prompt("Digite seu chute!"));

    if(chute == numeroPensado) {

        mostra("Você ACERTOU, o número pensado era " + numeroPensado);
        break;

    } else {

        mostra("Você ERROU!");
    }

    tentativas++;
}

mostra("FIM");
</script>
```

Salvaremos e recarregaremos a página. Podemos tentar acertar mais uma vez para conferir se o código está adequado. As estruturas de repetição são capazes de resolver muitos problemas no mundo da programação.