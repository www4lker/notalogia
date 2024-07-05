---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/piadas-de-programadores/","tags":["javascript","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Piadas de programadores

## criado em: 
-  29-04-2023 - 19:16

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 2/mais perguntas sobre programação\|mais perguntas sobre programação]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/faq programação extra\|faq programação extra]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 2/para além do PONG\|para além do PONG]]
- tags: #javascript #ANELO 
- Fontes & Links: 

---


>Do you know some jokes about programmers?

*ChatGPT*

Sure, here are some jokes about programmers:

1.  Why did the programmer quit his job? He didn't get arrays.
    
2.  Why do programmers prefer dark mode? Because light attracts bugs.
    
3.  Why do programmers prefer dogs? Because they are good at fetching errors.
    
4.  Why do programmers always mix up Christmas and Halloween? Because Oct 31 equals Dec 25.
    
5.  What's the object-oriented way to become wealthy? Inheritance.
    
6.  Why did the programmer go broke? Because he used up all his cache.
    
7.  Why do programmers prefer UNIX? Because UNIX is user-friendly. It's just picky about its friends.
    
8.  Why do programmers prefer coding at night? Because the computer screen looks like day mode.
    

Hope you enjoy them!

---

The programmer's wife said:
- Go to the market and bring a liter of milk. If there are eggs, get six.

The programmer came back with six liters of milk, then his wife said:
- Programmer! Why did you bring six liters of milk?

And the Programmer replied:
- They had eggs....

---

>can you make a javascript code from the statement including his confusion? after that write te code with error resolved

``` javascript
function buyGroceries() {
  let milk = 1;
  let eggs = 6;
  
  if (market.hasEggs()) {
    milk = 6;
  }
  
  return [milk, eggs];
}

let groceries = buyGroceries();
console.log(`Bought ${groceries[0]} liters of milk and ${groceries[1]} eggs.`); ```

This code sets the initial values of `milk` and `eggs` to 1 and 6 respectively. The `buyGroceries` function checks if the market has eggs available, and if so, sets `milk` to 6 instead of 1. Finally, the function returns an array with the values of `milk` and `eggs`.

The code has a logical error because the programmer misinterpreted the instruction to buy 6 eggs as "buy 6 liters of milk." To fix the error, the `if` statement should update the value of `eggs` to 6, not `milk`. Here is the corrected code:

``` javascript
function buyGroceries() {
  let milk = 1;
  let eggs = 0;
  
  if (market.hasEggs()) {
    eggs = 6;
  }
  
  return [milk, eggs];
}

let groceries = buyGroceries();
console.log(`Bought ${groceries[0]} liters of milk and ${groceries[1]} eggs.`);
 ```
