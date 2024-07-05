---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/concatenacao-parte-2/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# concatenação parte 2

## criado em: 
-  21-03-2023 - 11:36

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/adicionando variáveis no programa\|adicionando variáveis no programa]]
- tags: 
- Fontes & Links: 

---

Faremos mais testes de operações, desta vez subtraindo `2016 - 39`:

```xml
<meta charset="UTF-8">

<script>

    document.write("A idade do Flávio é");
    document.write(2016 - 39);

</script>
```

Salvaremos o código e recarregaremos a página. Vamos obter o seguinte resultado:

> A idade do Flávio é 1977

Entretanto, este número não representa a idade, e sim o ano de nascimento do Flávio. O programa deve ser coerente, por isso alteraremos a mensagem:

```xml
<script>

    document.write("Flávio nasceu em")
    document.write(2016 - 39);

</script>
```

Salvaremos, e recarregaremos a página. Desta vez o browser exibe:

> Flávio nasceu em 1977

É preciso ter cuidado, a cada alteração feita deve-se salvar o programa, para depois recarregá-lo no navegador. Pode acontecer de esquecermos de salvar o arquivo, ou de recarregar, e não visualizarmos a versão mais recente.

Feito isso, trabalharemos agora com outro tipo de problema para aprofundarmos nosso entendimento. O que acontecerá se incluirmos a operação na mesma frase de `Flávio nasceu em`?

```javascript
document.write("Flávio nasceu em 2016 - 39");
```

Teremos um texto, e a exibição será a seguinte:

> Flávio nasceu em 2016 - 39

O que acontece se colocarmos a frase em uma string separada da operação numérica?

```javascript
document.write("Flávio nasceu em" + "2016 - 39")
```

Ao salvarmos e recarregarmos a página, teremos o mesmo resultado:

> Flávio nasceu em 2016 - 39

Faremos uma nova operação para descobrirmos as médias entre três idades, para isso, deveremos somá-las e dividir por `3`:

```javascript
document.write("A média das idades é");
document.write(20 + 10 + 30/3);
```

Com isso, esperamos que o resultado seja `20`. Salvaremos o programa, e recarregaremos a página no navegador. Tivemos o seguinte resultado:

> A média das idades é 40

Este não é o resultado correto, que deveria ser `20`.

A programação, assim como na matemática, prioriza a avaliação das multiplicações e divisões. No caso acima, o JavaScript primeiro realiza a divisão de `30/3`, resultando em `10` para, em seguida, somar aos demais `20 + 10 + 10`, resultando em `40`.

Sendo assim, se quisermos indicar que algo deve ser avaliado primeiro, devemos inseri-lo entre parênteses - sem confundir com os parênteses que seguem o comando `write`. Antes da operação de divisão, queremos que o programa realize a somatória de `20 + 10 + 30`, portanto, é esse trecho que isolaremos:

```javascript
document.write((20 + 10 + 30)/3);
```

Salvaremos, e recarregaremos o navegador. Obtivemos o resultado correto:

> A média das idades é 20

Vamos supor que temos a seguinte situação:

```javascript
document.write("A soma das idades é" + 20 + 10 + 30);
```

Como não há nenhum parênteses que indique prioridade, a leitura será feita normalmente, da esquerda para a direita. Por termos string e números, será feita uma **concatenação**, assim, o resultado será:

> A média das idades é 201030

Não é este nosso objetivo. Podemos salvar e recarregar a página para confirmar o resultado. Queremos que a operação de soma seja realizada primeiro, assim, recorreremos aos parênteses:

```javascript
document.write("A soma das idades é" + (20 + 10 + 30));
```

Lembrando que devemos sempre ter o mesmo número de parênteses de um lado e de outro. Salvaremos e retornaremos ao navegador. Obtivemos o seguinte resultado:

> A soma das idades é 60

Se quisermos calcular a média, manteremos a soma como está, e acrescentaremos a divisão por três (`/3`):

```javascript
document.write("A soma das idades é" + (20 + 10 + 30)/3);
```

A operação que está entre parênteses será considerada primeiro. Em seguida, ele fará a divisão, e o resultado disso será concatenado com a frase `A soma das idades é`. Teremos como resultado final, portanto:

> A soma das idades é 20

Trabalharemos a seguir com a operação:

```javascript
document.write("Flávio nasceu em" + 2016 - 39);
```

Em seguida, isolaremos a operação matemática entre parênteses:

```javascript
document.write("Flávio nasceu em" + (2016 - 39));
```

Dessa forma, primeiramente, será calculado o resultado de `2016 - 39`, para então seguir às demais informações. Inseriremos mais um comando, indicando a idade de Joaquim:

```javascript
document.write("Flávio nasceu em" + (2016 - 39));
document.write("Joaquim nasceu em" + (2016 - 20));
```

E outro, com a idade de Barney:

```javascript
document.write("Flávio nasceu em" + (2016 - 39));
document.write("Joaquim nasceu em" + (2016 - 20));
document.write("Barney nasceu em" + (2016 - 40));
```

O resultado esperado é o ano de nascimento de cada um, resultado das respectivas subtrações. Salvaremos o programa, retornaremos ao navegador e recarregaremos a página. Obtivemos o seguinte resultado:

```css
Flávio nasceu em 1977Joaquim nasceu em 1996Barney nasceu em 1976
```

Os valores estão corretos, entretanto, faremos com que sejam exibidos separadamente por linha. Para isso, podemos concatenar um `<br>`:

```javascript
document.write("Flávio nasceu em" + (2016 - 39) + "<br>");
document.write("Joaquim nasceu em" + (2016 - 20) + "<br>");
document.write("Barney nasceu em" + (2016 - 40) + "<br>");
```

A primeira coisa que o JavaScript fará é identificar a presença de parênteses, que indiquem uma operação a ser priorizada. No caso, temos as subtrações referentes aos anos de nascimento.

Feito isso, a análise ocorrerá normalmente, da esquerda para a direita. Como temos texto e número, haverá a concatenação destes, resultando na frase `Flavio nasceu em 1977`, por exemplo. Por fim, será concatenado o `<br>`, já que o comando está inserido no código HTML, resultando na quebra de linha entre uma frase e a seguinte.

Salvaremos o programa, retornaremos ao navegador e carregaremos a página, com o seguinte resultado:

```css
Flávio nasceu em 1977
Joaquim nasceu em 1996
Barney nasceu em 1976
```

Alternativamente, podemos obter o mesmo resultado escrevendo o código da seguinte forma:

```javascript
document.write("Flávio nasceu em " + (2016 - 39));
document.write("<br>");
document.write("Joaquim nasceu em " + (2016 - 20));
document.write("<br>");
document.write("Barney nasceu em " + (2016 - 40));
document.write("<br>");
```

A forma de escrita fica a critério do programador, levando-se em consideração a facilitação do entendimento por parte do leitor.