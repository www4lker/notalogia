---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/hoisted-var/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# hoisted var

## criado em: 
-  21-03-2023 - 14:21

### Conteúdo Relacionado
- notas: 
- tags: 
- Fontes & Links: 

---

*por que em java script a ordem do var altera a resolução de uma operanção?*

Em JavaScript, a ordem das variáveis pode afetar o resultado de uma operação quando a expressão envolve variáveis que ainda não foram inicializadas. Isso ocorre porque as variáveis são "elevadas" (hoisted) para o topo do escopo em que foram declaradas antes da execução do código, mas a atribuição de valor à variável só ocorre no ponto em que a declaração é feita no código.

Por exemplo, se você tentar fazer uma operação que envolve uma variável que ainda não foi inicializada, o resultado pode ser diferente dependendo da ordem das declarações das variáveis no seu código. Por isso, é importante sempre inicializar as variáveis antes de usá-las em uma operação.

---

>Em JavaScript, a ordem das variáveis pode afetar o resultado de uma operação quando a expressão envolve variáveis que ainda não foram inicializadas. Isso ocorre porque, em JavaScript, as variáveis são elevadas (hoisted) para o topo do escopo em que foram declaradas antes da execução do código.

>Isso significa que, independentemente da posição em que a variável é declarada dentro do escopo, ela é sempre considerada como tendo sido declarada no início do escopo, antes da execução do código. No entanto, **a atribuição de valor à variável só ocorre no ponto em que a declaração é feita no código.**

>Assim, se uma expressão envolver variáveis que ainda não foram inicializadas, a ordem das declarações pode afetar o resultado. Por exemplo:

var x = 5;
var y = x + 3;
console.log(y); // resultado: 8

var a;
var b = a + 3;
console.log(b); // resultado: **NaN** (Not a Number)


>No segundo exemplo, a variável `a` é declarada, mas não recebe um valor antes da atribuição à variável `b`. Como resultado, `a` é considerada como tendo o valor `undefined` no momento em que a expressão `a + 3` é avaliada, resultando em `NaN` (Not a Number) como resultado final. Se a ordem das declarações for invertida, o resultado será diferente:

css

`var a; var b = 3 + a; console.log(b); // resultado: NaN (Not a Number)`

>Aqui, `b` é atribuída a expressão `3 + a`, em que `a` ainda tem o valor `undefined`. Como a adição de um número com `undefined` resulta em `NaN`, o resultado final também é `NaN`.