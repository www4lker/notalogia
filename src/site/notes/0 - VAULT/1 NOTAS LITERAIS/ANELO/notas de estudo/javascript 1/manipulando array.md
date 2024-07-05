---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/manipulando-array/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# manipulando array

## criado em: 
-  24-03-2023 - 13:19

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/fim da faixa branca - despedida do curso de logica 1\|fim da faixa branca - despedida do curso de logica 1]]
- tags: 
- Fontes & Links: https://cursos.alura.com.br/course/logica-programacao-javascript-html/task/17765

---

Nesta parte final do nosso curso, refinaremos certos aspectos do nosso programa, como a lista de `segredos`, que é fixa, mas poderia ser gerada aleatoriamente. Ao declararmos um _array_, podemos passar os itens em sua própria declaração, ou podemos utilizar a função `push()`, da seguinte forma:

```scss
<script>

segredos.push(5)
segredos.push(7)
segredos.push(10)
segredos.push(2)
sergedos.push(3)

//código continua
```

Como já sabíamos quais eram os itens do _array_, os declarávamos entre colchetes (**`[]`**) como fazíamos anteriormente. A partir de agora, como queremos que sejam números aleatórios, faremos da seguinte forma:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [];
    segredos.push(Math.round(Math.random() * 10));
    segredos.push(Math.round(Math.random() * 10));
    segredos.push(Math.round(Math.random() * 10));
    segredos.push(Math.round(Math.random() * 10));
    segredos.push(Math.round(Math.random() * 10));

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Para sabermos quais serão os itens gerados e mostrar uma mensagem secreta para o desenvolvedor, utilizaremos o `console.log()`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [];
    segredos.push(Math.round(Math.random() * 10));
    segredos.push(Math.round(Math.random() * 10));
    segredos.push(Math.round(Math.random() * 10));
    segredos.push(Math.round(Math.random() * 10));
    segredos.push(Math.round(Math.random() * 10));

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Tudo que é passado para o `console.log()` é visualizado apenas se o console do navegador for aberto. Salvaremos o programa e retornaremos ao navegador para recarregarmos a página. Abriremos o console, onde veremos o _array_ com os seguintes números:

```makefile
Array[5]
0: 9
1: 3
2: 4
3: 4
4:10
lenght: 5
__proto__: Array[0]
```

Há um problema: foram gerados números aleatórios, entretanto, coincidiu de termos um número duplicado - isto não pode acontecer. Resolveremos este problema criando um mecanismo para a geração automática de segredos sem elementos duplicados.

Primeiro, veremos que é moroso digitarmos todas as vezes o método do `Math.random()`, então criaremos a função `sorteia()`, que terá em seu bloco o método abaixo:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    var segredos = [];
    segredos.push(sorteia());
    segredos.push(sorteia());
    segredos.push(sorteia());
    segredos.push(sorteia());
    segredos.push(sorteia());

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Apesar de nos poupar na escrita, temos de utilizar o `push()` uma série de vezes. O ideal é que este processo de sorteio seja automatizado. Para isso, criaremos uma função chamada `sorteiaNumeros()`, a qual precisará nos devolver uma lista de segredos, e receberá como parâmetro a quantidade de segredos que queremos gerar. Assim, se queremos `5`, ela será escrita da seguinte forma:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    var segredos = sorteiaNumeros(5);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Escrita desta forma, a função `sorteiaNumeros()` ainda **não existe**. Ela deve ser capaz de nos dar uma lista com números aleatórios que não se repetem. Para criá-la, teremos que declarar a `function`, que receberá como parâmetro `quantidade`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

    }

    var segredos = sorteiaNumeros(5);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

O número que passarmos como parâmetro em `sorteiaNumeros()` é o total de itens aleatórios que não se repetem, e que serão retornados. No caso, passaremos `3`, sendo assim, `quantidade` valerá `3`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

    }

    var segredos = sorteiaNumeros(3);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Dentro da função `sorteiaNumero()` criaremos uma nova variável, também chamada `segredos` - o nome não importa, já que ela existe somente dentro da função.

> Tudo que está inserido em uma função só existe dentro desta, a menos que seja utilizado um `return` para capturar o seu resultado.

A variável `segredos` começa com o _array_ vazio:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

        var segredos = [];

    }

    var segredos = sorteiaNumeros(3);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Em seguida, criaremos o contador `numero`, que iniciará em `1` e, enquanto `numero` for menor ou igual a `quantidade`, o `segredos.push()` receberá a função `sorteia()`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

        var segredos = [];

        var numero = 1;

        while(numero <= quantidade) {

              segredos.push(sorteia());
              numero++;

        }

    }

    var segredos = sorteiaNumeros(3);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Ao final de tudo, teremos um `return` de `segredos`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

        var segredos = [];

        var numero = 1;

        while(numero <= quantidade) {

              segredos.push(sorteia());
              numero++;

        }

        return segredos;

    }

    var segredos = sorteiaNumeros(3);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Recapitulando:

-   Nosso código será carregado e executará a função `sorteia()`;
-   Esta, por sua vez, é uma atalho para que possamos retornar um número aleatório entre `1` e `10`;
-   A segunda função, `sorteiaNumeros()`, recebe a quantidade de números que queremos sortear para nos devolver uma lista de segredos que, ao ser chamada, declara uma lista vazia;
-   A variável `numero` foi criada para sabermos que a quantidade máxima de números que precisamos gerar foi atingida;
-   O último número será incrementado, mas não poderá dar continuidade ao `while()`, com isso partimos para a execução da última instrução, que é `return segredos`;
-   Assim, o `segredos` que está na `var segredos` recebe o valor do `segredos` que está em `return`.

Vamos verificar se funciona, salvando o programa, retornando ao programa e recarregando a página.

No campo de texto, digitaremos `4`, e surgirá uma mensagem de erro, assim sucessivamente, até digitarmos o número `8`, ocasião em que surgirá a mensagem "Você acertou!". Recarregaremos a página e tentaremos novamente o mesmo número. Desta vez surgirá uma mensagem de erro, porque foi gerada uma nova lista de números aleatórios.

Nosso problema de números repetidos persiste. Para visualizarmos isto, logo após o `var segredos`, declararemos o `console.log()`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

        var segredos = [];

        var numero = 1;

        while(numero <= quantidade) {

              segredos.push(sorteia());
              numero++;

        }

        return segredos;

    }

    var segredos = sorteiaNumeros(3);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Salvaremos o programa e recarregaremos a página. Para visualizarmos melhor, aumentaremos o número de elementos, de `3` para `4`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

        var segredos = [];

        var numero = 1;

        while(numero <= quantidade) {

              segredos.push(sorteia());
              numero++;

        }

        return segredos;

    }

    var segredos = sorteiaNumeros(4);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Salvaremos e recarregaremos a página. No console, veremos que foram gerados os seguintes números:

```csharp
[5, 8, 9, 5]
```

Ou seja, aparecem duas vezes o número `5` - isto não pode acontecer. Portanto, o resultado de `sorteia()` será inserido em uma variável que chamaremos de `numeroAleatorio`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

        var segredos = [];

        var numero = 1;

        while(numero <= quantidade) {

              var numeroAleatorio = sorteia();
              segredos.push(numeroAleatorio);
              numero++;

        }

        return segredos;

    }

    var segredos = sorteiaNumeros(4);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

A ideia é usarmos o `push()` somente se o segredo não for encontrado dentre os elementos da lista criada. Sendo assim, declararemos que, se o `achou` for igual a `false`, chamamos o `segredos.push()`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

        var segredos = [];

        var numero = 1;

        while(numero <= quantidade) {

              var numeroAleatorio = sorteia();

              if (achou == false) {
                     segredos.push(numeroAleatorio);
              }
              numero++;

        }

        return segredos;

    }

    var segredos = sorteiaNumeros(4);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Precisaremos declarar a variável `achou`, logo abaixo da `numeroAleatorio`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

        var segredos = [];

        var numero = 1;

        while(numero <= quantidade) {

              var numeroAleatorio = sorteia();
              var achou = false;

              if (achou == false) {
                     segredos.push(numeroAleatorio);
              }
              numero++;

        }

        return segredos;

    }

    var segredos = sorteiaNumeros(4);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Entre a `var achou` e o nosso `if()` teremos que varrer a lista de números sorteados de segredos, e verificar se o número selecionado aleatoriamente está contido nela. Se estiver, o `achou` será verdadeiro, e o `push()` não será executado. Assim, criaremos um `for`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

        var segredos = [];

        var numero = 1;

        while(numero <= quantidade) {

              var numeroAleatorio = sorteia();
              var achou = false;

              for(var posicao = 0; posicao < segredos.length; posicao++) {

                     if(segredos[posicao] == numeroAleatorio){
                           achou = true;
                           break;
                     }

              }

              if (achou == false) {
                     segredos.push(numeroAleatorio);
              }
              numero++;

        }

        return segredos;

    }

    var segredos = sorteiaNumeros(4);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Recapitulando:

-   Pedimos para que fossem sorteados três números;
-   A variável `segredos` inicialmente está vazia;
-   A variável `numero` inicia em `1`;
-   `numero` é uma variável que nos ajudará a contabilizar quantos itens já foram sorteados;
-   O `while()` deverá ser repetido o mesmo número de vezes contido em `quantidade`, no caso, `4`;
-   Dentro do `while()`, será sorteado um número aleatório e, em seguida, a variável `achou` terá como valor `false`, indicando que ele ainda não foi encontrado - isso porque este ainda não verificado na lista de segredos;
-   Assim, percorreremos a lista de segredos para sabermos se o número gerado está inserido nela, caso esteja, o `achou` recebe `true`, e teremos um `break`, e deste modo a repetição cessa;
-   Se não achou, o elemento `numeroAleatorio` é inserido novamente.

Temos, adiante, o incremento do número em `numero++`, mas ele só deve acontecer na hipótese do número **não ser encontrado**. Por isso, o incremento deve estar inserido em nosso `if(achou == false)`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

        var segredos = [];

        var numero = 1;

        while(numero <= quantidade) {

              var numeroAleatorio = sorteia();
              var achou = false;

              for(var posicao = 0; posicao < segredos.length; posicao++) {

                     if(segredos[posicao] == numeroAleatorio){
                           achou = true;
                           break;
                     }

              }

              if (achou == false) {
                     segredos.push(numeroAleatorio);
                     numero++;
              }

        }

        return segredos;

    }

    var segredos = sorteiaNumeros(4);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Com isso, temos o seguinte resultado: desejamos que o programa gere `4` números aleatórios, mas se no segundo for um duplicado, não poderemos ter um incremento da quantidade de números gerados, e sim a geração de um novo número.

Salvaremos o programa e recarregaremos a página. No console, veremos que são geradas listas com quatro números, sem que haja repetição entre os elementos. Para que possamos visualizar isto de forma mais clara, podemos aumentar o número de elementos para `5`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

        var segredos = [];

        var numero = 1;

        while(numero <= quantidade) {

              var numeroAleatorio = sorteia();
              var achou = false;

              for(var posicao = 0; posicao < segredos.length; posicao++) {

                     if(segredos[posicao] == numeroAleatorio){
                           achou = true;
                           break;
                     }

              }

              if (achou == false) {
                     segredos.push(numeroAleatorio);
                     numero++;
              }

        }

        return segredos;

    }

    var segredos = sorteiaNumeros(5);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Salvando o programa e recarregando a página, notaremos que, mesmo com cinco números, não há nenhum número repetido. Nosso próximo problema é que o programa fornece o número `0`, e não queremos que este seja um número válido. Para resolver isso, inseriremos o teste dentro de uma condição para a qual o número aleatório é diferente de `0`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

        var segredos = [];

        var numero = 1;

        while(numero <= quantidade) {

              var numeroAleatorio = sorteia();
              var achou = false;

              if (numeroAleatorio !== 0) {
                     for(var posicao = 0; posicao < segredos.length; posicao++) {

                           if(segredos[posicao] == numeroAleatorio){
                                achou = true;
                                break;
                           }

                     }

                     if (achou == false) {
                           segredos.push(numeroAleatorio);
                           numero++;
                     }
              }

        }

        return segredos;

    }

    var segredos = sorteiaNumeros(5);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Salvaremos e recarregaremos a página. No console, observaremos que não importa quantas vezes atualizemos a página, nunca teremos números duplicados, nem o número `0`. Para gerarmos `3` números, vamos alterar nossa função novamente.

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
    function sorteia() {

       return Math.round(Math.random() * 10);

    }

    function sorteiaNumeros(quantidade) {

        var segredos = [];

        var numero = 1;

        while(numero <= quantidade) {

              var numeroAleatorio = sorteia();
              var achou = false;

              if (numeroAleatorio !== 0) {
                     for(var posicao = 0; posicao < segredos.length; posicao++) {

                           if(segredos[posicao] == numeroAleatorio){
                                achou = true;
                                break;
                           }

                     }

                     if (achou == false) {
                           segredos.push(numeroAleatorio);
                           numero++;
                     }
              }

        }

        return segredos;

    }

    var segredos = sorteiaNumeros(3);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

    function verifica() {

       var achou = false;

       for(var posicao = 0; posicao < segredos.length; posicao++) {

              if(input.value == segredos[posicao]) {

                     alert("Você ACERTOU!");
                     achou = true;
                     break;
              } 
       }

       if(achou == false) {

              alert("Você ERROU!");
       }

       input.value = "";
       input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Podemos continuar atualizando a página, e nunca teremos um número duplicado. Com isso, combinamos a construção de funções, loops, entre outras ferramentas, para criar uma lista de segredos que não se repetem.