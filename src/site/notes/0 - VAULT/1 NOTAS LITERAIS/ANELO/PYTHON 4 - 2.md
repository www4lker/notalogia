---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-4-2/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# PYTHON 4 - 2
## Formatação de strings

## criado em: 
-  30-04-2023 - 12:34

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 4 - 1\|PYTHON 4 - 1]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 5 - 1\|PYTHON 5 - 1]]
- tags: #python #ANELO 
- Fontes & Links: 

---

## Transcrição

Com a lógica de tentativas implementada, vamos focar na impressão do número de tentativas para o usuário. Atualmente ela está assim:

```bash
print("Tentativa", rodada, "de", total_de_tentativas)
```

Desse jeito a frase é impressa do jeito que queremos, mas tem uma forma mais elegante de imprimir essa frase. Podemos deixar a string toda no código, dizendo onde que ela eventualmente pode mudar, no nosso caso é nos números. Onde a string pode mudar, colocamos **chaves** (**`{}`**):

```bash
print("Tentativa {} de {}")
```

As chaves significam que o Python deve substituí-las pelos valores das variáveis, então vamos passá-las:

```bash
print("Tentativa {} de {}", rodada, total_de_tentativas)
```

Se executarmos o programa, a seguinte frase é impressa:

```undefined
Tentativa {} de {} 1 3
```

Não é exatamente isso que queremos, as primeiras chaves devem receber o valor da rodada, e as segundas o total de tentativas. Para isso funcionar, devemos chamar uma função baseada nessa string, a função **`format`**, passando para ela as variáveis que devem ficar no lugar das chaves:

```lua
print("Tentativa {} de {}".format(rodada, total_de_tentativas))
```

Podemos testar e ver que agora está tudo funcionando como antes! O que acabamos de fazer se chama **interpolação de strings**, muito comum nas linguagens e que nos oferece recursos da string para fazermos essas substituições.

Assim o nosso código fica um pouco mais elegante, já que nele vemos a string inteira, sabendo exatamente onde ela será alterada.