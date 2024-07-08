---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/resumo-var/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# resumo var

## criado em: 
-  21-03-2023 - 13:56

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/hoisted var\|hoisted var]]
- tags: 
- Fontes & Links: 

---

Aprendemos a trabalhar com variáveis, que nos facilitam a manutenção de nosso programa, e o tornam mais dinâmico.

Por exemplo, para o ano, em vez de termos o número fixo no comando, cujas alterações posteriores teriam que ser feitas manualmente em todos os locais em que ele aparece, declaramos uma variável que guarda um valor, no caso `2016`. Para isso, utilizamos o prefixo `var`, abreviação de _variable_, em seguida nomeamos a variável como `ano`. Além disso, utilizamos o sinal de **`=`**, que lemos como "recebe". Portanto, a variável `ano` recebe `2016`:

```csharp
var ano = 2016
```

Ao lermos esta instrução, fica claro que a variável `ano` recebe `2016`. Assim, em todo o lugar em que esta variável for acessada, o JS "pegará" o seu valor naquele momento. Quando o código do trecho abaixo for executado, a primeira linha a ser processada é a declaração da variável. Em seguida, ele imprimirá a linha do `document.write()` com a idade do Flávio, que é uma série de concatenações:

```xml
<meta charset="UTF-8">

<script>

var ano = 2016;
   document.write("Flávio tem " + (ano - 1977) + " anos");
   document.write("<br>");
   document.write("Joaquim tem " + (ano - 1996) + " anos" );
   document.write("<br>");
//...
```

No momento em que o código for executado, será analisado o valor da variável `ano` até este ponto, no caso, `2016`. Este valor será impresso até atingir a linha em que a variável `ano` recebe o valor `2017`. Por definição, os valores da variável mudam, e podem ser alterados em diversos pontos ao longo do programa. Portanto, a partir da nova instrução, o valor de `ano` será `2017`:

```xml
<meta charset="UTF-8">

<script>

var ano = 2016;

document.write("Flávio tem " + (ano - 1977) + " anos");
document.write("<br>");
document.write("Joaquim tem " + (ano - 1976) + " anos");
document.write("<br>")};

ano = 2017;
document.write("Barney tem " + (ano - 1976) + " anos");
document.write("<br>");

//...
```

Não há influência sobre as instruções anteriores porque elas já foram processadas, com o valor de `ano` de `2016`. O marco de mudança do valor da variável em nosso programa é na linha `ano = 2017`. Vimos também que é possível realizar operações matemáticas, como adições e multiplicações, desde que elas guardem um número. Podemos guardar em uma variável, por exemplo, informações de idade:

```csharp
var idadeFlavio = 39;
var idadeJoaquim = 20;
var idadeBarney = 41;
```

Quando compreendemos rapidamente a que o nome de uma variável se refere, sendo simples entender quais valores ela guarda, facilitamos o trabalho dos próximos programadores que alterarão o nosso código. E se tivéssemos colocado apenas uma letra como o nome da variável? Por exemplo:

```csharp
var x = 39;
var y = 20;
var z = 41;
```

Seria difícil identificar o que cada número significa, por isso a importância de conferirmos um nome e deixar claro que tipo de valor aquela determinada variável armazena. Inclusive, podemos realizar operações matemáticas utilizando os nomes das variáveis, e guardar seu resultado em outra variável:

```csharp
var idadeFlavio = 39;
var idadeJoaquim = 20;
var idadeBarney = 41;

var media = (idadeFlavio + idadeJoaquim + idadeBarney)/3;
```

Uma variável não guarda só um tipo texto (`string`), mas também um tipo número, e outros que aprenderemos no decorrer do curso. Não deixem de fazer os exercícios, e continuaremos a seguir!