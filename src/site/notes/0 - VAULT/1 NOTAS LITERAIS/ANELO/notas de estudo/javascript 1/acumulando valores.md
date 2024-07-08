---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/acumulando-valores/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# acumulando valores

## criado em: 
-  23-03-2023 - 14:26

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/parando a repetição\|parando a repetição]]
- tags: 
- Fontes & Links: 

---

Nesta aula, criaremos outro programa! Selecionaremos a opção "Salvar Como", e daremos ao novo arquivo o nome de `media_idades_familiares.html`. Apagaremos o trecho do programa referente à tabuada de 7, mantendo somente as funções `pulaLinha()` e `mostra()`:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

</script>
```

Nosso objetivo é calcular a média das idades de nossos familiares, e utilizaremos nomes e idades fictícios, os quais serão inseridos na forma de variáveis:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var idadePedro = 28;
var idadeMarta = 32;
var idadeJorge = 60;
var idadeBete = 22;

</script>
```

Para termos a médias entre as idades, precisaremos somá-las e dividir pela quantidade. Criaremos uma variável `totalIdades`:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var idadePedro = 28;
var idadeMarta = 32;
var idadeJorge = 60;
var idadeBete = 22;

var totalIdades = (idadePedro + idadeMarta + idadeJorge + idadeBete);

</script>
```

Em seguida, para calcularmos a média entre elas, criaremos a variável `mediaIdades`, que receberá `totalIdades` dividida por `4`. Para imprimir, utilizaremos a função `mostra()`:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var idadePedro = 28;
var idadeMarta = 32;
var idadeJorge = 60;
var idadeBete = 22;

var totalIdades = (idadePedro + idadeMarta + idadeJorge + idadeBete);
var mediaIdades = totalIdades/4;

mostra(mediaIdades);

</script>
```

Salvaremos o programa, retornaremos ao navegador e selecionaremos as opções "Arquivo > Abrir arquivo... > media_idade_familiares.html", para abrirmos o programa. Obteremos o seguinte resultado:

```undefined
35.5
```

Se quisermos ampliar a utilização do programa, veremos que cada família possui uma quantidade diferente de familiares. Se quisermos tornar o programa genérico, para que funcione com qualquer família, teremos sempre que alterar todas as variáveis, e não queremos esta solução.

Queremos que o programa funcione de modo a perguntar ao usuário a quantidade de familiares a serem analisados. O usuário insere a resposta e, em seguida, queremos que o programa pergunte as idades dos familiares. O número de vezes que o programa perguntará é igual ao número de familiares inseridos pelo usuário.

Assim, utilizaremos a função `prompt()`, pedindo para que seja lida uma informação do teclado, tantas vezes quanto houver familiares. Por exemplo, se há cinco familiares, as idades serão solicitadas cinco vezes.

Além disso, teremos que somar as idades inseridas para podermos, ao final, calcular a média. Apagaremos o código criado até o momento, mantendo somente as funções `pulaLinha()` e `mostra()`:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

</script>
```

A primeira informação que precisamos perguntar ao usuário é a quantidade de familiares, portanto, teremos uma variável chamada `totalFamiliares`:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var totalFamiliares = 

</script>
```

Para perguntarmos ao usuário, utilizaremos o `prompt()` com a seguinte pergunta "Quantidade de familiares?":

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var totalFamiliares = prompt("Quantidade de familiares?");

</script>
```

Já que queremos ler esta resposta ao `prompt()` como um número, utilizaremos o `parseInt()`:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var totalFamiliares = parseInt(prompt("Quantidade de familiares?"));

</script>
```

Com isto, temos o total de familiares. Para descobrirmos as idades de cada um, perguntaremos tantas vezes quanto o número de familiares. Primeiro, inseriremos a pergunta, e como leremos a resposta como um número, utilizaremos o `parseInt()`:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var totalFamiliares = parseInt(prompt("Quantidade de familiares?"));

var idade = parseInt(prompt("Informe idade do familiar"));
</script>
```

Salvaremos o programa e retornaremos ao navegador, onde recarregaremos a página. Surgirá um primeiro pop up solicitando o número de familiares, e digitaremos `3`. A seguir, surgirá um pop up solicitando a idade do familiar. Já que temos `3` familiares, para que o programa funcione, precisamos que isso seja perguntado `3` vezes, entretanto, ao pressionarmos "Ok" veremos que só foi perguntado uma vez.

Isso acontece porque não indicamos ao programa que ele precisa fazer esta pergunta de acordo com a quantidade de familiares inserida. Para isso, criaremos um `while()`:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var totalFamiliares = parseInt(prompt("Quantidade de familiares?"));

while(? <= totalFamiliares) {

    var idade = parseInt(prompt("Informe idade do familiar"));
}

</script>
```

Mas como o `while()` saberá que já perguntou uma, duas ou três vezes? Precisaremos de uma variável de incremento para que seja alterada a cada leitura de idade de um familiar, fazendo com que ela saiba quantas idades já leu. Então, criaremos a `var numero` que receberá `0`:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var totalFamiliares = parseInt(prompt("Quantidade de familiares?"));

var numero = 0;
while(? <= totalFamiliares) {

    var idade = parseInt(prompt("Informe idade do familiar"));
}

</script>
```

Enquanto `numero` for menor ou igual ao `totalFamiliares`, o `prompt()` "Informe idade do familiar" será executado:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var totalFamiliares = parseInt(prompt("Quantidade de familiares?"));

var numero = 0;
while(numero <= totalFamiliares) {

    var idade = parseInt(prompt("Informe idade do familiar"));
}

</script>
```

Supondo que o total de familiares seja `3`, e que já temos uma leitura, teremos `var numero = 1`:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var totalFamiliares = parseInt(prompt("Quantidade de familiares?"));

var numero = 1;
while(numero <= totalFamiliares) {

    var idade = parseInt(prompt("Informe idade do familiar"));
}

</script>
```

Enquanto `1` for igual ou menor a `3`, será feita a pergunta. Temos que incrementar `numero` para que, ao ultrapassar `3`, parem de ser feitas perguntas. Ao final, imprimiremos a palavra `FIM`:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var totalFamiliares = parseInt(prompt("Quantidade de familiares?"));

var numero = 1;
while(numero <= totalFamiliares) {
    var idade = parseInt(prompt("Informe idade do familiar"));
    numero++;
}

mostra("FIM");

</script>
```

Assim, temos que para um determinado número de familiares será feita uma determinada quantidade de perguntas. Se tivermos `10` familiares, faremos `10` perguntas. Salvaremos o programa e recarregaremos a página. Isto fará com que surja o primeiro pop up, solicitando o número de familiares. Digitaremos `3`, de modo que deverão ser feitas `3` perguntas.

O próximo pop up surgirá, solicitando a idade do familiar, e digitaremos `10`. Surgirá um novo pop up, em que digitaremos `20`, e por último, digitaremos `30`. Ao pressionarmos "Ok" neste último pop up, não deverão surgir mais pop ups.

O programa funcionou, e após perguntar a quantidade de familiares e a idade destes, o programa exibiu `FIM` na tela. Conseguimos configurar as perguntas, precisamos em seguida programar o cálculo da média das idades. Este cálculo envolverá a soma de todas as idades inseridas. Criaremos uma variável chamada `totalIdades`, que iniciará em `0`:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var totalFamiliares = parseInt(prompt("Quantidade de familiares?"));

var numero = 1;
while(numero <= totalFamiliares) {
var totalIdades = 0;
    var idade = parseInt(prompt("Informe idade do familiar"));
    totalIdades = totalIdades + idade;
    numero++;

}

mostra("FIM");

</script>
```

Leremos a idade do usuário, e declararemos que `totalIdades` receberá `totalIdades + idade`. A ideia é guardarmos todas as idades em `totalIdades`, a qual deverá acumular todos os números inseridos. Em seguida, criaremos a variável `mediaDasIdades`, que recebe o `totalIdades` dividido pela quantidade de familiares, ou seja, `totalFamiliares`:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var totalFamiliares = parseInt(prompt("Quantidade de familiares?"));

var numero = 1;
while(numero <= totalFamiliares) {
var totalIdades = 0;
    var idade = parseInt(prompt("Informe idade do familiar"));
    totalIdades = totalIdades + idade;
    numero++;

}
var mediaDasIdades = totalIdades/totalFamiliares
mostra("FIM");
</script>
```

Ao final, imprimiremos uma mensagem "A média das idades dos familiares é", concatenada à `mediaDasIdades`:

```xml
<script>

function pulaLinha() {

    document.write("<br>");
    document.write("<br>");

}

function mostra(frase) {

    document.write(frase);
    pulaLinha();

}

var totalFamiliares = parseInt(prompt("Quantidade de familiares?"));

var numero = 1;
while(numero <= totalFamiliares) {
var totalIdades = 0;
    var idade = parseInt(prompt("Informe idade do familiar"));
    totalIdades = totalIdades + idade;
    numero++;

}
var mediaDasIdades = totalIdades/totalFamiliares
mostra("A média das idades dos familiares é " + mediaDasIdades);
mostra("FIM");
</script>
```

Salvaremos e recarregaremos a página. Digitaremos uma quantidade de familiares igual a `3`, e, em seguida, as respectivas idades: `10`, `20` e `30`. Obteremos o seguinte resultado:

```css
A média das idades dos familiares é 10

FIM
```

A média deveria ter resultado em `20`, portanto, não deu certo.

Como a inicialização do `totalIdades` está inserida no `while()`, todas as vezes que o `while()` for inicializado, a variável `totalIdades` será zerada, pois recebe `0`. Assim, não serão somadas as idades, mas sim consideradas individualmente, até que o `totalIdades` receba somente o último valor a ser inserido, que no caso foi `30`. Como havia `3` indivíduos, a divisão é `30/3`, cujo resultado é `10`.

Para solucionarmos isso, a inicialização da variável `totalIdades` não pode estar dentro do `while()`, pois este rodará várias vezes e, se em cada uma delas for zerado o valor, nada será acumulado. Salvaremos o programa e recarregaremos a página. Digitaremos `3` familiares, e as idades `10`, `20` e `30`. Obteremos o seguinte resultado:

```css
A média das idades dos familiares é 20
```

Este processo, no qual precisamos acumular um valor durante uma repetição, é bastante comum. Podemos, por exemplo, utilizá-lo para calcular os salários de todos os funcionários de uma empresa.