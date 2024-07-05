---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/pseudo-random/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# pseudo random

## criado em: 
-  30-04-2023 - 16:20

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 6 - 1\|PYTHON 6 - 1]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON AVANÇANDO NA LINGUAGEM - 6 DE 7\|PYTHON AVANÇANDO NA LINGUAGEM - 6 DE 7]]
- tags: #ANELO 
- Fontes & Links: 

---

## Pseudo-Random?

Aparentemente a geração de números aleatórios funcionou muito bem. Cada vez que chamamos o `random.random()` ou `random.randrange(..)`, foi gerado um outro número.
[[0 - VAULT/1 NOTAS LITERAIS/ANELO/computadores são determinísticos\|computadores são determinísticos]]
No entanto, computadores têm os seus problemas com aleatoriedade, pois são sistemas determinísticos. Em outras palavras, o nosso Python é previsível e na verdade não sabe criar números verdadeiramente aleatórios. Por isso se chama _Pseudo-Random_!

## Por que funcionou então?

`random` é um função que, dada a mesma entrada, gerará o mesmo número. O truque é oferecer sempre uma entrada diferente para ter números diferentes e exatamente isso que está acontecendo por baixo dos panos.

Essa entrada também é chamada de _seed_ (semente, em português). Entre as chamadas da função `random`, sempre é utilizado um novo _seed_. Por padrão o Python usa a hora (os milissegundos) como semente, mas nada nos impede de definir o mesmo _seed_ antecipadamente. Para isso, existe a função `seed`!

## Usando seed

Por exemplo, no jogo usamos a função `randrange` para gerar um número aleatório entre 1 e 100. Antes do `randrange` podemos chamar o `seed` para definir a entrada:

```python-repl
>>> random.seed(100)
>>> random.randrange(1, 101)
19
```

Repare que foi gerado 19 e se usarmos o mesmo _seed_ será gerado o mesmo número:

```python-repl
>>> random.seed(100)
>>> random.randrange(1, 101)
19
```

Repare que a biblioteca `random` é bem previsível e por isso se chama _pseudo-random_!