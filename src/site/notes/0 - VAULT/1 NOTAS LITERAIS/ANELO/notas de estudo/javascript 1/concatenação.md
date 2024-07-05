---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/concatenacao/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# concatenação

## criado em: 
-  21-03-2023 - 11:27

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/concatenação parte 2\|concatenação parte 2]]
- tags: 
- Fontes & Links: 

---

Veremos agora como podemos complementar a frase "A idade do Flávio é", exibindo a idade. Podemos inserir na mesma frase, da seguinte forma:

```xml
<meta charset="UTF-8">

 <script>

    alert("A idade do Flávio é 18 ");

 </script>
```

Ao salvarmos o programa e recarregarmos a página, vemos que este método funciona. Alternativamente, podemos criar um segundo alerta para exibir esta informação:

```xml
 <meta charset="UTF-8">

  <script>

    alert("A idade do Flávio é ");
    alert("18");

  </script>
```

Salvaremos e recarregaremos a página no navegador. Surge um primeiro alerta, com a mensagem "A idade do Flávio é", pressionaremos "OK" e, em seguida, surge um segundo pop up, com a mensagem "18".

Só que, se utilizarmos o `alert` no mundo JavaScript para exibir um texto para o usuário, e caso tenhamos dez mensagens, quantas vezes o usuário terá de pressionar "OK"? Várias. Isso tornará a experiência do visitante ruim. Se ele quiser ler a última linha, não conseguirá, porque surgirão muitos alertas seguidos.

O que fazer? O mundo JavaScript é representado por tudo que está inserido na tag `<script>`. Todo o conteúdo desta tag é interpretado pelo navegador como JavaScript. O mundo HTML é compreendido como tudo que está **fora** da tag `<script>`. O que faremos é escrever, a partir do mundo JS, um HTML. Para isto, adicionaremos `document.write()`:

```xml
<script>

    document.write()

</script>
```

A palavra `document` significa, em português, "documento". Nossa página HTML, nosso programa, é um documento. Já a palavra `write` corresponde à palavra "escrever". O `write` recebe parênteses ao final, ou seja, ele aceita receber algo para escrever no documento. Como vimos, o texto no JavaScript é incluído entre aspas.

O texto é chamado de `string`, tanto em JS como em outras linguagens de programação. Escreveremos a seguinte mensagem: "A idade do Flávio é"'

```xml
<meta charset="UTF-8">

<script>

    document.write("A idade do Flávio é ");

</script>
```

Salvaremos, retornaremos ao navegador e recarregaremos a página. No browser, veremos a mensagem que acabamos de escrever:

> A idade do Flávio é

Inseriremos uma segunda instrução `document`:

```xml
<meta charset="UTF-8">

<script>

    document.write("A idade do Flávio é ");
    document.write("18");

</script>
```

Salvaremos utilizando o atalho "Ctrl + S", e retornaremos ao navegador, recarregando a página. Surgirá a seguinte mensagem:

> A idade do Flávio é 18

Alguém que está começando a programar pode se perguntar: há muitas informações escritas em HTML no mundo JavaScript, que poderiam ter sido escritas de forma mais simples, diretamente, apenas com a primeira linguagem?

Vamos simular a seguinte situação, em que eliminaremos o `document.write`, pois ele só é pertinente ao JavaScript:

```xml
<meta charset="UTF-8">

A idade do Flávio é
18

<script>

</script>
```

Será que obteremos o mesmo resultado?

Retornaremos ao navegador e recarregaremos a página, após o qual teremos a mesma mensagem:

> A idade do Flávio é 18

Por que então utilizar o `document.write()` para, do mundo JavaScript, escrever em HTML? Porque o JavaScript é uma linguagem dinâmica. Podemos, eventualmente, imprimir estas informações múltiplas vezes. Apesar de escrevermos mais, no JavaScript podemos escrever um código dinâmico, mesmo em HTML.

Há duas formas de escrevermos usando `document.write`, as quais podemos separar em dois comandos:

```xml
<script>

    document.write("A idade do Flávio é ");
    document.write("18");

</script>
```

Ou inserir o valor `18` já na primeira frase:

```xml
<script>

    document.write("A idade do Flávio é 18");

</script>
```

De ambas as formas, o resultado visual será o mesmo:

![página com a frase "a idade do flávio é 18" em uma mesma linha](https://s3.amazonaws.com/caelum-online-public/440+-+L%C3%B3gica+de+Programa%C3%A7%C3%A3o/Aula+02/02.04_001_pagina-com-a.png)

Neste momento, o método menos verboso seria inserirmos o valor `18` logo após a frase `A idade do Flávio é`. Entretanto, isso nem sempre é interessante. Se quisermos pular uma linha, por exemplo, podemos utilizar a tag `<br>`. Isso porque a frase exibida no navegador está inserida no mundo HTML, e neste contexto, utilizamos esta tag sempre que queremos pular uma linha.

Como estamos escrevendo no mundo HTML, quando o navegador for processar a informação verá o `<br>` e entenderá que deve pular uma linha. Sendo assim, teremos o seguinte resultado na web:

```bash
 A idade do Flávio é 18

```

Poderíamos, alternativamente, ter escrito da seguinte forma:

```xml
<script>

    document.write("A idade do Flávio é ");
    document.write("18");
    document.write("<br>");

</script>
```

Salvaremos, retornaremos ao navegador, e recarregaremos a página. Obtivemos o mesmo resultado:

```bash
A idade do Flávio é 18
```

Portanto, na programação há diversas formas de se atingir um mesmo objetivo. Em algumas delas, escreveremos mais código, enquanto outras são mais diretas e simples. A forma a ser utilizada dependerá do tipo de problema que você está tentando resolver.

O que aconteceria se escrevêssemos o número `18` entre parênteses, sem as aspas?

```xml
<script>

    document.write("A idade do Flávio é ");
    document.write(18);

</script>
```

O JavaScript só considera algo como texto se estiver entre aspas, portanto, da forma como escrevemos `18`, o número será interpretado como texto? Não. Como sua representação é numérica, ele será interpretado como um número.

Salvaremos, recarregaremos a página, e teremos o mesmo resultado na web:

> A idade do Flávio é 18

Portanto, o `document.write` aceita trabalhar com tipo `texto` - "tipo" indica que é um tipo de dado -, cujo termo técnico é _string_, e "18", que é um número. Minha idade real não é 18, entretanto, os números nos permitem realizar operações. Por exemplo, o símbolo **`+`** representa soma, assim, podemos somar "18 + 20":

```xml
<script>

    document.write("A idade do Flávio é ");
    document.write(18 + 20);

</script>
```

Salvaremos, e recarregaremos a página. Vemos que a mensagem mudou, e agora temos:

> A idade do Flávio é 38

Portanto, o número nos permite realizar operações matemáticas, por exemplo, podemos utilizar o símbolo **`*`** para realizar multiplicações:

```xml
<script>

    document.write("A idade do Flávio é ");
    document.write(18 * 20);

</script>
```

Com isto, obteremos o seguinte resultado:

> A idade do Flávio é 360

Podemos realizar também uma operação de divisão, utilizando o símbolo **`/`** (barra):

```xml
<script>

    document.write("A idade do Flávio é ");
    document.write(18 / 2);

</script>
```

E nosso resultado, ao salvarmos o programa e recarregarmos a página, será:

> A idade do Flávio é 9

Poderemos optar por uma subtração, usando o símbolo **`-`** (hífen):

```xml
<script>

    document.write("A idade do Flávio é ");
    document.write(18 - 2);

</script>
```

Cujo resultado será:

> A idade do Flávio é 16.

O que acontece se colocarmos o número 18 entre aspas?

```xml
<script>

    document.write("A idade do Flávio é ");
    document.write("18");

</script>
```

O JavaScript entenderá isso como um número, ou um texto? Ele interpretará como um texto, porque está entre aspas. Faremos uma operação de adição, onde ambos os números serão colocados entre aspas:

```xml
<script>

    document.write("A idade do Flávio é ");
    document.write("18" + "20");

</script>
```

Cada número é interpretado como uma string, sendo assim, quando será a soma de `"18" + "20"`? Salvaremos o programa, retornaremos à página e a recarregaremos. Temos o seguinte resultado:

> A idade do Flávio é 1820

Quando temos uma operação de soma envolvendo texto, o JavaScript não entende se tratar de um número, e portanto realiza uma operação à qual damos o nome de **concatenação**. Isto significa que ele juntou um texto ao outro, o que resultou em `1820`. Este é então passado para o `write`, que o imprime desta forma.

Temos o comando `document.write`, e precisamos passar para ele o que desejamos imprimir. Da forma como escrevemos, ele entenderá que queremos imprimir a **concatenação** do número `18` com `20`. Portanto, a primeira operação realizada pelo JavaScript é unir estes dois números para, em seguida, informar ao `write` que ele deve imprimir.

O que acontece se tirarmos as aspas em apenas um dos números?

```javascript
document.write("18" + 20);
```

Estamos tentando somar um texto com um número. Uma string somada a outra resulta em uma concatenação, um número somado a outro resulta na soma numérica dos dois, mas quando temos uma string a ser somada com um número, se testarmos salvando e recarregando a página, teremos:

> A idade do Flávio é 1820

Aconteceu que o JavaScript, ao receber um texto e um número, converte este último para texto, resultando em `1820`. Ou seja, quando há texto e número, ele converte tudo para texto.