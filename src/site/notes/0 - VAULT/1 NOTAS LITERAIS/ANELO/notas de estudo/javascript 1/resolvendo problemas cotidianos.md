---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/resolvendo-problemas-cotidianos/","tags":["javascript"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# resolvendo problemas cotidianos

## criado em: 
-  22-03-2023 - 10:59

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/Funções em javascript\|Funções em javascript]]
- tags: #javascript 
- Fontes & Links: [alura](https://cursos.alura.com.br/course/logica-programacao-javascript-html/task/17704)

---

# Calculando IMC

Nesta parte do curso aprenderemos a criar programas com mais utilidades, e veremos como é possível calcular nosso **IMC (Índice de Massa Corporal)**. No menu superior, selecionaremos "File > Save As...", e escolheremos outro nome, já que se trata de um novo programa. Chamaremos de `imc.html`.

Manteremos para este programa somente as funções `pulaLinha()` e `mostra()`:

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

Todo programa que criarmos a partir de agora terá esta estrutura mínima, para podermos aproveitar o que já foi feito. O cálculo do IMC, segundo a Organização Mundial da Saúde, é composto pelo peso divido pela altura multiplicado pela altura. Portanto, criaremos uma variável chamada `pesoFlavio`, e outra, `alturaFlavio`:

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

var pesoFlavio = 73;
var alturaFlavio = 1.71;

</script>
```

Partiremos agora para o cálculo do IMC. Criaremos uma variável chamada `imcFlavio`, que receberá a divisão entre `pesoFlavio` e `alturaFlavio` multiplicada pela `alturaFlavio`:

```csharp
var pesoFlavio = 73;
var alturaFlavio = 1.71;

var imcFlavio = pesoFlavio / alturaFlavio * alturaFlavio
```

Se deixarmos como está, teremos um problema. Isso porque ele considerará a divisão antes de realizar a multiplicação. Para evitarmos isso, isolaremos a operação de multiplicação com parênteses:

```csharp
var pesoFlavio = 73;
var alturaFlavio = 1.71;

var imcFlavio = pesoFlavio / (alturaFlavio * alturaFlavio);
```

Com o resultado do IMC, utilizaremos a função `mostra()` para imprimi-lo na tela:

```csharp
var pesoFlavio = 73;
var alturaFlavio = 1.71;

var imcFlavio = pesoFlavio / (alturaFlavio * alturaFlavio);

mostra("O imc do Flávio é " + imcFlavio);
```

Salvaremos e retornaremos ao navegador. Abriremos este novo programa que acabou de ser criado, selecionando "Arquivo > Abrir arquivo..." na barra de menu superior, e escolhendo o arquivo `imc.html`.

Ao ser executado, o programa exibe o seguinte resultado:

```bash
O imc do Flávio é 24.9649647925858
```

Não vamos nos preocupar por enquanto em arredondar este resultado. Queremos calcular também o IMC de um amigo, portanto criaremos uma variável `pesoAmigo`, e outra, `alturaAmigo`:

```csharp
var pesoFlavio = 73;
var alturaFlavio = 1.71;
var imcFlavio = pesoFlavio / (alturaFlavio * alturaFlavio);
mostra("O imc do Flávio é " + imcFlavio);

var pesoAmigo = 68;
var alturaAmigo = 1.72;
```

Em seguida, criaremos a variável `imcAmigo` calculando da mesma forma como fizemos anteriormente:

```csharp
var pesoFlavio = 73;
var alturaFlavio = 1.71;
var imcFlavio = pesoFlavio / (alturaFlavio * alturaFlavio);
mostra("O imc do Flávio é " + imcFlavio);

var pesoAmigo = 68;
var alturaAmigo = 1.72;
var imcAmigo = pesoAmigo / (alturaAmigo * alturaAmigo);
```

Por fim, utilizaremos a função `mostra()` para que esta informação seja impressa:

```csharp
var pesoFlavio = 73;
var alturaFlavio = 1.71;
var imcFlavio = pesoFlavio / (alturaFlavio * alturaFlavio);
mostra("O imc do Flávio é " + imcFlavio);

var pesoAmigo = 68;
var alturaAmigo = 1.72;
var imcAmigo = pesoAmigo / (alturaAmigo * alturaAmigo);
mostra("O imc do meu amigo é " + imcAmigo); 
```

Salvaremos, retornaremos ao navegador e recarregaremos a página. Obteremos o seguinte resultado:

```bash
O imc do Flávio é 24.9649647925858

O imc do meu amigo é 22.985397512168742
```

O que significam estes IMCs? São resultados bons ou ruins? Veremos isso adiante. Precisamos observar que, tanto no cálculo do `imcFlavio` quanto do `imcAmigo` é utilizada a mesma fórmula matemática, o mesmo cálculo. E se outro programador quiser calcular o IMC, digamos, da sua tia? Serão criadas as variáveis:

```csharp
var pesoTia = 50;
var alturaTia = 1.62;
```

Ele terá que saber a fórmula para calcular o IMC, que é o peso dividido pela altura, multiplicada pela altura. Assim, será repetida a aplicação do cálculo de IMC já utilizada por duas vezes no programa.

Suponhamos que o cálculo do IMC é eventualmente alterado pela Organização Mundial da Saúde, assim, teremos que lembrar de todos os lugares em que o cálculo aparece. Resolveremos este problema criando uma função chamada `calculaImc()`:

```csharp
function calculaImc() {

}

var pesoFlavio = 73;
var alturaFlavio = 1.71;
var imcFlavio = pesoFlavio / (alturaFlavio * alturaFlavio);
mostra("O imc do Flávio é " + imcFlavio);

var pesoAmigo = 68;
var alturaAmigo = 1.72;
var imcAmigo = pesoAmigo / (alturaAmigo * alturaAmigo);
mostra("O imc do meu amigo é " + imcAmigo);
```

Lembrando que, para criar uma função, precisamos utilizar o `function` mais o nome, os parênteses e as chaves.

Não há necessidade de colocarmos o ponto e vírgula (**`;`**) após fecharmos a chave (**`}`**), pois o JavaScript já entende que o final de um bloco indica o final de uma instrução. Copiaremos a linha que conta com o cálculo e inseriremos no bloco da instrução:

```csharp
function calculaImc() {

var imcFlavio = pesoFlavio / (alturaFlavio * alturaFlavio);

}
```

Como queremos que a mesma função sirva para várias pessoas, em vez de utilizarmos os nomes dos indivíduos nas variáveis, manteremos somente o que cada uma representa:

```csharp
function calculaImc() {

var imc = peso / (altura* altura);

}
```

Em seguida, removeremos as linhas de código em que temos o cálculo do IMC:

```csharp
function calculaImc() {

var imc = peso / (altura* altura);

}

var pesoFlavio = 73;
var alturaFlavio = 1.71;

var pesoAmigo = 68;
var alturaAmigo = 1.72;
```

Em seu lugar, chamaremos a função `calculaImc()`:

```csharp
function calculaImc() {

var imc = peso / (altura* altura);

}

var pesoFlavio = 73;
var alturaFlavio = 1.71;
calculaImc();

var pesoAmigo = 68;
var alturaAmigo = 1.72;
calculaImc();
```

Falta passarmos para a função os valores que ela deverá considerar na hora de fazer os cálculos:

```csharp
function calculaImc() {

var imc = peso / (altura* altura);

}

var pesoFlavio = 73;
var alturaFlavio = 1.71;
calculaImc(pesoFlavio, alturaFlavio);

var pesoAmigo = 68;
var alturaAmigo = 1.72;
calculaImc(pesoAmigo, alturaAmigo);
```

Sabemos que, na programação, ao adotarmos o `pesoFlavio`, estamos nos referindo ao valor `73`, da variável, e o mesmo acontecerá para todos os demais. Para simplificar, inseriremos os números diretamente:

```csharp
function calculaImc() {

var imc = peso / (altura* altura);

}

var pesoFlavio = 73;
var alturaFlavio = 1.71;
calculaImc(73, 1.71);

var pesoAmigo = 68;
var alturaAmigo = 1.72;
calculaImc(68, 1.72);
```

Deste modo, temos que o primeiro `calculaImc()` recebe como parâmetros, respectivamente, `73` e `1.71`, e o mesmo para o segundo `calculaImc()`:

```csharp
function calculaImc() {

var imc = peso / (altura* altura);

}


calculaImc(73, 1.71);
calculaImc(68, 1.72);
```

Salvaremos, retornaremos ao navegador e recarregaremos a página. Veremos que nada é exibido, e isto acontece porque não preparamos a função `calculaImc()` para receber dois parâmetros. Temos que indicar que os parâmetro serão `x, y`:

```javascript
function calculaImc(x, y) {

var imc = peso / (altura* altura);

}


calculaImc(73, 1.71);
calculaImc(68, 1.72);
```

Para não nos confundirmos e deixarmos mais clara a informação a qual cada valor corresponde, em vez de `x` e `y`, utilizaremos `altura` e `peso`:

```javascript
function calculaImc(altura, peso) {

var imc = peso / (altura* altura);

}


calculaImc(1.71, 73);
calculaImc(1.72, 68);
```

Ao chamarmos o `calculaImc()`, o `1.71` será passado para `altura`, e `73` para o `peso`. Assim, o IMC será calculado com base nos valores dos parâmetros. Para que os resultados sejam exibidos, incluiremos a instrução `mostra()` em nossa função:

```javascript
function calculaImc(altura, peso) {

    var imc = peso / (altura * altura);
    mostra("O imc calculado é " + imc);
}
```

Salvaremos e recarregaremos a página, e o resultado obtido é exibido na tela:

```undefined
O imc calculado é 24.9649647925858

O imc calculado é 22.985397512168742
```

Em vez de espalharmos a fórmula do cálculo do IMC, criamos uma funcionalidade que está preparada - se passarmos primeiro a altura, e depois o peso - para calcular o IMC, e exibir o valor, por meio da função `mostra()`. Se a fórmula for alterada, o IMC é calculado pelo método antigo, `+ 1`:

```javascript
function calculaImc(altura, peso) {

    var imc = peso / (altura * altura) +1;
    mostra("O imc calculado é " + imc);
}
```

Só precisaremos alterar a função, não todos os pontos em que ela é chamada. Nesta aula, trabalhamos com conceitos já conhecidos, entretanto estamos lidando com uma função que possui dois parâmetros.