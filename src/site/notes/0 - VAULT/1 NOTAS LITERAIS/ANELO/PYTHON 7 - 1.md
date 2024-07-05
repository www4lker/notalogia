---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-7-1/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON 7 - 1
### Adicionando níveis ao jogo

## criado em: 
-  30-04-2023 - 16:26

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 6 - 2\|PYTHON 6 - 2]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 7 - 2\|PYTHON 7 - 2]]
- tags: #python #ANELO 
- Fontes & Links: 

---

Vamos adicionar níveis ao nosso jogo, e conforme o nível vai ficando mais difícil, menos tentativas o usuário terá.

Começaremos perguntando ao usuário qual nível de dificuldade ele quer:

```markdown
import random

print("*********************************")
print("Bem vindo ao jogo de Adivinhação!")
print("*********************************")

numero_secreto = random.randrange(1, 101)
total_de_tentativas = 3

print("Qual o nível de dificuldade?")
print("(1) Fácil (2) Médio (3) Difícil")

# resto do código comentado
```

E capturaremos o que ele digitar, já convertendo o valor para inteiro e guardando em uma variável:

```markdown
import random

print("*********************************")
print("Bem vindo ao jogo de Adivinhação!")
print("*********************************")

numero_secreto = random.randrange(1, 101)
total_de_tentativas = 3

print("Qual o nível de dificuldade?")
print("(1) Fácil (2) Médio (3) Difícil")

nivel = int(input("Defina o nível: "))

# resto do código comentado
```

Agora falta mudar o total de tentativas baseado no nível que o usuário escolher. A variável será inicializada com 0, e faremos um **`if`** para verificar o nível escolhido, se o ele for fácil, o usuário terá 20 tentativas, se for médio terá 10, e se for difícil terá 5 tentativas:

```markdown
import random

print("*********************************")
print("Bem vindo ao jogo de Adivinhação!")
print("*********************************")

numero_secreto = random.randrange(1, 101)
total_de_tentativas = 0

print("Qual o nível de dificuldade?")
print("(1) Fácil (2) Médio (3) Difícil")

nivel = int(input("Defina o nível: "))

if (nivel == 1):
    total_de_tentativas = 20
elif (nivel == 2):
    total_de_tentativas = 10
else:
    total_de_tentativas = 5

# resto do código comentado
```

Com isso conseguimos definir os níveis de dificuldade no nosso jogo. No próximo vídeos definiremos pontuação!