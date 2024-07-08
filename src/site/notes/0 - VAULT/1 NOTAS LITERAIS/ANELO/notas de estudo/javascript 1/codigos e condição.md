---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/codigos-e-condicao/","tags":["javascript"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# codigos e condição

## criado em: 
-  22-03-2023 - 15:09

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/condicionando\|condicionando]]
- tags: #javascript 
- Fontes & Links: 

---

Nesta aula, aprenderemos a resolver um novo tipo de problema. Com o programa `imc.html` aberto, selecionaremos as opções "File > Save as..." e salvaremos como `futebol.html`. Como trataremos de futebol, removeremos as partes do código relacionadas ao cálculo do IMC, e manteremos o seguinte:

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

Nosso objetivo será perguntar ao usuário o número de vitórias e empates do seu time. Se você não gostar de futebol, pode inserir números aleatórios. Criaremos uma variável `vitorias` que receberá um `prompt()`:

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

var vitorias = prompt();

</script>
```

Temos que fazer uma pergunta ao usuário, no caso, utilizaremos "Entre com o número de vitórias":

```csharp
var vitorias = prompt("Entre com o número de vitórias");
```

A próxima variável se chamará `empates`, e a pergunta será "Entre com o número de empates":

```csharp
var vitorias = prompt("Entre com o número de vitórias.");
var empates = prompt("Entre com o número de empates.");
```

Salvaremos, e retornaremos ao navegador. Temos que abrir este novo arquivo e, para isso, selecionaremos "Arquivo > Abrir arquivo...> futebol.html". Quando o carregarmos, surgirá um pop up com a mensagem:

> Esta página diz: Entre com o número de vitórias.

Digitaremos o número `15` e pressionaremos "Ok". Em seguida, surge um novo pop up com a seguinte mensagem:

> Essa página diz: Enter com o número de empates.

Digitaremos `2` e pressionaremos "Ok". Nada acontece, pois ainda não inserimos nenhuma instrução sobre o que fazer com estes números. Com o número de vitórias e empates, calcularemos a quantidade de pontos de cada time. Uma vitória vale `3` (três) pontos, e um empate, `1` (um) ponto. Portanto, multiplicaremos a quantidade de vitórias por `3` e somaremos este resultado ao número de empates.

Criaremos uma variável `pontos`, que receberá a operação matemática descrita acima:

```csharp
var vitorias = prompt("Entre com o número de vitórias.");
var empates = prompt("Entre com o número de empates.");

var pontos = vitorias  * 3 + empates;
```

Será que precisamos de parênteses? Não, pois a multiplicação será considerada em primeiro lugar, para posteriormente ser somada ao número de empates. Entretanto, é possível utilizarmos os parênteses se desejarmos deixar a equação mais clara. Em seguida, imprimiremos "Os pontos do seu time são ", concatenado com `pontos`:

```csharp
var vitorias = prompt("Entre com o número de vitórias.");
var empates = prompt("Entre com o número de empates.");

var pontos = vitorias  * 3 + empates;

mostra("Os pontos do seu time são " + pontos);
```

Salvaremos, retornaremos ao navegador, recarregaremos a página, e digitaremos `3`, para o número de vitórias, e `1` para o número de empates. Dessa forma, esperamos que o total de pontos seja `10`. Obtivemos o seguinte resultado:

> Os pontos do seu time são 91

Observamos que mesmo incluindo os parênteses e isolando a operação de multiplicação, o resultado seria o mesmo. O `return` da função `prompt()` - que não foi criada por nós, e é do JavaScript -, sempre retorna como texto, não como número.

Por que isso funcionou para nosso cálculo de IMC, e não está funcionando agora? Vamos criar um `alert()` para somar o número de vitórias com `10`:

```csharp
var vitorias = prompt("Entre com o número de vitórias.");
alert(vitorias + 10);

var empates = prompt("Entre com o número de empates.");

var pontos = vitorias  * 3 + empates;

mostra("Os pontos do seu time são " + pontos);
```

O número de vitórias será interpretado como um texto, então, ao recarregarmos a página e digitarmos `5`, ao ser somado ao número `10`, ocorrerá uma concatenação cujo resultado deve ser `510`. Salvaremos o programa e recarregaremos a página.

Digitaremos `5` para o número de vitórias e pressionaremos "Ok". Conforme esperado, obteremos o seguinte resultado:

> Essa página diz: 510

Sempre que usamos o `prompt()`, o conteúdo é lido como um texto. E se multiplicarmos um texto por um número?

```csharp
var vitorias = prompt("Entre com o número de vitórias.");

alert(vitorias * 3);
```

Salvaremos e recarregaremos a página. Digitaremos `5` como o número de vitórias e pressionaremos "Ok". Teremos:

> Essa página diz: 15

Funcionou!

Isso acontece por conta do JavaScript. Lemos `prompt()` sempre como um **texto**. Se no texto houver um número e fizermos uma operação de multiplicação ou divisão, o JavaScript converte o texto para **número**, e é por isso que a multiplicação funciona.

Por definição, não pode haver multiplicação de um texto com um número, portanto, se digitarmos, por exemplo, "Flávio" no pop up, não será possível realizar a operação, o resultado será `NaN`, algo inválido.

Retornando ao nosso programa:

```csharp
var vitorias = prompt("Entre com o número de vitórias.");

var empates = prompt("Entre com o número de empates.");

var pontos = vitorias  * 3 + empates;

mostra("Os pontos do seu time são " + pontos);
```

Ao chegar na variável `pontos`, a primeira parte da equação está correta e o JavaScript multiplica o número de vitórias por `3`. A seguir, ele tentará concatená-lo com `empates`, mas nesse caso não há conversão, já que ao digitarmos o número de empates ele é interpretado como uma string.

Assim, teríamos `9` - resultado da multiplicação do número de vitórias por `3` - somado ao `1`, que é interpretado como uma string. Como vimos, quando temos um número e uma string, eles são concatenados e, assim, o resultado será `91`.

Como queremos que o `prompt()` seja lido como número - e não como string -, garantiremos isso nos assegurando de que nosso cálculo funcionará.

Para esta conversão, primeiramente, veremos como é possível fazê-lo pelo console do navegador. Acessaremos "Visualizar > Desenvolvedor > Exibir o código fonte", criaremos uma variável `texto` que recebe o número `10`, e em seguida pressionaremos a tecla "Enter":

```csharp
var texto = "10"
```

Em seguida, ao escrevermos `texto` e pressionarmos "Enter", teremos o seguinte resultado:

```javascript
var texto = "10"
undefined
texto
"10"
texto
"10"
```

Este aparece entre aspas por ser um texto. Em seguida, criaremos uma variável `numero`, que recebe `parseInt()`, uma função existente no JavaScript, e preparada para receber um texto a ser convertido em número.

A função `parseInt()` terá como parâmetro a variável `texto`, que por sua vez tem no seu conteúdo uma string. Com isso, queremos que isto seja convertido para número; isto é, no caso a string `10` se tornará o número `10`:

```javascript
var texto = "10"
undefined
texto
"10"
texto
"10"
texto
"10"
var numero = parseInt(texto);
```

Pressionaremos "Enter" e, em seguida, digitaremos "texto" e apertaremos em "Enter" novamente:

```javascript
var texto = "10"
undefined
texto
"10"
texto
"10"
texto
"10"
var numero = parseInt(texto);
undefined
texto
"10"
```

Ao digitarmos `numero` e pressionarmos "Enter", acontecerá o seguinte:

```javascript
var texto = "10"
undefined
texto
"10"
texto
"10"
texto
"10"
var numero = parseInt(texto);
undefined
texto
"10"
numero
10
```

Ou seja, por não estar entre aspas, o valor foi convertido. O que **não** podemos fazer é o seguinte:

```javascript
var numero = parseInt("Flavio");
```

A conversão não será feita, já que `Flavio` não é um número. Neste caso, o resultado será:

```javascript
var numero = parseInt("Flavio");
undefined
numero
NaN
```

Foi exibida a mensagem `NaN`, que significa "não é um número". Retornaremos ao nosso código no editor de textos. Para convertermos o retorno do `prompt()`, o passaremos diretamente para `parseInt()`:

```javascript
var vitorias = parseInt(prompt("Entre com o número de vitórias."));

var empates = prompt("Entre com o número de empates.");

var pontos = vitorias  * 3 + empates;

mostra("Os pontos do seu time são " + pontos);
```

Esta função precisa receber algo para que possa transformá-lo em um número. Poderíamos passar uma string, no entanto usaremos o retorno do `prompt()`, e faremos o mesmo na variável `empates`:

```javascript
var vitorias = parseInt(prompt("Entre com o número de vitórias."));

var empates = parseInt(prompt("Entre com o número de empates."));
```

Salvaremos e recarregaremos a página no navegador. Surge o primeiro pop up solicitando o número de vitórias, e digitaremos `3`. Em seguida, digitaremos `1` para o número de empates. Obteremos o seguinte resultado:

> Os pontos do seu time são 10

Funcionou!

Importante lembrar que se quiséssemos ler um nome, por exemplo, não seria necessário utilizar a função `parseInt()`, porque neste caso queremos que isto seja considerado como texto. Sempre que formos ler uma entrada, e a intenção for trabalhar com números, temos que fazer o `parseInt()` para que o valor digitado, que por padrão é lido como texto, seja interpretado como um número.