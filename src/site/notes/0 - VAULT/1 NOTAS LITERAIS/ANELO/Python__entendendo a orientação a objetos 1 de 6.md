---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-entendendo-a-orientacao-a-objetos-1-de-6/","tags":["python","alura","poo","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Python__entendendo a orientação a objetos 1 de 6

## criado em: 
-  20-05-2023 - 10:44

### Conteúdo Relacionado
- notas: 
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python__entendendo a orientação a objetos 1 de 6\|Python__entendendo a orientação a objetos 1 de 6]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python__entendendo a orientação a objetos 2 de 6\|Python__entendendo a orientação a objetos 2 de 6]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python__entendendo a orientação a objetos 3 de 6\|Python__entendendo a orientação a objetos 3 de 6]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python__entendendo a orientação a objetos 4 de 6\|Python__entendendo a orientação a objetos 4 de 6]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python__entendendo a orientação a objetos 5 de 6\|Python__entendendo a orientação a objetos 5 de 6]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python__entendendo a orientação a objetos 6 de 6\|Python__entendendo a orientação a objetos 6 de 6]]
- tags: #python #alura #poo #ANELO 
- Fontes & Links: https://cursos.alura.com.br/formacao-Python-linguagem

---
## O problema do paradigma procedural


-   Apresentação
-   Dados da conta
-   Dados e comportamento
-   O paradigma OO
-   Procedural ou OO?
-   Boas-vindas?
-   Mãos na massa: Primeiros passos do projeto
-   O que aprendemos?
-   Arquivos do projeto atual

---


Como nos treinamentos anteriores, iremos utilizar o PyCharm como Python IDE, para nos auxiliar a implementar o código. Você pode baixá-lo [aqui](https://www.jetbrains.com/pycharm/download/).

## Criando o projeto

Crie o projeto **oo**, e se assegure que o Python 3 esteja selecionado no campo **_Interpreter_**. Com o projeto criado, crie o arquivo **teste.py**.

## Implementando o código

Para implementar o código visto nesta aula, siga os passos abaixo:

**1 -** Crie a função **`cria_conta`**, que recebe como argumento **`numero`**, **`titular`**, **`saldo`** e **`limite`**.

**2 -** Dentro dela, crie o dicionário **`conta`** com os argumentos da função e retorne-o no final da função.

**3 -** Crie a função **`deposita`**, que recebe como argumento a **`conta`** e o **`valor`** e adiciona o valor ao saldo da conta.

**4 -** Crie a função **`saca`**, que recebe como argumento a **`conta`** e o **`valor`** e subtrai o valor do saldo da conta.

**5 -** Crie a função **`extrato`**, que recebe como argumento a **`conta`** e imprime o seu saldo.


---

```python
def cria_conta(numero, titular, saldo, limite):
    conta = {"numero": numero, "titular": titular, "saldo": saldo, "limite": limite}
    return conta

def deposita(conta, valor):
    conta["saldo"] += valor

def saca(conta, valor):
    conta["saldo"] -= valor

def extrato(conta):
    print("Saldo {}".format(conta["saldo"]))
```

---

**O que aprendemos?**

Nesta aula, revisamos:

-   [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Dicionário\|Dicionário]]
-   [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Funções\|Funções]]
-   [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Encapsulamento de código\|Encapsulamento de código]]
