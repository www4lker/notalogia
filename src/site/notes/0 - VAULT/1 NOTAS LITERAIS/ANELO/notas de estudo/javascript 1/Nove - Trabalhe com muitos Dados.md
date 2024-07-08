---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/nove-trabalhe-com-muitos-dados/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# 01 Armazenando muitos dados

## criado em: 
-  24-03-2023 - 12:21

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/manipulando array\|manipulando array]]
- tags: 
- Fontes & Links: 

---

Continuaremos a trabalhar com o programa `advinha_mais.html`, como na aula anterior. Nosso programa faz uma comparação entre aquilo que o usuário digita no campo de `input` e o **segredo** estabelecido em nosso código. Ao rodar, ele processa uma série de instruções:

-   Em primeiro lugar, ele gera um número aleatório dentro da variável `segredo`;
-   Em seguida, ele busca o `input` do mundo HTML para o JavaScript, fazendo com que o campo de texto ganhe foco, em razão do `input.focus()`;
-   Posteriormente, declaramos a função `verifica()`, a qual recebe o valor digitado pelo usuário no `input` e o compara com o segredo. Se correto, é exibido o alerta "Você acertou", caso contrário, surge um alerta com a mensagem "Você errou!";
-   Acertando ou errando, o campo de texto é limpo sempre que um número é digitado, e é exibido um pop up. Além disso, este campo limpo também ganha foco; e
-   Como queremos que a função seja executada somente ao clique do botão, criamos uma variável `button`, que busca esta funcionalidade do mundo HTML, e a associamos ao clique, por meio de `onclick`.

Nossa intenção agora é aumentar as chances de acerto para o usuário. Criaremos uma série de variáveis, cada uma contendo um valor de segredo diferente:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredo1 = 5;
    var segredo2 = 6;
    var segredo3 = 7;

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

Temos portanto três segredos, e queremos testar se o palpite do usuário, inserido no campo de texto, é igual ao `segredo1`, `segredo2` ou `segredo3`. Poderíamos fazer isto copiando a fórmula que já criamos e a utilizando para cada uma das variáveis, da seguinte forma:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredo1 = 5;
        var segredo2 = 6;
        var segredo3 = 7;

    var segredo = Math.round(Math.random() * 10);

    var input = document.querySelector("input");
        input.focus();

    function verifica() {

                if(input.value == segredo1) {

        alert("Você ACERTOU!");
        } else {

        alert("Você ERROU!!!!!!!!");
        }

                if(input.value == segredo2) {

        alert("Você ACERTOU!");
        } else {

        alert("Você ERROU!!!!!!!!");
        }

                if(input.value == segredo3) {

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

Salvaremos, retornaremos ao navegador e recarregaremos a página. Digitaremos `3` e pressionaremos o botão ao lado. Surgirá um pop up com "Você errou!", pressionaremos "Ok", mas o pop up aparecerá novamente, e assim sucessivamente, todas as vezes em que pressionamos "Ok", até esgotarmos todos os três segredos.

Se digitarmos, por exemplo, `5`, acertamos o primeiro segredo, mas o programa ainda assim conferirá o `input` com os demais, ou seja, surgirá um primeiro pop up com a mensagem "Você acertou!", seguido de mais três pop ups com "Você errou!".

Poderíamos acertar um **ou** outro segredo e, se tivéssemos mais segredos, seria necessário criar mais variáveis, além de fazer mais cópias do nosso `if()`. Esta não é a solução ideal, pois quanto mais segredos tivermos mais linhas de código serão necessárias. Então vamos editar o código para deixá-lo como estava antes de criarmos os segredos adicionais, e estabeleceremos o valor do segredo em `5`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredo = 5;

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

Faremos com que a variável `segredo` não guarde somente um valor, mas uma lista com diversos números. **Não podemos** fazer isso da seguinte forma:

```csharp
var segredo = 5 = 6 = 10 = 20;
```

Isto é **incorreto**. Precisaremos utilizar um novo tipo de dado, chamado **_array_**, inserindo os valores entre **colchetes** (**`[]`**):

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredo = [];

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

Se a variável conterá vários segredos, temos como boa prática de programação colocar seu nome no plural, portanto, de `var segredo` passaremos para `var segredos`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [];

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

Em seguida, inseriremos alguns valores para `segredos`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [5,7,10,2];

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

Dentro de um _array_, separamos os conteúdos por vírgula (**`,`**). Ao clicarmos em `verifica()`, o número inserido será comparado individualmente com cada um dos valores contidos no _array_ de `segredos`. Retornaremos ao navegador e acessaremos o console, em que declararemos a variável `segredos`.

> Para selecionar o console do navegador, basta clicar em "Visualizar" na barra de menu superior e, em seguida, "Desenvolvedor > Console JavaScript".

```csharp
var segredos = [5,7,10,2]
```

Ao pressionaremos "Enter", surgirá a palavra `undefined` abaixo:

```javascript
var segredos = [5,7,10,2]
undefined
```

Se escrevermos em seguida a palavra `segredos` e apertarmos "Enter" de novo, nosso _array_ será impresso:

```csharp
var segredos = [5,7,10,2]
undefined
segredos
[5,7,10,2]
```

E se quisermos acessar somente um elemento do _array_? O primeiro, por exemplo? Para fazermos isso, teremos que passar a sua posição para o console. Como queremos o primeiro, utilizaremos o número `1` e o inseriremos entre os colchetes:

```csharp
var segredos = [5,7,10,2]
undefined
segredos
[5,7,10,2]
segredos[1]
```

Clicando em "Enter", veremos que é exibido o número `7`, isto é, a segunda posição:

```csharp
var segredos = [5,7,10,2]
undefined
segredos
[5,7,10,2]
segredos[1]
7
```

Isto aconteceu porque no JavaScript - e em algumas outras linguagens de programação -, a primeira posição é representada pelo número `0`. Sendo assim, se quisermos isolar o primeiro elemento do _array_, precisaremos utilizá-lo:

```csharp
var segredos = [5,7,10,2]
undefined
segredos
[5,7,10,2]
segredos[1]
7
segredos[0]
5
```

... E assim por diante. Neste _array_, temos um total de quatro posições, portanto, elas são representadas pelos números `0`, `1`, `2` e `3`. Se digitarmos `segredos[4]` e pressionarmos "Enter" diversas vezes, ele retornará `undefined`:

```javascript
var segredos = [5,7,10,2]
undefined
segredos
[5,7,10,2]
segredos[1]
7
segredos[0]
5
segredos[1]
7
segredos[3]
2
segredos[4]
undefined
```

Aprendemos a criar um _array_ no JavaScript e a acessar cada elemento individualmente. Para fazermos a verificação, a função deverá percorrer cada elemento do _array_. No console do navegador, apagaremos tudo que escrevemos até este ponto e digitaremos `var segredos = [5,7,10,2]`, em seguida pressionaremos "Enter" e teremos o seguinte resultado:

```javascript
var segredos = [5,7,10,2];
undefined
```

Se o palpite for, por exemplo, `4`, é necessário examinar os segredos da seguinte forma:

```javascript
var segredos = [5,7,10,2];
undefined
segredos[0] == 4
false
```

O que fizemos foi digitar `segredos` e acompanhar da posição que queremos analisar, no caso, `0`. Como vimos, o duplo sinal de igual (**`==`**) representa igualdade, diferente de quando é utilizado sozinho, que lemos como "recebe". Assim, estamos perguntando se o número da posição `0` é igual a `4`. Clicando em "Enter", é feita a verificação, e teremos como resposta, `false`. Tentaremos outra posição, a `1`:

```javascript
var segredos = [5,7,10,2];
undefined
segredos[0] == 4
false
segredos[1] == 4
false
```

E assim por diante, até a posição `3`:

```javascript
var segredos = [5,7,10,2];
undefined
segredos[0] == 4
false
segredos[1] == 4
false
segredos[2] == 4
false
segredos[3] == 4
false
```

Se formos testar o número `7`, precisamos digitar toda esta operação novamente:

```javascript
var segredos = [5,7,10,2];
undefined
segredos[0] == 4
false
segredos[1] == 4
false
segredos[2] == 4
false
segredos[3] == 4
false
segredos[0] == 7
false
segredos[1] == 7
true
```

Como o número da segunda posição é `7`, obtivemos um resultado verdadeiro. A verificação deve começar na posição `0` e seguir até o limite da lista, que em nosso caso é a posição `3`.

> Em regra, o número de posições equivale ao de elementos menos um, por exemplo, quando temos `4` elementos, o número de posições será `4 - 1`, portanto, `3`.

Alternativamente, poderíamos ter uma variável `posicao` que recebe o valor `0` e, em seguida, faríamos a verificação declarando:

```undefined
segredos[posicao] == 9
```

Estamos perguntando se o segredo da `posição` `0` é o número `9` e, no caso, não é:

```javascript
var segredos = [5,7,10,2];
undefined
segredos[0] == 4
false
segredos[1] == 4
false
segredos[2] == 4
false
segredos[3] == 4
false
segredos[0] == 7
false
segredos[1] == 7
true
posicao = 0
0
segredos[posicao] == 9
false
```

Assim, faremos a incrementação da posição, que passará a ser `posicao++`, e de `0`, ela foi para `1`. Testaremos novamente:

```javascript
var segredos = [5,7,10,2];
undefined
segredos[0] == 4
false
segredos[1] == 4
false
segredos[2] == 4
false
segredos[3] == 4
false
segredos[0] == 7
false
segredos[1] == 7
true
posicao = 0
0
segredos[posicao] == 9
false
posicao++
0
segredos[posicao] == 9
false
```

Acabamos de testar a primeira posição, agora incrementaremos a variável mais uma vez para testarmos a próxima. Em seguida, realizaremos um novo teste, com a variável `posicao`, considerando que agora ela passou a equivaler à segunda posição:

```javascript
var segredos = [5,7,10,2];
undefined
segredos[0] == 4
false
segredos[1] == 4
false
segredos[2] == 4
false
segredos[3] == 4
false
segredos[0] == 7
false
segredos[1] == 7
true
posicao = 0
0
segredos[posicao] == 9
false
posicao++
0
segredos[posicao] == 9
false
posicao++
1
segredos[posicao] == 9
false
```

Limparemos o console novamente e realizaremos novos testes, com o número `10`:

```javascript
var segredos = [5,7,10,2];
undefined
var posicao = 0;
undefined
segredos[posicao] == 10
false
posicao++
0
segredos[posicao] == 10
false
posicao++
1
segredos[posicao] == 10
true
```

Temos que fazer uma repetição para testarmos todas as posições. Retornaremos ao código e, na função `verifica()`, criaremos um `for()`, lembrando que ele conta com três espaços:

```scss
for(espaco1; espaco2; espaco3)
```

Deste modo, nossa verificação contida no `if()` será inserida neste `for()`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [5,7,10,2];

    var input = document.querySelector("input");
        input.focus();

    function verifica() {

            for(espaco1; espaco2; espaco3) {

                if(input.value == segredo) {

                    alert("Você ACERTOU!");
        } else {

                    alert("Você ERROU!!!!!!!!");
        }
            }

                input.value = "";
                input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Por que colocar dentro do `for()`? Porque precisamos repetir a verificação do que foi digitado, com o segredo, para cada item do nosso _array_.

No `for()`, declararemos uma variável chamada `posicao`, que inicialmente recebe o valor `0`. A condição para repetição é que a `posicao` seja menor do que `4` e que, enquanto não atingir este limite, continue a se repetir. Por fim, a variável será incrementada, portanto utilizaremos `posicao++`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [5,7,10,2];

    var input = document.querySelector("input");
        input.focus();

    function verifica() {

            for(var posicao = 0; posicao < 4; posicao++) {

                if(input.value == segredo) {

                    alert("Você ACERTOU!");
        } else {

                    alert("Você ERROU!!!!!!!!");
        }
            }

                input.value = "";
                input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Assim, quando `posicao` alcançar `4`, o JavaScript perguntará se este número é menor que `4`, e como não é, ele deixará de repetir o teste. Isso porque não existe a posição `4` em nosso _array_. Ao fazermos o teste, agora não o compararemos mais com `segredo`, mesmo porque esta variável não existe mais. Em seu lugar, inseriremos o _array_ de `segredos`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [5,7,10,2];

    var input = document.querySelector("input");
        input.focus();

    function verifica() {

            for(var posicao = 0; posicao < 4; posicao++) {

                if(input.value == segredos) {

                    alert("Você ACERTOU!");
        } else {

                    alert("Você ERROU!!!!!!!!");
        }
            }

                input.value = "";
                input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Além disso, faremos com que a comparação seja feita na posição escolhida, aquela determinada pelo nosso `for()`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [5,7,10,2];

    var input = document.querySelector("input");
        input.focus();

    function verifica() {

            for(var posicao = 0; posicao < 4; posicao++) {

                if(input.value == segredos[posicao]) {

                    alert("Você ACERTOU!");
        } else {

                    alert("Você ERROU!!!!!!!!");
        }
            }

                input.value = "";
                input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Salvaremos o programa e recarregaremos a página. Digitaremos `3` e pressionaremos o botão, o que fará com que surjam quatro pop ups, e em todos eles seremos informados de que erramos o número.

Em seguida, digitaremos `10`, e como este número está na posição `2`, ele deve testar duas vezes e acertar na terceira. Surge um primeiro pop up com a mensagem de erro, um segundo com a mesma mensagem, e um terceiro informando que acertamos, mas ele continua realizando o teste na última posição - e não queremos que isto aconteça.

Se acertarmos, não faz sentido continuarmos a verificação. Por isso, utilizaremos a função `break`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [5,7,10,2];

    var input = document.querySelector("input");
        input.focus();

    function verifica() {

            for(var posicao = 0; posicao < 4; posicao++) {

                if(input.value == segredos[posicao]) {

                    alert("Você ACERTOU!");
                    break;
        } else {

                    alert("Você ERROU!!!!!!!!");
        }
            }

                input.value = "";
                input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Salvaremos o programa e recarregaremos a página. Digitaremos o número `7`, que corresponde a posição 1, portanto o primeiro teste retorna um erro e, no segundo, acertamos. Após isso, não são feitos mais testes - nosso código funcionou!

Outro ponto em nosso programa é que ele exibe um pop up com mensagem para cada erro cometido, e não queremos que isto aconteça. Nosso objetivo é que seja exibida uma única mensagem. Por isto, removeremos o `else` que contém a mensagem de erro:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [5,7,10,2];

    var input = document.querySelector("input");
        input.focus();

    function verifica() {

            for(var posicao = 0; posicao < 4; posicao++) {

                if(input.value == segredos[posicao]) {

                    alert("Você ACERTOU!");
                    break;
        } 
            }

                input.value = "";
                input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Salvaremos o programa e recarregaremos a página. Digitaremos `2` e clicaremos no botão, e receberemos somente um aviso de acerto, conforme pretendido. Em seguida, usaremos `6` que, como sabemos, não está em nosso _array_. Pressionaremos o botão, e nada acontece. Quando o usuário comete um erro não é exibida nenhuma mensagem.

Um detalhe ao qual precisamos estar atentos é: se alterarmos o número de elementos em um _array_, precisaremos alterar também nosso `for()`, para que os testes sejam feitos até o limite da nova posição. Por exemplo, se em vez de `4` tivéssemos `5` elementos em nosso _array_, nosso código passaria a ser o seguinte:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [5,7,10,2,3];

    var input = document.querySelector("input");
        input.focus();

    function verifica() {

            for(var posicao = 0; posicao < 5; posicao++) {

                if(input.value == segredos[posicao]) {

                    alert("Você ACERTOU!");
                    break;
        } 
            }

                input.value = "";
                input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Para não termos que alterar nosso `for()` todas as vezes que quisermos adicionar um novo elemento, poderemos utilizar o `.length` para termos sempre o _array_ atual no `for()`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [5,7,10,2,3];

    var input = document.querySelector("input");
        input.focus();

    function verifica() {

            for(var posicao = 0; posicao < segredos.length; posicao++) {

                if(input.value == segredos[posicao]) {

                    alert("Você ACERTOU!");
                    break;
        } 
            }

                input.value = "";
                input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Isso gera um retorno da quantidade de elementos contidos naquele _array_, para a função. Em seguida, resolveremos um problema que vimos anteriormente, que é a falta de um alerta indicando ao usuário que ele errou o número. Inseriremos esta referência ao final do `for()`, ou seja, após a varredura em todos os elementos do _array_, por meio da inserção do `alert()`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [5,7,10,2,3];

    var input = document.querySelector("input");
        input.focus();

    function verifica() {

            for(var posicao = 0; posicao < segredos.length; posicao++) {

                if(input.value == segredos[posicao]) {

                    alert("Você ACERTOU!");
                    break;
        } 
            }

                alert("Você errou!");

                                input.value = "";
                input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

> Recapitulando: o _array_ será varrido por completo, todas as posições serão testadas e, ao final, se não houve compatibilidade em nenhum elemento, será exibida a mensagem "Você errou!".

Salvaremos o programa e recarregaremos a página. Digitaremos `3` e pressionaremos um botão, aparecerá um pop up com a mensagem "Você acertou!", em seguida surge um novo pop up com "Você errou!". Nossa ideia é exibir o alerta "Você ERROU!" somente quando o usuário não conseguir acertar nenhum dos números em nosso _array_.

Para resolvermos isso, antes do `for()`, declararemos uma variável chamada `achou`, que recebe `false`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [5,7,10,2,3];

    var input = document.querySelector("input");
        input.focus();

    function verifica() {

            var achou = false;

            for(var posicao = 0; posicao < segredos.length; posicao++) {

                if(input.value == segredos[posicao]) {

                    alert("Você ACERTOU!");
                    break;
        } 
            }

                alert("Você errou!");

                                input.value = "";
                input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Quando o número digitado corresponder a um dos elementos do _array_, declararemos `achou = true`:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [5,7,10,2,3];

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

                alert("Você errou!");

                                input.value = "";
                input.focus();

    }

    var button = document.querySelector("button");

    button.onclick = verifica;

</script>
```

Com isso, informamos ao JavaScript que um dos números é compatível. Caso o número digitado não esteja presente em `segredos`, informaremos que `if(achou == false)`, ou seja, se `achou` for `false`, deve ser exibido um aviso informando ao usuário que ele errou:

```xml
<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>

    var segredos = [5,7,10,2,3];

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

Salvaremos o programa e recarregaremos a página. Vamos testar com `1`, e surgirá um pop up com "Você ERROU!". Em seguida, digitaremos `3`, e o pop up aparecerá com a mensagem "Você acertou!" e em seguida, nada mais, ou seja, funcionou!