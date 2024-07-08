---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-2/porque-arrays-comecam-com-zero/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# porque arrays começam com zero

## criado em: 
-  27-03-2023 - 18:51

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 2/como codigo vira eletricidade e vice versa\|como codigo vira eletricidade e vice versa]]
- tags: 
- Fontes & Links: 

---

Explique em termos simples o motivo de, em programação, contarmos arrays a partir de zero:

Em programação, contamos arrays a partir do zero por uma questão de conveniência e tradição. Quando começamos a contar do zero, podemos calcular facilmente a posição de um elemento em um array usando o índice e o endereço base (onde o array começa na memória).

Imagine que temos um array chamado "A" e o endereço base deste array é "B". Se queremos acessar o primeiro elemento (índice 0), basta somar B + 0, e obtemos a posição na memória do elemento. Para acessar o segundo elemento (índice 1), somamos B + 1 e assim por diante.

Essa abordagem torna os cálculos de posição na memória mais simples e eficientes, e é por isso que, em programação, geralmente contamos arrays a partir de zero.