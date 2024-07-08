---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/leis-de-de-morgan/","tags":["logica","python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# leis de De Morgan

## criado em: 
-  06-05-2023 - 18:14

### Conteúdo Relacionado
- notas: 
- tags: #logica #python #ANELO 
- Fontes & Links: 

---

As Leis de Morgan são um conjunto de teoremas na lógica proposicional que descrevem a relação entre os operadores lógicos `not`, `and` e `or`. Essas leis são importantes porque mostram como é possível expressar uma operação lógica em termos de outras operações lógicas.

As duas leis de Morgan são:

1.  A negação de uma conjunção (expressão com o operador `and`) é equivalente à disjunção das negações dos termos envolvidos. Ou seja, a negação de uma expressão como `A and B` é equivalente a `(not A) or (not B)`.
    
2.  A negação de uma disjunção (expressão com o operador `or`) é equivalente à conjunção das negações dos termos envolvidos. Ou seja, a negação de uma expressão como `A or B` é equivalente a `(not A) and (not B)`.
    

Em termos mais simples, a primeira lei de Morgan diz que, se você negar uma declaração `A` e outra declaração `B`, e então disjuntar essas duas declarações negadas, o resultado será o mesmo que conjuntar as declarações originais com um `and`. A segunda lei de Morgan, por sua vez, diz que se você negar uma declaração `A` e outra declaração `B`, e então conjuntar essas duas declarações negadas, o resultado será o mesmo que disjuntar as declarações originais com um `or`.

As Leis de Morgan podem ser úteis em vários contextos, incluindo a simplificação de expressões lógicas complexas e a verificação da validade de argumentos lógicos. É importante notar que as Leis de Morgan só se aplicam a operações lógicas envolvendo dois termos. Se houver mais de dois termos em uma expressão, é necessário usar outras técnicas de simplificação lógica para simplificar a expressão.