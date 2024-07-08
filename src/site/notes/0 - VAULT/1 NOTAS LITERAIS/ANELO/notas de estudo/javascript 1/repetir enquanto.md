---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/repetir-enquanto/","tags":["javascript","repetição"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# repetir enquanto

## criado em: 
-  23-03-2023 - 09:31

### Conteúdo Relacionado
- notas: 
- tags: #javascript #repetição
- Fontes & Links: [alura 7](https://cursos.alura.com.br/course/logica-programacao-javascript-html/task/17737)

---

Nesta aula, aprenderemos a criar um programa que exiba todos os anos em que houve copas do mundo de futebol, desde 1930, data do primeiro campeonato.

Criaremos um novo arquivo, a partir do nosso jogo de adivinhação, selecionando a opção "File > Save As... > ano_copa.html". Manteremos apenas as funções `mostra` e `pulaLinha`:

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

Declararemos uma variável `anoCopa` que receberá o ano `1930`:

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

var anoCopa = 1930;

</script>
```

Criaremos um `alert` para exibir a frase "Teve copa em", concatenada com a variável `anoCopa`:

```csharp
var anoCopa = 1930;

alert("Teve copa em " + anoCopa);
```

Salvaremos e retornaremos ao navegador. Abriremos o arquivo do programa `ano_copa.html`, selecionando "Arquivo > Abrir arquivo...". Surge um pop up com a seguinte mensagem:

```css
Teve copa em 1930
```

Nosso objetivo é fazer com que o programa exiba todos os anos em que houve copas do mundo.

Retornaremos ao código.

Precisamos informar ao programa que os anos de copa serão `anoCopa` mais 4:

```csharp
var anoCopa = 1930

alert("Teve copa em " + anoCopa);
anoCopa = anoCopa + 4
```

Assim, o `anoCopa` passa a valer `1934`. Repetiremos o processo, por diversas vezes, para que em cada uma delas tenhamos um ano de copa diferente:

```makefile
var anoCopa = 1930;

alert("Teve copa em " + anoCopa);
anoCopa = anoCopa + 4;

alert("Teve copa em " + anoCopa);
anoCopa = anoCopa + 4;

alert("Teve copa em " + anoCopa);
anoCopa = anoCopa + 4;

alert("Teve copa em " + anoCopa);
anoCopa = anoCopa + 4;

alert("Teve copa em " + anoCopa);
anoCopa = anoCopa + 4;

alert("Teve copa em " + anoCopa);
anoCopa = anoCopa + 4
```

Salvaremos, retornaremos ao navegador e recarregaremos a página. Assim surgirá um alerta referente a cada um dos anos em que houve Copa do Mundo.

Entretanto, é impraticável termos que copiar e colar tantas vezes até termos o número total de copas.

Como podemos observar, todas as instruções são iguais. E se pudéssemos criar uma função para repeti-las?

Primeiro, manteremos apenas uma das instruções em nosso código:

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

var anoCopa = 1930;

alert("Teve copa em " + anoCopa);
anoCopa = anoCopa + 4;

</script>
```

Criaremos uma função `repita` e abriremos um bloco:

```csharp
var anoCopa = 1930;

repita {

}

alert("Teve copa em " + anoCopa);
anoCopa = anoCopa + 4;
```

Inseriremos a mensagem que queremos repetir dentro do bloco da função, e tudo que estiver lá será replicado:

```csharp
var anoCopa = 1930;

repita {

    alert("Teve copa em " + anoCopa);
    anoCopa = anoCopa + 4;

}
```

Se funcionar, isso nos permitirá declarar o `anoCopa` como `1930`, e repetirá infinitas vezes a operação `anoCopa = anoCopa + 4`. Criaremos um alerta, para indicar o fim:

```csharp
var anoCopa = 1930;

repita {

    alert("Teve copa em " + anoCopa);
    anoCopa = anoCopa + 4;

}

alert("FIM");
```

Como a operação está inserida no bloco da função `repita`, o programa não acionará o `alert("FIM")`, em vez disso, retornará ao bloco e acionará a instrução infinitas vezes.

Como podemos fazer isso em JavaScript?

A primeira ferramenta de repetição que aprenderemos é chamada `while`, que recebe `true`:

```csharp
var anoCopa = 1930;

while(true) {

    alert("Teve copa em " + anoCopa);
    anoCopa = anoCopa + 4;

}

alert("FIM");
```

O `while(true)` indica que sempre será repetido o conteúdo do bloco dessa função. Se o `while` receber `false`, nada será repetido. Se salvarmos o programa, e recarregarmos a página, somente será exibido um alerta, com a mensagem `FIM`. A repetição não foi exibida.

Se trocarmos o `false` por `true`, significa que, enquanto isso for verdadeiro, haverá repetição, portanto temos:

```csharp
var anoCopa = 1930;

while(true) {

    alert("Teve copa em " + anoCopa);
    anoCopa = anoCopa + 4;

}

alert("FIM");
```

Salvaremos o programa, retornaremos ao navegador e salvaremos a página.

Surge um pop up com a mensagem: `Teve copa em 1930`, a cada vez que pressionamos "Ok", surge um novo ano de copa, como `1934`, `1938`, e assim sucessivamente. Entretanto, o programa não para, enquanto pressionarmos "Ok" sempre surgirá um novo ano de copa.

O Google Chrome apresenta uma opção, que diz "Impedir que esta página crie caixas de diálogo adicionais", ao marcarmos na caixa e pressionarmos "Ok", não surgirão mais pop ups. Ao fazermos isso, temos que fechar a aba atual e abrir uma nova, e utilizá-la para visualizar o programa.

Não queremos que sejam impressos anos infinitos, mas sim que o faça até que `anoCopa` seja menos que 2016, representamos isso da seguinte forma:

```scss
while(anoCopa <= 2016)
```

Que, no código, é inserido da seguinte forma:

```csharp
var anoCopa = 1930;

while(anoCopa <= 2016) {

    alert("Teve copa em " + anoCopa);
    anoCopa = anoCopa + 4;

}

alert("FIM");
```

Assim como a condição `if`, o `while` testará se `anoCopa` é menor ou igual a 2016, se for verdadeiro, as instruções contidas no bloco serão executadas. Isso significa que o programa acessará o bloco, enquanto `anoCopa <= 2016` for verdadeiro.

Ao chegarmos em 2017, é verificado se o número é menor ou igual a 2016, não sendo, a repetição cessará, o programa sairá da instrução e imprimirá o alerta `FIM`.

Vamos testar. Salvaremos o programa, retornaremos ao navegador e abriremos o programa `ano_copa.html`.

Surgirá o primeiro alerta, com o texto:

```css
Teve copa em 1930
```

Pressionaremos "Ok", até chegarmos em 2014, quando ao clicar em "Ok" será exibida a mensagem `FIM`.

Conseguimos implementar uma condição de repetição para que a condição do `while`, em determinado ponto, seja `false`.

Recapitulando, o `anoCopa` inicia em 1930 e, como este número é menor que 2016, o programa executará a instrução contida no bloco da função.

E se colocarmos que o ano inicial é 2017?

```csharp
var anoCopa = 2017;

while(anoCopa <= 2016) {

    alert("Teve copa em " + anoCopa);
    anoCopa = anoCopa + 4;
}

alert("FIM");
```

O JavaScript questionará se 2017 é menor que 2016, como a resposta é negativa, ele jamais executará as instruções dentro do bloco do `while`, passando direto para o `alert("FIM")`. Vamos testar. Salvaremos o programa e recarregaremos a página.

Surgirá um pop up com a mensagem:

```css
Essa página diz:

FIM
```

Retornaremos para `1930`.

Exibir o `alert` pode não ser agradável para o usuário. Assim, utilizaremos a função `mostra`:

```csharp
var anoCopa = 1930;

while(anoCopa <= 2016) {

    mostra("Teve copa em " + anoCopa);
    anoCopa = anoCopa + 4;
}

mostra("FIM");
```

Salvaremos e recarregaremos a página. Obtivemos uma lista contendo todos os anos em que houve copa:

```css
Teve copa em 1930

Teve copa em 1934

Teve copa em 1938

Teve copa em 1942

Teve copa em 1946
```

Assim sucessivamente, até a copa de 2014:

```css
Teve copa em 2014

FIM
```

Com poucas linhas de código, conseguimos repetir a instrução, enquanto a condição `anoCopa <= 2016` for verdadeira. Se alterarmos a condição para `while(true)`, será repetida a instrução ao infinito, fazendo com que o navegador trave. Salvaremos e recarregaremos a página.

O navegador não conseguirá processar essa informação, por isso o fecharemos. É preciso ter cuidado, há navegadores em que isso não é possível, é feita a impressão infinita no HTML, que acaba travando a máquina.

Retornaremos para a condição anterior.

Em vez de imprimirmos até 2016, podemos configurar de modo que imprima até o limite dos anos de copa.

Declararemos uma variável `limite`, que receberá um `prompt` solicitando ao usuário que digite a data limite:

```csharp
var limite = prompt("Entre com a data limite");
var anoCopa = 1930;

while(anoCopa <= 2016) {

    mostra("Teve copa em " + anoCopa);
    anoCopa = anoCopa + 4;
}

mostra("FIM");
```

Já que estamos tratando de um número, é uma boa prática colocarmos o`parseInt`:

```javascript
var limite = parseInt(prompt("Entre com a data limite"));
var anoCopa = 1930;

while(anoCopa <= 2016) {

    mostra("Teve copa em " + anoCopa);
    anoCopa = anoCopa + 4;
}

mostra("FIM");
```

Substituiremos o `2016` pela variável `limite`:

```javascript
var limite = parseInt(prompt("Entre com a data limite"));

var anoCopa = 1930;

while(anoCopa <= limite) {

    mostra("Teve copa em " + anoCopa);
    anoCopa = anoCopa + 4;
}

mostra("FIM");
```

Salvaremos e recarregaremos. Surgirá um pop up solicitando uma data limite, digitaremos `1998`. Pressionaremos "Ok". Temos como resultado a lista com todos os anos de copa, até 1998 e, após isso, a mensagem `FIM`.

Se digitarmos outro número, além de 1998 e que não seja 2002, não há problema, ele exibirá somente até o último ano em que houve copa do mundo. Se digitarmos `2016` serão impressos os anos até 2014.

Adiante, veremos outras estruturas de repetição possíveis.