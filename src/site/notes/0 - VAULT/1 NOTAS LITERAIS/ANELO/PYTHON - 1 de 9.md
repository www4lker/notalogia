---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-1-de-9/","tags":["python","ALURA"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# PYTHON - 1 e 2 de 9

## criado em: 
-  27-04-2023 - 12:50

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON - COMEÇANDO COM A LINGUAGEM - ALURA\|PYTHON - COMEÇANDO COM A LINGUAGEM - ALURA]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON - 3 de 9\|PYTHON - 3 de 9]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON AVANÇANDO NA LINGUAGEM - 1 DE 7\|PYTHON AVANÇANDO NA LINGUAGEM - 1 DE 7]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON AVANÇANDO NA LINGUAGEM - 2 DE 7\|PYTHON AVANÇANDO NA LINGUAGEM - 2 DE 7]]
- tags: #python #ALURA 

---
![Pasted image 20230427125102.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230427125102.png) 
(00:01) Olá, bem vindo à Alura, ao nosso primeiro curso sobre Python na versão 3. Nesse curso introdutório, vamos implementar um jogo para começar a programar com Python. É um jogo de adivinhação, onde o computador vai escolher um número e o usuário precisa adivinhá-lo.

(00:47) Vamos aprender a trabalhar com variáveis de diversos tipos, como gerar um número aleatório, como tomar decisões através de **`if else`**, pois o computador dará uma dica para nós, se o número é menor ou maior. O jogo tem várias rodadas, então existe a necessidade de repetir uma parte do código. É preciso ler a entrada do usuário e mostrar o resultado para o jogador.

(01:40) Enfim, nesse curso teremos vários desafios a resolver e eu convido você a me acompanhar nessas próximas aulas, para aprender essa linguagem fantástica e se divertir muito com Python 3.

### Para saber mais: built-in

No curso anterior, falamos bastante sobre as funções _built-in_, como `type(..)`, `int()` ou `input(..)`. Lembrando que funções _built-in_ são aquelas que você não precisa importar explicitamente, pois elas estão disponíveis para seu uso automaticamente.

Existe uma função relacionado com o tipo `bool`, com o mesmo nome. Veja o código abaixo:

```python-repl
>>> bool(0)
False
>>> bool("")
False
>>> bool(None)
False
>>> bool(1)
True
>>> bool(-100)
True
>>> bool(13.5)
True
>>> bool("teste")
True
>>> bool(True)
True
```

Repare que os valores _vazios_ ou zeros são considerado `False`, do contrário são considerados `True`.

A função executa por baixo dos panos algo que se chama de _"Truth Value Testing"_. Isto é, decidir quando um valor é considerado `True` ou `False`.

---

