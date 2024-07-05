---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/condicionando/","tags":["javascript"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# condicionando

## criado em: 
-  22-03-2023 - 15:26

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/repetir enquanto\|repetir enquanto]]
- tags: #javascript 
- Fontes & Links: 

---

Já conseguimos ler a quantidade de vitórias do time, de empates, e calcular o total de pontos. Entretanto, nossa intenção é dotar o programa de mais inteligência. Supondo que no ano passado o total de pontos tenha sido `28`, queremos que ele seja capaz de informar se o time está pior ou melhor em relação ao ano anterior.

Faremos uma comparação do total de pontos calculado com o total de pontos do ano anterior (no caso, `28`), e teremos uma mensagem personalizada para cada tipo de situação. Utilizaremos a função `mostra()` para imprimir a frase "Seu time está melhor do que no ano passado":

```javascript
var vitorias = parseInt(prompt("Entre com o número de vitórias."));

var empates = parseInt(prompt("Entre com o número de empates."));

var pontos = (vitorias * 3) + empates;

mostra("Os pontos do seu time são " + pontos);

mostra("Seu time está melhor do que no ano passado");
```

Em seguida, inseriremos a frase "Seu time está pior do que no ano passado"):

```javascript
var vitorias = parseInt(prompt("Entre com o número de vitórias."));

var empates = parseInt(prompt("Entre com o número de empates."));

var pontos = (vitorias * 3) + empates;

mostra("Os pontos do seu time são " + pontos);

mostra("Seu time está melhor do que no ano passado");

mostra("Seu time está pior do que no ano passado");
```

Por fim, imprimiremos a frase "Seu time está igual ao ano passado!":

```javascript
var vitorias = parseInt(prompt("Entre com o número de vitórias."));

var empates = parseInt(prompt("Entre com o número de empates."));

var pontos = (vitorias * 3) + empates;

mostra("Os pontos do seu time são " + pontos);

mostra("Seu time está melhor do que no ano passado.");

mostra("Seu time está pior do que no ano passado.");

mostra("Seu time está igual ao ano passado.");
```

Salvaremos e recarregaremos a página. Digitaremos os valores referentes a `3` vitórias e `1` empate. O total de pontos é `10`, sendo que este número é inferior aos do ano anterior, que totalizaram `28`. Sendo assim, o texto que deve ser exibido é "seu time está pior do que no ano passado". Entretanto, temos a seguinte exibição:

```perl
Os pontos do seu time é 10

Seu time está melhor do que no ano passado.

Seu time está pior do que no ano passado.

Seu time está igual ao ano passado.
```

O programa ainda não tem a inteligência para saber, a partir do total de pontos, qual das mensagens deve exibir. Pensando na construção das frases, só poderemos mostrar a frase que indica que o time está melhor que no ano passado se o total de pontos neste ano for maior que `28`. Portanto, teremos a seguinte construção:

```scss
se pontos maior 28
    mostra("Seu time está melhor do que no ano passado.");

mostra("Seu time está pior do que no ano passado.");

mostra("Seu time está igual ao ano passado.");
```

E assim por diante para as demais frases:

```scss
se pontos maior 28
    mostra("Seu time está melhor do que no ano passado.");

se pontos menor 28
    mostra("Seu time está pior do que no ano passado.");

se pontos igual 28
    mostra("Seu time está igual ao ano passado.");
```

Se calcularmos `12` pontos, por exemplo, teremos que verificar em primeiro lugar se este resultado é maior que `28`. Não sendo, passamos para a próxima frase, que avalia se os pontos são um número menor que `28` (e no caso, são), assim, a mensagem exibida será "seu time está pior do que no ano passado".

A terceira e última condição indica que os pontos permaneceram o mesmo, ou seja, `28`. Como não é esse o nosso caso, não será exibida a mensagem correspondente. Salvaremos e recarregaremos a página, e nada acontece. Abriremos o console, iremos a "Visualizar > Desenvolvedor > Console JavaScript", em que teremos a seguinte mensagem:

```javascript
Uncaught SyntaxError: Unexpected Identifier
```

Há um identificador não esperado. Ele não entendeu as frases que inserimos, pois estão em português. A primeira coisa a fazermos é trocar a palavra "se" pela sua tradução em inglês, "if":

```scss
if pontos maior 28
    mostra("Seu time está melhor do que no ano passado.");

if pontos menor 28
    mostra("Seu time está pior do que no ano passado.");

if pontos igual 28
    mostra("Seu time está igual igual ao ano passado.");
```

Em seguida, trocaremos as palavras "maior" e "menor" por seus símbolos matemáticos:

```scss
if pontos > 28
    mostra("Seu time está melhor do que no ano passado.");

if pontos < 28
    mostra("Seu time está pior do que no ano passado.");
```

No caso do "igual", o símbolo (`=`) é utilizado para indicar uma atribuição. Em muitas linguagens de programação, para testarmos uma igualdade, e para que o JavaScript saiba que queremos atribuir ou comparar algo, temos de utilizar o símbolo duas vezes (`==`). O código ficará portanto da seguinte forma:

```bash
if pontos > 28
    mostra("Seu time está melhor do que no ano passado.");

if pontos < 28
    mostra("Seu time está pior do que no ano passado.");

if pontos == 28
    mostra("Seu time está igual igual ao ano passado.");
```

Precisamos ter muito cuidado com isso; se quisermos realizar uma comparação, precisamos utilizar o símbolo de "igual" duas vezes (`==`).

Será que já funciona desse jeito?

Ainda não. O `if()` recebe o resultado da comparação entre a quantidade de pontos e o número `28`, sendo que para cada frase haverá uma resposta, verdadeira ou falsa. Isto será representado pela inclusão das operações entre parênteses:

```scss
if(pontos > 28)
    mostra("Seu time está melhor do que no ano passado.");

if(pontos < 28)
    mostra("Seu time está pior do que no ano passado.");

if(pontos == 28)
    mostra("Seu time está igual igual ao ano passado.");
```

Salvaremos tudo e recarregaremos a página. Nada é exibido, então abriremos o console do navegador, da mesma forma como fizemos anteriormente, em que digitaremos:

```csharp
var pontos = 12;
```

Pressionaremos a tecla "Enter", e surgirá a mensagem `undefined`. Em seguida, digitaremos:

```javascript
var pontos = 12;
undefined
pontos > 10
```

Apertando "Enter" de novo, surgirá a mensagem `true`:

```javascript
var pontos = 12;
undefined
pontos > 10
true
```

O resultado das operações de comparação é sempre `true` (verdadeiro), ou `false` (falso). Em seguida, digitaremos `pontos < 10`:

```javascript
var pontos = 12;
undefined
pontos > 10
true
pontos < 10
```

Pressionaremos a tecla "Enter" e teremos a resposta `false`:

```javascript
var pontos = 12;
undefined
pontos > 10
true
pontos < 10
false
```

Assim, o `if()` só exibirá o `mostra()` caso o resultado da operação entre parênteses seja `true`. Precisamos definir que o `if()` pode ter mais de uma instrução, e pode fazer mais de uma coisa. Para isso, ele deverá ter um bloco, representado pelas chaves (`{}`):

```scss
if(pontos > 28) {
    mostra("Seu time está melhor do que no ano passado.");
}
```

Se quiséssemos incluir mais de uma mensagem:

```scss
if(pontos > 28) {
    mostra("Seu time está melhor do que no ano passado.");
    mostra("Seu time está melhor do que no ano passado.");
}
```

Teríamos duas instruções dentro do bloco `if()`, e as mensagens só serão exibidas se o número de pontos for maior que `28`. Manteremos somente uma mensagem e criaremos blocos para as demais frases:

```scss
if(pontos > 28) {

    mostra("Seu time está melhor do que no ano passado.");

}

if(pontos < 28) {

    mostra("Seu time está pior do que no ano passado.");
}

if(pontos == 28) {

    mostra("Seu time está igual igual ao ano passado.");

}
```

Salvaremos e recarregaremos a página. No primeiro pop up, digitaremos `3` para o número de vitórias, e `1` para o número de empates. Teremos a seguinte exibição:

```perl
Os pontos do seu time são 10

Seu time está pior do que no ano passado.
```

Nosso programa é inteligente o suficiente para exibir **somente** a mensagem de que está pior, ignorando as demais, porque só entra no bloco do `if()` se a sua condição for verdadeira.

Faremos um novo teste. Recarregaremos a página e inseriremos um total de `10` vitórias e `2` empates, totalizando `32` pontos, o que nos trará a seguinte exibição:

```perl
Os pontos do seu time são 32

Seu time está melhor do que no ano passado.
```

Funcionou, ele entrou na condição em que a pontuação é maior que o ano passado e ignorou as demais. Recarregaremos a página para mais um teste. Inseriremos o total de `1` vitória e `25` empates, totalizando `28` pontos. Assim, teremos a seguinte exibição:

```lua
Os pontos do seu time são 28

Seu time está igual ao ano passado.
```

Agora temos um programa mais inteligente. E se ao final do código inserirmos um comando `mostra()` com a mensagem "FIM"?

```scss
if(pontos > 28) {

    mostra("Seu time está melhor do que no ano passado.");

}

if(pontos < 28) {

    mostra("Seu time está pior do que no ano passado.");
}

if(pontos == 28) {

    mostra("Seu time está igual ao ano passado.");

}

mostra("FIM");
```

Ele exibe o "FIM"? Sim, porque não há condição nenhuma para que ele seja exibido. Ao recarregarmos a página, e inserirmos `3` vitórias e `1` empate, veremos a seguinte exibição na tela:

```perl
Os pontos do seu time são 10

Seu time está pior do que no ano passado.

FIM
```

Com isso, conseguimos controlar o comportamento do programa de acordo com alguma condição. Se inserirmos `true` para todos os `if`s:

```scss
if(true) {

    mostra("Seu time está melhor do que no ano passado.");

}

if(true) {

    mostra("Seu time está pior do que no ano passado.");
}

if(true) {

    mostra("Seu time está igual ao ano passado.");

}

mostra("FIM");
```

Serão exibidas todas as mensagens. Alternativamente, se inserirmos `false`:

```scss
if(false) {

    mostra("Seu time está melhor do que no ano passado.");

}

if(false) {

    mostra("Seu time está pior do que no ano passado.");
}

if(false) {

    mostra("Seu time está igual ao ano passado.");

}

mostra("FIM");
```

Nenhuma mensagem é exibida. Por isso, temos de manter uma condição para que o programa possa trabalhar em cima dela.