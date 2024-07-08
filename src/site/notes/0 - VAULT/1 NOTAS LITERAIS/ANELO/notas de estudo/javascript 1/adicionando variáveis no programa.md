---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/adicionando-variaveis-no-programa/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# adicionando variáveis no programa

## criado em: 
-  21-03-2023 - 13:23

### Conteúdo Relacionado
- notas: [[ ninguem me disse que tinhamatematica\| ninguem me disse que tinhamatematica]]
- tags: 
- Fontes & Links: 

---

Concluímos a exibição dos anos de nascimento, mas podemos dar outras informações, como a idade em si. Para isso, alteraremos o texto para `Flávio tem (...) anos` e, incluiremos os anos de nascimento para termos como resultado final as idades de cada um:

```xml
<meta charset="UTF-8">

<script>

    document.write("Flávio tem " + (2016 - 1977) + " anos");
    document.write("<br>");
    document.write("Joaquim tem " + (2016 - 1996) + " anos");
    document.write("<br>");
    document.write("Barney tem " + (2016 - 1976) + " anos");
    document.write("<br>");

</script>
```

Observe que lembramos de incluir um espaço antes da palavra `anos`, para que ela não apareça "grudada" à idade. Salvaremos e recarregaremos a página, com o seguinte resultado:

> Flávio tem 39 anos
> 
> Joaquim tem 20 anos
> 
> Barney tem 40 anos

Só que, se salvarmos o programa como está, e avançarmos um ano, como se passássemos de 2016 para 2017, ou qualquer outro ano no futuro, o que acontecerá com nosso programa? Teríamos que alterar o ano manualmente para cada um dos comandos:

```xml
<meta charset="UTF-8">

<script>

    document.write("Flávio tem " + (2017 - 1977) + " anos");
    document.write("<br>");
    document.write("Joaquim tem " + (2017 - 1996) + " anos");
    document.write("<br>");
    document.write("Barney tem " + (2017 - 1976) + " anos");
    document.write("<br>");

</script>
```

Salvaremos e recarregaremos a página, para vermos que o programa funciona, sucessivamente, para todos os anos no futuro. Mas e se tivéssemos, em vez de três, quarenta pessoas? Teríamos que trocar manualmente o ano atual para cada uma delas, isso seria demasiadamente laborioso.

Queremos pensar em uma maneira para podermos, em um único lugar, escrever o ano e fazer com que ele seja acessado nos comandos, como se tivéssemos um envelope "ano" com um valor específico, como "2016". Portanto, onde temos `2016` no código, trocaremos por `ano`:

```xml
<meta charset="UTF-8">

<script>

    document.write("Flávio tem " + (ano - 1977) + " anos");
    document.write("<br>");
    document.write("Joaquim tem " + (ano - 1996) + " anos");
    document.write("<br>");
    document.write("Barney tem " + (ano - 1976) + " anos");
    document.write("<br>");

</script>
```

Se trocarmos o valor de `ano`, de `2016` para `2017`, por exemplo, precisaremos fazer esta alteração somente em um lugar, e todos os lugares em que esta palavra for utilizada terão o novo valor aplicado.

Em nosso programa, conseguimos este efeito de "envelope" por meio da criação de **variáveis**. Como o próprio nome sugere, elas variam, e são representadas da seguinte forma:

```csharp
var ano;
```

Mas qual é o **valor** da variável `ano`? Para que ele seja recebido, utilizaremos o símbolo **`=`** (sinal de igual). Em programação, não lemos **`=`** como "igual", e sim como "recebe". Definiremos então o valor como `2016`:

```xml
<script>

    var ano = 2016;

    document.write("Flávio tem " + (ano - 1977) + " anos");
    document.write("<br>");
    document.write("Joaquim tem " + (ano - 1996) + " anos");
    document.write("<br>");
    document.write("Barney tem " + (ano - 1976) + " anos");
    document.write("<br>");

</script>
```

Assim, a variável `ano` recebe o valor `2016`. Salvaremos o programa e retornaremos ao navegador para recarregarmos a página. Obtivemos o seguinte resultado:

```undefined
Flávio tem 39 anos
Joaquim tem 20 anos
Barney tem 40 anos
```

Nosso código funcionou como esperado. Suponhamos que estejamos em 2017. Precisaremos fazer a alteração em um único lugar - na variável -, para que os valores das idades sejam atualizados:

```xml
<script>

    var ano = 2017;

    document.write("Flávio tem " + (ano - 1977) + " anos");
    document.write("<br>");
    document.write("Joaquim tem " + (ano - 1996) + " anos");
    document.write("<br>");
    document.write("Barney tem " + (ano - 1976) + " anos");
    document.write("<br>");

</script>
```

Automaticamente, todos os lugares em que a palavra `ano` está presente serão interpretados como `2017`. Salvaremos, recarregaremos a página, e obteremos o seguinte resultado:

> Flávio tem 40 anos
> 
> Joaquim tem 21 anos
> 
> Barney tem 41 anos

O resultado foi o desejado! Quando o JavaScript se depara com a variável `ano`, ele somente a interpretará como uma string se estiver em aspas (`"ano"`). Como não é o caso, ele verificará se é um número. Não se tratando de um numeral, o JS determinará se é uma variável. Anteriormente, escrevemos `var ano`, sendo assim, ela existe, e quando o valor for computado, a palavra `ano` será trocada pelo valor `2017`.

> O processo de "raciocínio" do JavaScript será questionar se determinado trecho está entre aspas, e se estiver, é uma string, caso negativo, será feita uma próxima pergunta: trata-se de um número? Caso a resposta seja "não", significa que se trata de uma **variável**.

É interessante trabalharmos com variáveis, porque ao declaramos eles em um único lugar, várias instruções podem depender de uma mesma variável e, quando alteramos seu valor, isso é refletido em todos os pontos do código onde aparece.

**Cuidado**, como dito anteriormente, a variável é escrita somente com letras minúsculas. Se alterarmos um caractere para maiúsculo, como no exemplo abaixo, em que "a" está em maiúsculo em "Ano",

```javascript
document.write("Flávio tem " + (Ano - 1977) + " anos");
```

E se salvarmos e recarregarmos a página, veremos que nada foi exibido. Ao abrirmos o console em "Ferramentas > Visualizar > Desenvolvedor > Console JavaScript", veremos a seguinte mensagem de erro:

> Uncaught ReferenceError: Ano is not defined.

Ou seja, `Ano` não foi definido. Este erro é comum quando começamos a programar, e indica que a variável `Ano` não existe, pois definimos `ano`. Em qualquer momento, no próprio código, podemos indicar um novo valor para esta mesma variável:

```xml
<script>

    var ano = 2016;

    document.write("Flávio tem " + (ano - 1977) + " anos");
    document.write("<br>");
    document.write("Joaquim tem " + (ano - 1996) + " anos");
    document.write("<br>");

    ano = 2017;
    document.write("Barney tem " + (ano - 1976) + " anos");
    document.write("<br>");

</script>
```

O navegador processará a tag `<script>` linha a linha, na ordem em que foram declaradas. Na primeira, teremos a informação de que a variável `ano` recebe o valor `2016`. Portanto, conforme o código acima, para Flávio e Joaquim o valor considerado será `2016`.

Temos uma linha mais abaixo em que declaramos que a variável `ano` terá `2017` como valor. Assim, tudo que estiver abaixo dela deverá considerar a variável desta forma, ou seja, Barney, por exemplo, terá como ano base `2017`.

O prefixo `var` só é utilizado ao declararmos a variável pela primeira vez, então não é necessário utilizá-lo ao definirmos um novo valor. As variáveis nos ajudam, também, a fazer a manutenção de nosso código, já que ela é declarada em um único ponto e pode ser utilizada em diversos momentos.