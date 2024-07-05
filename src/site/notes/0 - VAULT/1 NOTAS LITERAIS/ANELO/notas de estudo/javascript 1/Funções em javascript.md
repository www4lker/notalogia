---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/funcoes-em-javascript/","tags":["javascript","logica"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Funções em javascript

## criado em: 
-  22-03-2023 - 09:45

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/função dentro da função\|função dentro da função]]
- tags: #javascript #logica
- Fontes & Links: 

---

Até aqui, resolvemos um problema de manutenção. Sempre que quisermos pular uma linha, mesmo declarando a variável `puloLinha`, usaremos `document.write(puloLinha)`. Isso é melhor em relação ao modelo anterior pois `puloLinha` pode guardar um pulo com várias linhas.

Mas se pedirmos para uma pessoa sem conhecimento em Programação nos dizer o significado da instrução `document.write()`, ela provavelmente não entenderá do que se trata. Isto ocorre por conta da falta de clareza no código.

Além disso, é tedioso para os programadores escreverem diversas vezes a mesma instrução. A utilidade de `document.write()` consiste em escrever na tela aquilo que passamos como parâmetro entre os parênteses. Por exemplo, se queremos dividir `3` por `4`:

```javascript
document.write(3/4);
```

O resultado não será um número exato, e para arredondarmos, podemos utilizar o `Math.round()`:

```javascript
document.write(Math.round(3/4));
```

O objetivo é bem definido, e queremos arredondar o resultado da operação. Portanto, vemos que o próprio `alert()` tem a função delimitada, que é justamente exibi-lo na tela. Estas funcionalidades já existem no JavaScript. E se pudéssemos criar nossa própria funcionalidade, algo que tenha uma **função** bem definida? Em JavaScript ou em qualquer outra linguagem de programação, há meios para criarmos nossas próprias funcionalidades.

A seguir, eliminaremos a variável `puloLinha`, e excluiremos também as declarações de `document.write(puloLinha)`:

```xml
<meta charset="UTF-8">

<script>

var ano = 2016;

document.write("Flávio tem " + (ano - 1977) + " anos");
?
document.write("Joaquim tem " + (ano - 1996) + " anos");
?

ano = 2017;
document.write("Barney tem " + (ano - 1976) + " anos");

</script>
```

Supondo que estamos seguindo um texto de um livro, faria sentido se o conteúdo fosse o seguinte?

```javascript
document.write("Flávio tem " + (ano - 1977) + " anos");
pulaLinha
document.write("Joaquim tem " + (ano - 1996) + " anos");
pulaLinha
```

O texto está escrito em português, se chamarmos um colega para ler a instrução, ele entenderá que a função de `pulaLinha` é de pular uma linha. O JavaScript nos permite fazer essa tarefa, criar nossas funcionalidades, ou seja, as próprias funções.

No entanto, há uma peculiaridade - quando queremos executar o `document.write`, temos que inserir o parâmetro entre parênteses, e no caso do `pulaLinha`, não haverá nenhum, então a funcionalidade simplesmente será executada. De qualquer forma, incluiremos os parênteses:

```javascript
document.write("Flávio tem " + (ano - 1977) + " anos");

pulaLinha();

document.write("Joaquim tem " + (ano - 1996) + " anos");

pulaLinha();
```

Por que isso? Retornaremos ao console do navegador, e na barra de menu superior acessaremos "Visualizar > Desenvolvedor > Console JavaScript", em que digitaremos o seguinte comando:

```scss
alert();
```

Pressionaremos a tecla "Enter", o que fará com que surja um alerta em forma de pop up, apesar de não termos inserido nenhum parâmetro. Isso porque se trata de uma funcionalidade já existente no JavaScript. Entretanto, para que ela pudesse ser executada, tivemos de utilizar os parênteses. Ela normalmente recebe um parâmetro, a mensagem que queremos exibir:

```scss
alert("olá");
```

Com isto temos o seguinte pop up:

```less
Essa página diz:

Olá
```

No caso, nossa função `pulaLinha()` não receberá nada, sendo simplesmente declarada. Sabemos que ela na verdade terá a linha com `document.write()`, utilizada anteriormente:

```javascript
document.write("<br>");
```

Como criamos uma função no JS? Convencionaremos que todas as funções que criarmos estarão nas primeiras instruções da tag `<script>`, ou seja, declararemos no início do código. Para declararmos uma função, utilizaremos o termo em inglês _function_, seguido de um nome, no caso, `pulaLinha`:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha()

//...
</script>
```

Inserimos os parênteses por ser uma exigência do JavaScript para declararmos uma função. Queremos que esta função escreva `document.write("<br>")`, portanto faremos isso dentro do bloco da função, entre chaves:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {
        }
//...
</script>
```

Tudo que estiver entre as chaves pertence à função `pulaLinha()`. Um ponto importante - a função é sempre descrita por um verbo, seja ele "pula", "grita", "comemora", ou qualquer outro, isto porque ela sempre indica uma ação a ser executada. Como `document.write()` pertencerá à função, adicionaremos-na dentro das chaves:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

 document.write("<br>");
        }
//...
</script>
```

Este código é válido, mas sempre dentro de um bloco utilizaremos a tecla "Tab":

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");

}
//...
</script>
```

Nós indentaremos o trecho de código. Trata-se de uma boa prática, uma convenção no mundo da programação - se estamos em um bloco, utilizamos "Tab" para criar um espaçamento na linha e, assim, o código ficará **indentado** e teremos uma melhor noção de hierarquia. Neste caso, saberemos que `document.write()` pertence à função `pulaLinha()`.

Verificaremos se o código está funcionando. Salvaremos, retornaremos ao navegador e recarregaremos a página. Deu certo! Obtivemos o seguinte resultado, em que foram puladas linhas entre cada frase:

```undefined
Flávio tem 39 anos
Joaquim tem 20 anos
Barney tem 41 anos
```

E se quisermos pular mais de uma linha? Podemos inserir mais de uma instrução na função, da seguinte forma:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
        }
//...
</script>
```

Uma função pode ser um atalho para várias outras instruções, por exemplo, quando `pulaLinha()` for processado, é como se o JavaScript estivesse substituindo por duas quebras de linha no formato `document.write("<br>")`, como se passássemos disso:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");

}

var ano = 2016;

document.write("Flávio tem " + (ano - 1977) + " anos");
pulaLinha();

document.write("Joaquim tem " + (ano - 1996) + " anos");

pulaLinha();

ano = 2017;
document.write("Barney tem " + (ano - 1976) + " anos");

</script>
```

Para isso:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br>");
        document.write("<br>");
    }

var ano = 2016;

document.write("Flávio tem " + (ano - 1977) + " anos");

    document.write("<br>");
    document.write("<br>");

document.write("Joaquim tem " + (ano - 1996) + " anos");

    document.write("<br>");
    document.write("<br>");

ano = 2017;
document.write("Barney tem " + (ano - 1976) + " anos");

</script>
```

Assim, é como se, ao chegar em `pulaLinha()`, o JavaScript parasse para acessar o bloco da função e executasse as funções contidas nela. Podemos criar nossas próprias funções para deixar nossa programação mais legível, interessante, e mais fácil de se manter.

Podemos reutilizar o `pulaLinha()` em qualquer lugar do sistema; se quisermos alterar a maneira como esta função é utilizada, isto não afetará o restante do código. Podemos obter o mesmo resultado com apenas uma instrução:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {

        document.write("<br><br>");
    }
//...
</script>
```

Quem chama a função `pulaLinha()` nem saberá que ela foi alterada, desde que ela funcione da mesma forma. Salvaremos e recarregaremos o navegador, e veremos que o resultado foi o mesmo:

```undefined
Flávio tem 39 anos

Joaquim tem 20 anos

Barney tem 41 anos
```

A vantagem de uma função é tornar legível a intenção do que queremos fazer. Se quisermos pular uma linha, por exemplo, criaremos o `pulaLinha()`, sempre utilizando um verbo e indicando uma ação.

Uma função representa um conjunto de instruções, e é possível ter uma, duas, cem instruções - **não há limites**. Sendo assim, será desnecessário reescrevê-las em diversos pontos no código, basta utilizarmos a função criada.

Porém, é preciso ter cuidado, pois se esquecermos de abrir e fechar os parênteses...

```javascript
var ano = 2016;

document.write("Flávio tem " + (ano - 1977) + " anos");

    pulaLinha;

document.write("Joaquim tem " + (ano - 1996) + " anos");

    pulaLinha;
```

Ao executarmos o código acima, teremos o seguinte resultado:

```undefined
Flávio tem 39 anosJoaquim tem 20 anosBarney tem 41 anos
```

As linhas não foram puladas. Se abrirmos o console, veremos que nada acontece. Isso porque, para executar a função, é necessária a utilização dos parênteses. No JavaScript a função permanece guardada, isso significa que não importa quantos comandos houverem dentro dela, eles só serão executados uma vez que forem acionados.

Se, incluirmos um alerta em nossa função, e removermos os chamados `pulaLinha()`:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {
        alert("oi");
        document.write("<br>");
        document.write("<br>");

}

var ano = 2016;

document.write("Flávio tem " + (ano - 1977) + " anos");

document.write("Joaquim tem " + (ano - 1996) + " anos");

ano = 2017;

document.write("Barney tem " + (ano - 1976) + " anos");

</script>
```

Temos três instruções. Ao salvarmos e recarregarmos a página, o alerta não será exibido, tampouco há quebras de linha. Isso ocorre pois a função não foi chamada. Se desta vez inserirmos `pulaLinha()` usando parênteses:

```xml
<meta charset="UTF-8">

<script>

    function pulaLinha() {
        alert("oi");
        document.write("<br>");
        document.write("<br>");

}

var ano = 2016;

document.write("Flávio tem " + (ano - 1977) + " anos");

pulaLinha();

document.write("Joaquim tem " + (ano - 1996) + " anos");

pulaLinha();

ano = 2017;

document.write("Barney tem " + (ano - 1976) + " anos");

</script>
```

Todas as instruções serão executadas, o alerta e os dois pulos de linha. Ao recarregarmos o navegador, exibe-se o pop up com a mensagem `oi`.

![pop up com mensagem "oi"](https://s3.amazonaws.com/caelum-online-public/440+-+L%C3%B3gica+de+Programa%C3%A7%C3%A3o/pop+up+com+a+mensagem+oi.png)

Enquanto isso, no navegador veremos:

> Flávio tem 39 anos

> Joaquim tem 20 anos

> Barney tem 41 anos

Entre as linhas, há espaços em branco. Como chamamos a função duas vezes, o alerta será exibido novamente. Removeremos o alerta, e agora entendemos que a função serve como um atalho para as instruções que queremos executar no programa.

E se chamarmos a função de `x`?

```xml
<meta charset="UTF-8">

<script>

    function x() {

        document.write("<br>");
        document.write("<br>");

}

var ano = 2016;

document.write("Flávio tem " + (ano - 1977) + " anos");

x();

document.write("Joaquim tem " + (ano - 1996) + " anos");

x();

ano = 2017;

document.write("Barney tem " + (ano - 1976) + " anos");

</script>
```

O programa continuará funcionando, entretanto, ao visualizarmos a função `x()`, não temos como saber do que se trata. O nome de uma função é tão importante quanto o código que ela executa, para deixar claro o que ela faz.

Com isso, concluímos a criação de nossa primeira função, que não recebe parâmetro. O `document.write()` aceita receber parâmetros para, internamente, imprimir na tela aquilo que lhe é passado. Já o `pulaLinha()` ficou vazio e não está preparado para lidar com isso.

Nosso código pode ser melhorado ainda, como veremos adiant