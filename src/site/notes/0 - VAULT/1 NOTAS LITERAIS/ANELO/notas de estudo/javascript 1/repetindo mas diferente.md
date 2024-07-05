---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/repetindo-mas-diferente/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# repetindo mas diferente

## criado em: 
-  23-03-2023 - 13:57

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/acumulando valores\|acumulando valores]]
- tags: 
- Fontes & Links: 

---
Nesta aula, aprenderemos mais uma forma de utilizar repetições em nossos programas.

Desde crianças, aprendemos que a tabuada nada mais é que uma repetição... Criaremos um programa chamado `tabuada`. Com nosso programa `ano_copa` aberto, selecionaremos a opção "Salvar Como" e daremos a ele um novo nome: `tabuada.html`. Apagaremos os trechos que não lidam com a tabuada e manteremos somente as funções `pulaLinha()` e `mostra()`:

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

</script>
```

Criaremos a tabuada de **7**, que segue um mesmo padrão, o número `7` multiplicado por outro (entre `1` e `10`), ou seja, o multiplicador varia. Para isso, criaremos a variável `multiplicador`:

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

var multiplicador = 1;

</script>
```

Em seguida, usaremos `mostra()` para exibir o resultado das operações:

```csharp
var multiplicador = 1;

mostra(7 * multiplicador);
```

Retornaremos ao navegador, e abriremos o programa `tabuada.html`. É exibido para nós apenas o número `7` na tela. Entretanto, nossa intenção é que as multiplicações se repitam até o número `10`. Criaremos uma situação em que, enquanto o `multiplicador` for menor ou igual a `10`, o número `7` é multiplicado por ele:

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

var multiplicador = 1;

while(multiplicador <= 10) {

    mostra(7 * multiplicador);

}
</script>
```

Dessa forma, o JavaScript sempre entenderá o multiplicador como `1`, e precisamos criar um mecanismo que indique que este número deve crescer, até o limite estabelecido. Para isso, declararemos que `multiplicador` é igual a `multiplicador + 1`:

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

var multiplicador = 1;

while(multiplicador <= 10) {

    mostra(7 * multiplicador);
    multiplicador = multiplicador + 1
}

mostra("FIM");

</script>
```

Assim, quando o `multiplicador` atingir o limite (`10`), a condição de `while()` deixará de ser verdadeira e, então, o JavaScript poderá imprimir `FIM`. Vamos testar salvando o programa, retornando ao navegador e recarregando a página. Teremos a seguinte exibição:

```undefined
7

14

21

28

35

42

49

56

63

70

FIM
```

Funcionou como gostaríamos, temos a tabuada de 7. Existe ainda outra maneira de aplicarmos a repetição, que passaremos a estudar agora. Além do `while()`, existe o `for()`, veremos como este funciona. Primeiro, removeremos o `while()` e o substituiremos pelo `for()`, que possui uma estrutura com três espaços:

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

var multiplicador = 1;

for(espaço1; espaço2; espaço3) {

    mostra(7 * multiplicador);
    multiplicador = multiplicador + 1
}

mostra("FIM");

</script>
```

Cada um dos espaços é separado por um ponto e vírgula (`;`). Neste caso, a inicialização do multiplicador fica localizada no `espaço1`, diferentemente do `while()`, em que ficava fora:

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

for(var multiplicador = 1; espaço2; espaço3) {

    mostra(7 * multiplicador);
    multiplicador = multiplicador + 1
}

mostra("FIM");

</script>
```

No `while()`, havia uma condição para repetição - que o `multiplicador` fosse menor ou igual a `10`. Em `espaço2` do `for`, esta condição será inserida:

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

for(var multiplicador = 1; multiplicador <= 10; espaço3) {

    mostra(7 * multiplicador);
    multiplicador = multiplicador + 1
}

mostra("FIM");

</script>
```

Este pedaço do `for()` conterá a condição para o JavaScript saber se deve continuar a repetir. O terceiro espaço servirá para acrescer o multiplicador de `+ 1`. Se não fizermos isto, a condição `multiplicador <= 10` nunca será falsa.

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

for(var multiplicador = 1; multiplicador <= 10; multiplicador = multiplicador + 1) {

    mostra(7 * multiplicador);

}

mostra("FIM");

</script>
```

A estrutura do `for()` possui a mesma funcionalidade do `while()`, com a diferença de que ela é divida em três partes. A primeira é uma variável para inicializá-lo, a que será incrementada, o segundo contém a condição de repetição, a última parte do `for()` é o incremento da variável `multiplicador`, declarada no `espaço1`. Vamos salvar e recarregar a página. Teremos o mesmo resultado:

```undefined
7

14

21

28

35

42

49

56

63

70

FIM
```

Com o `while()`, o mesmo resultado é obtido da seguinte forma:

```csharp
var multiplicador = 1;

while(multiplicador <= 10) {

    mostra(7 * multiplicador);
    multiplicador = multiplicador + 1;
}
```

Na primeira linha, o `for()` deixa claro tudo o que é necessário para definir a repetição, ou seja, a variável que será incrementada, a condição que a compara com o valor e, por último, o critério de incremento da variável.

Precisaremos de uma variável a ser incrementada, pois caso contrário a condição de repetição jamais será falsa e o programa nunca parará de repetir. No `while()` ocorre o mesmo, entretanto, a inicialização da variável é externa, e o incremento da variável acontece dentro de seu bloco.

Antes de continuarmos, veremos uma prática de programação que nos permite escrever menos linhas de código. Digamos por exemplo que tenhamos uma variável chamada `total`, que recebe `0`:

```csharp
var total = 0;
```

Se quisermos incrementar este total adicionando `1` ao seu valor, temos que declarar que a variável receberá o que já tem, **mais** `1`:

```csharp
var total = 0;
total = total + 1;
```

Assim, o total valerá `1`. Se repetirmos esta operação:

```makefile
var total = 0;
total = total + 1;
total = total + 1;
```

Ele passará a valer `2`. Há um atalho para incrementarmos uma variável, sempre somando `1`. Trata-se do `total++`:

```csharp
var total = 0;
total++;
```

Esta ferramenta equivale à sintaxe:

```ini
total = total + 1;
```

É um atalho que nos permite escrever menos para realizarmos uma operação corriqueira. Portanto, substituiremos todos os `multiplicador = multiplicador + 1` por `multiplicador++`:

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

for(var multiplicador = 1; multiplicador <= 10; multiplicador++) {

    mostra(7 * multiplicador);

}

mostra("FIM");

</script>
```

Isso se chama **pós incremento**. Outra vantagem é quando trabalhamos com variáveis muito grandes. Vamos criar uma para teste, chamada `quantidadeDePalavrasDoLivroQueEuCompreiAnoPassado`:

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

for(var multiplicador = 1; multiplicador <= 10; multiplicador++) {

    mostra(7 * multiplicador);

}

mostra("FIM");

var quantidadeDePalavrasDoLivroQueEuCompreiAnoPassado = 0;

</script>
```

Se quisermos incrementar `+ 1`, teremos que utilizar novamente o nome da variável, e indicar que ela recebe ela mesma mais `1`:

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

for(var multiplicador = 1; multiplicador <= 10; multiplicador++) {

    mostra(7 * multiplicador);

}

mostra("FIM");

var quantidadeDePalavrasDoLivroQueEuCompreiAnoPassado = 0; quantidadeDePalavrasDoLivroQueEuCompreiAnoPassado = quantidadeDePalavrasDoLivroQueEuCompreiAnoPassado + 1;

</script>
```

Isto dá certo, mas podemos evitar de escrever tanto fazendo o seguinte:

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

for(var multiplicador = 1; multiplicador <= 10; multiplicador++) {

    mostra(7 * multiplicador);

}

mostra("FIM");

var quantidadeDePalavrasDoLivroQueEuCompreiAnoPassado = 0; quantidadeDePalavrasDoLivroQueEuCompreiAnoPassado++;

</script>
```

Removeremos esta variável do nosso código, já que foi criada somente para teste. Adiante, faremos melhorias nos programas que criamos até o momento.
