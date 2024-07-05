---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-6-1/","tags":["python","meth","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON 6 - 1
###

## criado em: 
-  30-04-2023 - 15:54

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 5 - 2\|PYTHON 5 - 2]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 6 - 2\|PYTHON 6 - 2]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PY - built in functions\|PY - built in functions]]
- tags: #python #meth #ANELO 
- Fontes & Links: 

---

A lógica principal do nosso jogo já está funcionando, mas ainda há um detalhe, o número secreto não é tão secreto assim, pois ele está fixo! Então vamos alterar isso, para que ele passe a ser um número aleatório, coisa que veremos nesse capítulo.

## Gerando um número aleatório

A ideia é que o próprio jogo, toda vez que for executado, gere esse número, ele que decide isso, não nós. E para gerar um número aleatório, o Python 3 possui a função **`random()`**, que gera um número no intervalo entre 0.0 e 1.0. Mas ao contrário das [funções _built-in_](https://docs.python.org/3/library/functions.html) do Python, como as funções **`input()`**, **`int()`**, **`print()`** e **`range()`**, que são **funções embutidas** do Python (que já vem com o mesmo), a função **`random`** não vem, pois está em um módulo separado, e esse módulo precisa ser importado.

Podemos ir ao console do Python e testar isso. Primeiro importando o módulo:

```python-repl
>>> import random
```

E a partir desse módulo, chamamos a função **`random()`**:

```python-repl
>>> import random
>>> random.random()
0.6022965518496559
```

## Arredondando um número

Só que, como podemos perceber, o número gerado tem muitas casas decimais e está no intervalo entre 0.0 e 1.0, mas no nosso jogo precisamos de um número entre 1 e 100. O que podemos fazer é multiplicar o número gerado por 100:

```python-repl
>>> import random
>>> random.random() * 100
58.30742817094118
```

Já conseguimos chegar a um número mais próximo do ideal, falta agora removermos as casas decimais. Podemos utilizar a já conhecida função **`int`**, que irá converter o número aleatório, que é um float, em um número inteiro:

```python-repl
>>> int(random.random() * 100)
91
```

Mas reparem no exemplo abaixo:

```python-repl
>>> numero_random = random.random() * 100
>>> numero_random
18.895629671768187
>>> int(numero_random)
18
```

A função **`int`** nada mais faz do que **remover** as casas decimais do número flutuante. Mas o número gerado acima está mais próximo de 19 do que de 18, correto? Será que temos uma função que **arredonda** esse número para nós? Sim! Temos mais uma função _built-in_, a **`round`**:

```python-repl
>>> numero_random = random.random() * 100
>>> numero_random
18.895629671768187
>>> int(numero_random)
18
>>> round(numero_random)
19
```

Conhecendo isso, podemos aplicar ao nosso jogo. Faremos isso no próximo vídeo, até lá!