---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/lacos-de-repeticao/","tags":["javascript","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# laços de repetição

## criado em: 
-  28-03-2023 - 00:38

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/sons gratis para projeto\|sons gratis para projeto]]
- tags: #javascript #ANELO 
- Fontes & Links: 

---

O for é uma estrutura de repetição em JavaScript que permite executar um bloco de código repetidas vezes, com base em uma condição específica. A estrutura básica do for é a seguinte:

scss

`for (inicialização; condição; incremento/decremento) {   // código a ser executado }`

Onde:

-   `inicialização` é a declaração de uma variável que será usada no loop e seu valor inicial;
-   `condição` é a condição que deve ser satisfeita para continuar o loop;
-   `incremento/decremento` é a atualização da variável de controle do loop em cada iteração.

Por exemplo, para imprimir os números de 0 a 4 na tela, podemos usar o for da seguinte maneira:

css

`for (let i = 0; i < 5; i++) {   console.log(i); }`

Neste exemplo, a variável `i` é inicializada com o valor 0. A condição é que `i` seja menor do que 5 para continuar o loop, então o bloco de código dentro do for é executado e a variável `i` é incrementada em 1 em cada iteração. O loop é executado até que `i` seja igual a 5 e, neste momento, o loop é encerrado.

O for também pode ser usado para iterar sobre elementos de uma lista ou matriz. Por exemplo, para imprimir cada elemento de uma lista de cores na tela, podemos fazer o seguinte:

css

`let cores = ['vermelho', 'verde', 'azul', 'amarelo']; for (let i = 0; i < cores.length; i++) {   console.log(cores[i]); }`

Neste exemplo, a variável `i` é inicializada com o valor 0. A condição é que `i` seja menor do que o comprimento da lista de cores para continuar o loop. O bloco de código dentro do for é executado em cada iteração, com o valor da lista de cores correspondente a `i` sendo impresso na tela.

O for é uma estrutura de controle muito útil em JavaScript para executar ações repetidas vezes. Combinado com outras estruturas de controle, como condicionais e funções, ele pode ser usado para criar algoritmos complexos e resolver problemas desafiadores.

---

não é necessário usar `i` como variável no for. O nome da variável pode ser qualquer nome de variável válido em JavaScript, como `j`, `k`, `contador`, `indice`, etc.

O importante é que a variável de controle seja inicializada com um valor apropriado, que a condição seja avaliada corretamente e que a variável seja atualizada de acordo com o que é necessário no bloco de código do loop.

Por exemplo, se quisermos imprimir os números de 1 a 10 na tela, podemos fazer o seguinte:

```
javascript

for (let contador = 1; contador <= 10; contador++) {   console.log(contador); }
```

Neste exemplo, a variável `contador` é inicializada com o valor 1. A condição é que `contador` seja menor ou igual a 10 para continuar o loop. O bloco de código dentro do for é executado em cada iteração, com o valor da variável `contador` sendo impresso na tela.

Portanto, o nome da variável pode ser qualquer nome válido em JavaScript, desde que a estrutura do for seja respeitada.