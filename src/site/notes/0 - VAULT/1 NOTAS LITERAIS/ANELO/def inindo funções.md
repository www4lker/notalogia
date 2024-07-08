---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/def-inindo-funcoes/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# def inindo funções

## criado em: 
-  30-04-2023 - 17:19

### Conteúdo Relacionado
- notas: 
- tags: #python #ANELO 
- Fontes & Links: 

---

## Declarando funções

Pouco vimos sobre funções, mas não se preocupe. Na medida em que você avança nos cursos sobre Python 3, vamos introduzir mais recursos.

Para declarar uma função, devemos usar a palavra chave `def` do mundo Python, seguida pelo nome da função. Lembrando que é consenso usar a nomenclatura _snake_case_:

```kotlin
def nome_da_funcao():
    # todo o código identado faz parte da função
    print("aprendendo funções")
```

Repare que uma função pode chamar uma outra função. `print` também é uma função e usamos ela dentro da nossa própria função.

## Executando funções

Para chamar a nossa própria função, usamos o nome dela seguido pelos parênteses, por exemplo:

```scss
nome_da_funcao()
```

Podemos chamar uma função quantas vezes quisermos:

```scss
nome_da_funcao()
nome_da_funcao()
nome_da_funcao()
```

Isso é a principal vantagem de funções, reaproveitar o código escrito nela!

## Parâmetros e retorno

Uma função também pode receber parâmetros e retornar algum valor, por exemplo:

```python
def soma(a, b):
     return a + b
```

A função `soma` recebe dois parâmetros (`a` e `b`) e retorna a soma. Ao chamar a função, podemos capturar o retorno:

```ini
s = soma(3, 4) 
```

Isso foi apenas uma pequena introdução, mas novamente, ainda vamos utilizar muito as funções e praticar para fixar o conteúdo.