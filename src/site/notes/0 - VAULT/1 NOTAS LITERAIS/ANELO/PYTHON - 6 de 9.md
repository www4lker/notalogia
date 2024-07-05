---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-6-de-9/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON - 6 de 9

## criado em: 
-  27-04-2023 - 13:04

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON - 4 e 5 de 9\|PYTHON - 4 e 5 de 9]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON - 10 de 9\|PYTHON - 10 de 9]]
- tags: #python #ANELO 
- Fontes & Links: 

---

## FUNÇÃO PRINT E VARIÁVEIS


Antes de criarmos um projeto, veremos como trabalhar no console do Python.

## A função print

Já vimos no vídeo anterior como imprimir uma mensagem:

```bash
print("ola mundo")
```

**Resultado**

```undefined
ola mundo
```

Vamos analisar mais a fundo essa função. No console do Python temos uma função de ajuda, a função **`help()`**:

```scss
help()
```

Podemos reparar que um novo console aparece:

```bash
help>
```

Agora, como queremos saber mais sobre a função **`print`**, vamos digitá-la:

```bash
help(print)
```

![Documentação da função print](https://s3.amazonaws.com/caelum-online-public/python3/img/01/help-print.png)

Inicialmente, o que nos importa são os três primeiros valores que a função **`print`** pode receber:

-   **`value`** é o valor que queremos imprimir, as reticências indicam que a função pode receber mais de um valor, basta separá-los por vírgula.
-   **`sep`** é o separador entre os valores, por padrão o separador é um espaço em branco.
-   **`end`** é o que acontecerá ao final da função, por padrão há uma quebra de linha, uma nova linha (**`\n`**).

Podemos apertar a tecla **Q** para sair da documentação da função e **CTRL + C** ou **CTRL + D** para sair do console de ajuda do Python. De volta ao console do próprio Python, podemos testar a função **`print`** com os valores que vimos:

```bash
print("Brasil", "ganhou", 5, "titulos mundiais", sep="-")
```

**Resultado**

```undefined
Brasil-ganhou-5-titulos mundiais
```

Como modificamos o separador, agora os valores são separador por um hífen. Vamos testar o **`end`** agora, não passando nada para ele:

```lua
print("Brasil", "ganhou", 5, "titulos mundiais", end="")
```

**Resultado**

```undefined
Brasil ganhou 5 titulos mundiais>>>
```

Uma nova linha não é criada, ou seja, o que colocarmos dentro do **`end`** será impresso ao final da função.

## Variáveis

Agora queremos flexibilizar a função, queremos poder imprimir outros países, como Itália, Alemanha, Argentina... Para isso teremos que mudar o nome do país e o número de títulos conquistados. Então vamos **definir o valor com o nome do país fora da função `print`**. Vamos definir uma **variável** para o nome do país, já que o seu valor pode variar:

```ini
pais = "Italia"
```

Definimos uma variável e atribuímos a ela um valor. Assim como fizemos com o nome do país, vamos fazer também com a quantidade de títulos:

```ini
pais = "Italia"
quantidade = 4
```

Com as variáveis definidas, podemos refazer a função `print`, só que dessa vez passando as variáveis no lugar dos antigos valores:

```makefile
pais = "Italia"
quantidade = 4
print(pais, "ganhou", quantidade, "titulos mundiais")
```

**Resultado**

```undefined
Italia ganhou 4 titulos mundiais
```

Agora a mensagem é impressa no mesmo molde da anterior, só que dessa vez com variáveis! Mas qual é o tipo dessas variáveis? O tipo da variável depende do valor que passamos para ela. Podemos "perguntar" para a variável qual é o seu tipo, passando-a para a função **`type`**:

```scss
type(pais)
type(quantidade)
```

**Resultado**

```kotlin
<class 'str'>
<class 'int'>
```

O valor **`str`** significa que a variável é do tipo **string**, já que o seu valor está entre aspas duplas. E **`int`** significa que a variável é do tipo **inteiro**, já que passamos um valor inteiro para a variável.

Veremos mais sobre os tipos das variáveis no próximo vídeo, até lá!