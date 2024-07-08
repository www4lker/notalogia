---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/comparando-javascript-com-python/","tags":["javascript","python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# comparando Javascript com Python

## criado em: 
-  30-04-2023 - 11:31

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Similarities between js and py\|Similarities between js and py]]
- tags: #javascript #python #ANELO
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/python é fácil\|python é fácil]]
- Fontes & Links: 

---

# Para saber mais: JavaScript vs Python

Muito pode se falar na comparação das duas linguagens, mas para esse exercício vamos focar nas operações de adição e multiplicação. Vimos que o Python apenas soma valores de tipos numéricos, ou seja, o exemplo seguir **não funciona** por causa do tipo **`str`**:

```ini
numero1 = 10
numero2 = "20"
soma = numero1 + numero2
```

**Resultado**

```bash
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

Agora, o que acontece com o mesmo código no mundo JavaScript? Você pode testar isso facilmente dentro do seu navegador, apertando **F12** para abrir o seu console. Nele, digite o mesmo código:

![Soma em JavaScript do número 10 com a string 20, que resulta em 1020](https://s3.amazonaws.com/caelum-online-public/python3/img/02/soma-javascript.png)

Repare que o JavaScript concatena os valores, criando a string: "1020"

Você pode pensar que isso faz sentido, já que a variável **`numero2`** é do tipo string, no entanto o que o JavaScript faz é uma conversão implícita. O JavaScript converte a variável **`numero1`** automaticamente para string, e isso pode ser perigoso.

Vou tentar dar mais um exemplo com JavaScript. Agora vamos multiplicar **`numero1`** com **`numero2`**:

```ini
numero1 = 10
numero2 = "20"
produto = numero1 * numero2
```

![Multiplicação em JavaScript do número 10 vezes a string 20, que resulta em 200](https://s3.amazonaws.com/caelum-online-public/python3/img/02/produto-javascript.png)

Repare que o JavaScript multiplicou e imprimiu 200! Agora também aconteceu uma conversão automática, mas dessa vez a variável **`numero2`** foi convertida para **`int`**. Novamente, o JavaScript é tolerante nesse aspecto e converte quando julga necessário. **O Python é mais rígido nesse sentido e não faz essas conversões implícitas.**

Ótimo, então vamos testar a multiplicação com Python:

```makefile
numero1 = 10
numero2 = "20"
produto = numero1 * numero2
print(produto)
```

O resultado nos surpreende:

```undefined
20202020202020202020
```

Não deu erro e sim imprimiu 10 vezes 20! Mas eu não acabei de falar que o Python é rígido e não converte automaticamente?

Falei e na verdade não aconteceu uma conversão automática/implícita. Trata-se apenas de um **_syntax sugar_** do mundo Python. Um _syntax sugar_, açúcar sintático da linguagem, apenas simplifica algo que seria trabalhoso, mas não muda a característica da linguagem. Então, ao invés de escrever dez vezes o número 20, podemos simplificar e escrever **`10 * "20"`**. Tudo bem?