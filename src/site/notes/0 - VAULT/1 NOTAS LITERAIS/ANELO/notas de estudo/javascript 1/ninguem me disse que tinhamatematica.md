---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/ninguem-me-disse-que-tinhamatematica/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# ninguem me disse que tinhamatematica

## criado em: 
-  21-03-2023 - 13:49

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/resumo var\|resumo var]]
- tags: 
- Fontes & Links: 

---

Uma variável pode guardar praticamente o que você quiser: um número, uma string ou outro pedaço de código. Sabemos que é possível calcularmos a média das idades usando a frase "A média das idades é" e concatenando com a soma das idades dividida pelo número de indivíduos.

```javascript
document.write('A  media das idades é  ' + (39 + 20 + 41)/3);
```

No código, teremos o seguinte:

```xml
<meta charset="UTF-8">

<script>

    var ano = 2016;

    document.write("Flávio tem " + (ano - 1977) + " anos");
    document.write("<br>");
    document.write("Joaquim tem " + (ano - 1996) + " anos");
    document.write("<br>");

    ano = 2017;
    document.write("Barney tem " + (ano - 1976) + " anos");
    document.write("<br>");

        document.write('A média das idades é  ' + (39 + 20 + 41)/3);

</script>
```

Salvaremos e recarregaremos a página, e obteremos o seguinte resultado:

```css
Flávio tem 39 anos
Joaquim tem 20 anos
Barney tem 41 anos
A média das idades é 33,333333333333336
```

Será que há um método para que seja feita a divisão em uma variável, antes de ser inserida em `write()`? Por exemplo:

```javascript
document.write('A média das idades é ' + media);
```

Sim, basta declararmos a variável `media` que contenha justamente a média das idades (a soma das idades dividida por `3`):

```csharp
var media = (39 + 20 + 41)/3;
```

Com isso, podemos fazer a substituição da operação pela variável, como no exemplo a seguir:

```javascript
var media = (39 + 20 + 41)/3;

document.write('A média das idades é ' + media);
```

O resultado é o mesmo, porém mais legível, pois conseguimos diminuir a quantidade de parênteses em um único comando. Declaramos uma nova variável, `media`, e precisamos incluir o prefixo `var`, assim como que para qualquer outra variável, em seu primeiro uso deve ser antecedida do prefixo `var`. Se quisermos alterar seu valor posteriormente, não há necessidade de utilizarmos o prefixo novamente.

Salvaremos o programa e recarregaremos o navegador. Obtivemos o mesmo resultado. A seguir, veremos como poderemos arredondar números com muitas casas decimais. Para isto, utilizamos o `document`, só que, para arrendondarmos, não trabalharemos com o documento, e sim com a matemática, portanto é este o comando que chamaremos. Em seguida, chamaremos a função `round` (do inglês, "arredondar"):

```javascript
Math.round()
```

Como parâmetro, passaremos a `media`:

```javascript
var media = (39 + 20 + 41)/3;

document.write('A média das idades é ' + Math.round(media));
```

Com o conteúdo entre parênteses de `document.write()`, definimos o que será exibido na tela, e com `Math.round` definiremos qual valor será arredondado. Salvaremos o programa, retornaremos ao navegador e recarregaremos a página. Temos o seguinte resultado:

```css
Flávio tem 39 anos
Joaquim tem 20 anos
Barney tem 41 anos
A média das idades é 33
```

Aprendemos portanto a arredondar um número; há muitos mecanismos por trás desta operação, que desvendaremos adiante. Ao observarmos o código, vemos que não é evidente qual idade corresponde a qual indivíduo. Na operação `39 + 20 + 41` não é possível inferir qual idade pertence a quem.

Para eliminarmos esta dificuldade, criaremos as seguintes variáveis:

```csharp
var idadeFlavio = 39;
var idadeJoaquim = 20;
var idadeBarney = 41;
```

Em vez de utilizarmos os números, nossa operação ficará da seguinte forma:

```javascript
var idadeFlavio = 39;
var idadeJoaquim = 20;
var idadeBarney = 41;
var media = (idadeFlavio + idadeJoaquim + idadeBarney)/3;

document.write('A média das idades é ' + Math.round(media));
```

Assim, fica claro que a média é referente aos valores das idades de Flávio, Joaquim e Barney. Neste caso, a variável melhora a legibilidade do código, além de facilitar sua manutenção.

Uma convenção importante: o nome de uma variável sempre se iniciará com uma letra **minúscula**. Se a variável contém duas palavras, por exemplo "idade + (nome)", a próxima palavra deve ser escrita com a primeira letra **maiúscula**. Este padrão recebe o nome de **camelCase**.

E se quisermos escrever a variável inteira em letras minúsculas, mesmo que sejam duas palavras? O seu código funcionará da mesma forma, o nome da variável apenas não vai seguir a convenção do mundo da programação. Para esclarecer que as variáveis não podem guardar somente números, criaremos o seguinte trecho:

```javascript
var nome = 'Flávio';

document.write('A idade de  ' + nome + ' é ' + idadeFlavio);
```

No JavaScript, podemos utilizar tanto as aspas simples (**`'`**) quanto aspas (**`"`**). Colocaremos as aspas duplas, mesmo porque outras linguagens de programação as utilizam.

```javascript
var nome = "Flávio";

document.write("A idade de  " + nome + " é " + idadeFlavio);
```

O comando `document.write` tem como parâmetro a string `A idade de`, concatenada com a variável `nome`. O JavaScript verificará qual o conteúdo da `var nome`, no caso, `Flávio`. A junção destas duas resultara em uma única string. O resultado final desta primeira parte da concatenação será:

```bash
"A idade de Flávio ".
```

Somaremos a isto a string `"e"` e, como sabemos, se somarmos duas strings teremos uma única, representando a união destas. Assim, o resultado será:

```bash
"A idade de Flávio é".
```

Por fim, será somado à string a variável `idadeFlavio`, cujo valor é um número. Como string combinado com número resulta em outra string, teremos:

```css
"A idade de Flávio é 39.
```

Sendo assim, quando o comando abaixo for executado,

```javascript
document.write("A idade de " + nome + " é " + idadeFlavio);
```

Teremos o seguinte resultado:

```css
A idade de Flávio é 39
```

Salvaremos o programa, retornaremos ao navegador e recarregaremos a página. Obtivemos o seguinte resultado:

```css
Flávio tem 39 anos
Joaquim tem 20 anos
Barney tem 41 anos
A média das idades é 33A idade de Flávio é 39
```

Como vemos, o texto ficou agrupado ao resultado da média das idades. Podemos incluir a tag `<br>` para pular uma linha:

```javascript
document.write("<br>A idade de " + nome + " é " + idadeFlavio);
```

Ao salvarmos e recarregarmos a página, teremos o seguinte resultado:

```css
Flávio tem 39 anos
Joaquim tem 20 anos
Barney tem 41 anos
A média das idades é 33
A idade de Flávio é 39
```

Deu certo! Como escrevemos a string no código HTML, o navegador processará o pulo de linha, para então exibir o texto. Alternativamente, poderíamos ter criado o mesmo resultado com o seguinte código:

```xml
<meta charset="UTF-8">

<script>

    var ano = 2016;

    document.write("Flávio tem " + (ano - 1977) + " anos");
    document.write("<br>");
    document.write("Joaquim tem " + (ano - 1996) + " anos");
    document.write("<br>");

    ano = 2017;
    document.write("Barney tem " + (ano - 1976) + " anos");
    document.write("<br>");

        var idadeFlavio = 39;
        var idadeJoaquim = 20;
        var idadeBarney = 41;

        var media = (idadeFlavio + idadeJoaquim + idadeBarney)/3;

        document.write("A média das idades é " + Math.round(media));

        var nome = "Flávio";

        document.write("<br>");
        document.write("A idade de " + nome + " é " + idadeFlavio);

</script>
```

Salvaremos a página, retornaremos ao navegador e recarregaremos a página. O resultado permanece inalterado.