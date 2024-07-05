---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/funcao-dentro-da-funcao/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# função dentro da função

## criado em: 
-  22-03-2023 - 10:08

### Conteúdo Relacionado
- notas: 
- tags: 
- Fontes & Links: 

---

Já simplificamos a maneira de pular linhas criando a função `pulaLinha()`. Será que é possível fazermos o mesmo com o `document.write()`? Quando queremos exibir algo para o usuário, sempre temos que escrevê-lo, incluindo também a mensagem entre parênteses, como em:

```javascript
document.write("Olá pessoal!");
```

É uma sintaxe extensa. Em vez de escrevermos tudo isso, criaremos uma função chamada `mostra()`. Quem mostra, **mostra algo**, portanto esta função receberá uma mensagem como parâmetro, em vez de nenhum. Se compararmos as instruções:

```javascript
document.write("Olá pessoal!");

mostra("Olá pessoal");
```

Vemos que a segunda, além de mais sucinta, fica explícita nossa intenção de mostrar algo. Quando um terceiro olhar nosso código, ao ver `mostra()`, saberá que seu propósito é exibir algo na tela.

E como criamos a função `mostra()`? Primeiro colocaremos alguns trechos em comentários, por meio de barras duplas (`//`). O programa ignorará a referida linha, que continuará presente para fins didáticos, para lembrarmos o que havia antes.

```lua
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");

}

var ano = 2016;

// document.write("Flávio tem " + (ano - 1977) + " anos");

pulaLinha();

// document.write("Joaquim tem " + (ano - 1996) + " anos");

pulaLinha();

ano = 2017;

// document.write("Barney tem " + (ano - 1976) + " anos");
// document.write("Olá pessoal!");

</script>
```

No lugar de `document.write()` queremos utilizar `mostra()`:

```lua
var ano = 2016;

// document.write("Flávio tem " + (ano - 1977) + " anos");

mostra();

pulaLinha();

// document.write("Joaquim tem " + (ano - 1996) + " anos");

pulaLinha();

ano = 2017;

// document.write("Barney tem " + (ano - 1976) + " anos");
// document.write("Olá pessoal!");

</script>
```

Com isto queremos que seja exibido o resultado da concatenação:

```javascript
document.write("Flávio tem " + (ano - 1977) + " anos");
```

O mesmo para todas as concatenações presentes no programa:

```lua
var ano = 2016;

// document.write("Flávio tem " + (ano - 1977) + " anos");

mostra("Flávio tem " + (ano - 1977) + " anos");

pulaLinha();

// document.write("Joaquim tem " + (ano - 1996) + " anos");

mostra("Joaquim tem " + (ano - 1996) + " anos");

pulaLinha();

ano = 2017;

// document.write("Barney tem " + (ano - 1976) + " anos");

mostra("Barney tem " + (ano - 1976) + " anos");

// document.write("Olá pessoal!");

mostra("Olá pessoal!");

</script>
```

Entretanto, a função `mostra()` não existe. Apagaremos os comentários apenas para diminuir a poluição visual:

```bash
var ano = 2016;

mostra("Flávio tem " + (ano - 1977) + " anos");

pulaLinha();

mostra("Joaquim tem " + (ano - 1996) + " anos");

pulaLinha();

ano = 2017;

mostra("Barney tem " + (ano - 1976) + " anos");

mostra("Olá pessoal!");

</script>
```

Nosso objetivo é que `mostra()` faça `document.write()`, que por sua vez recebe o que queremos exibir. O importante é que toda função seja declarada no início do arquivo, não importa se antes ou depois de `pulaLinha()`. Primeiro declararemos a função e o nome:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");

}

function mostra() {

}

var ano = 2016;
```

Em seguida, determinaremos o que ela fará:

```javascript
function mostra() {

    document.write("Olá");

}
```

No programa, estamos passando diferentes concatenações para que a função `mostra()` exiba, mas o que será realmente exibido? Faremos um teste. Salvaremos o programa, retornaremos ao navegador e recarregaremos o programa. Obtivemos o seguinte:

```css
Olá

Olá

OláOlá
```

Ou seja, o programa ignorou completamente o que havíamos passado para ser exibido, o parâmetro, e está exibindo somente `Olá`. Precisamos descobrir uma forma de os parâmetros serem transmitidos para o `document.write()` presente na construção da função. Como faremos isso?

Temos os parênteses obrigatórios após o nome da função:

```csharp
function mostra() {
}
```

Escolheremos um nome aleatório para inserir, por exemplo `ronaldo`. Quando `mostra()` receber um parâmetro, ele será enviado para dentro da variável `ronaldo`. Ao chegar nessa instrução, o JS interpretará como se `ronaldo` fosse igual à frase que queremos exibir.

O parâmetro da função é considerado como se fosse uma variável. No caso, `ronaldo` recebe o que está sendo passado no programa, em `mostra()`. No caso do `Olá pessoal!`, ele exibirá este texto. Tendo definido o parâmetro da função, em `document.write()`, o incluiremos como parâmetro também:

```javascript
function mostra(ronaldo) {

    document.write(ronaldo);

}
```

Será que funciona? Salvaremos e recarregaremos a página:

```undefined
Flávio tem 39 anos

Joaquim tem 20 anos

Barney tem 41 anosOlá pessoal!
```

Deu certo! As frases foram exibidas.

Aprendemos a criar uma função, mas desta vez estamos criando uma que recebe um parâmetro. Se quisermos que a função receba algo, precisaremos indicar isto incluindo um nome. Nós escolhemos `ronaldo`, mas para que fique mais claro, mudaremos para `frase`:

```javascript
function mostra(frase) {

    document.write(frase);

}
```

Ao chamar a função `mostra()`, o JavaScript pegará o resultado da concatenação e interpretará como se `frase` fosse igual a isto. Por exemplo:

```scss
function mostra(frase) {

    document.write(frase);

}

mostra("Olá pessoal!");
```

Para o JavaScript, `frase` será igual a `Olá pessoal!`, e com isso conseguimos passar parâmetros para uma função. Será que é possível simplificar ainda mais nosso código? Toda vez que imprimimos uma frase, queremos pular uma linha:

```xml
<script>
    function pulaLinha() {

    document.write("<br>");
    document.write("<br>");
        }

    function mostra(frase ){

    document.write(frase);
        }

    mostra("Olá pessoal!");

    var ano = 2016;

    mostra("Flávio tem " + (ano - 1977) + " anos");

    pulaLinha();

    mostra("Joaquim tem " + (ano - 1996) + " anos");

    pulaLinha();

    ano = 2017;

    mostra("Barney tem " + (ano - 1976) + " anos");

</script>
```

Exceto pela última linha, que não pularemos. Removeremos a mensagem `Olá pessoal!`, bem como `pulaLinha()`, que não será inserido entre as frases. Recarregaremos a página, e temos o seguinte resultado:

```undefined
Flávio tem 39 anosJoaquim tem 20 anosBarney tem 41 anos
```

Nenhuma linha foi pulada. Para tornar isso mais simples, incluiremos a função `pulaLinha()` em `mostra()`:

```scss
function mostra(frase) {

    document.write(frase);
    pulaLinha();
}
```

Agora, a função `mostra()` conta com duas instruções. Quando a chamamos, será feito o `document.write()`, exibindo-se o parâmetro, e na próxima instrução será pulada uma linha. Uma função pode ter como instrução a chamada de outra função. Salvaremos, e recarregaremos a página. Obteremos o resultado desejado:

```undefined
Flávio tem 39 anos

Joaquim tem 20 anos

Barney tem 41 anos
```

Se compararmos este código com o anterior, ele está mais claro. Não precisamos escrever `document.write()` diversas vezes, nem pular linhas em várias ocasiões. Guardamos a complexidade de pular linhas em uma única função:

```javascript
function pulaLinha() {
    document.write("<br>");
    document.write("<br>");

}
```

E o código responsável por exibir as informações para o usuário estará em outra:

```scss
function mostra(frase) {

    document.write(frase);
    pulaLinha();
}
```

A diferença entre elas é que, apesar de ambas possuírem duas instruções, a primeira não recebe um parâmetro, enquanto a segunda o faz. O que acontece se inserirmos `mostra()` sem nenhum parâmetro em nosso código?

```csharp
var ano = 2016;

mostra();
```

Vamos inserir, salvar o programa e recarregar o navegador. Obteremos o seguinte resultado:

```javascript
undefined

Flávio tem 39 anos

Joaquim tem 20 anos

Barney tem 41 anos
```

Não ocorre erro, mas é exibida a mensagem `undefined`, ou seja, "indefinido". Isso porque ao chamarmos a função e não passarmos um parâmetro, temos um valor de `frase` indefinido. Se passarmos um valor qualquer, como `Calopsita!`:

```csharp
var ano = 2016;

mostra("Calopsita!");
```

E recarregarmos o navegador, veremos o seguinte resultado:

```undefined
Calopsita!

Flávio tem 39 anos

Joaquim tem 20 anos

Barney tem 41 anos
```

Portanto, o que acabamos de fazer é o estopim para começarmos a criar aplicações mais úteis, dar forma a programas mais elaborados. Se dominamos o conceito de função, tudo é mais fácil no mundo da programação.