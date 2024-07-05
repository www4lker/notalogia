---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-8-1/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON 8 - 1

## criado em: 
-  30-04-2023 - 17:07

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 7 - 2\|PYTHON 7 - 2]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 8 - 2\|PYTHON 8 - 2]]
- tags: #python #ANELO 
- Fontes & Links: 

---

Se conseguimos executar o jogo dentro do PyCharm, também conseguimos rodar o jogo na linha de comando, no terminal. Dentro do diretório do projeto **jogos**, basta executar:

```undefined
python3 adivinhacao.py
```

No próximo treinamento, criaremos mais um jogo, a **forca**. Então já vamos deixar o seu arquivo preparado, criando o **forca.py**, também dentro do projeto **jogos**. Dentro desse arquivo, vamos deixar as mensagens de início e fim de jogo, semelhante ao jogo de adivinhação:

```markdown
print("*********************************")
print("***Bem vindo ao jogo da Forca!***")
print("*********************************")

print("Fim do jogo")
```

## Oferecendo todos os jogos ao usuário

Vamos oferecer os dois jogos ao usuário, ou seja, devemos perguntar ao usuário qual jogo ele quer executar, jogar. Mas onde vamos colocar essa funcionalidade? A ideia é não misturar os jogos, deixar cada um em um arquivo separado. Então vamos criar um novo arquivo com essa funcionalidade, o arquivo **jogos.py**, perguntando qual jogo ele quer escolher jogar:

```markdown
print("*********************************")
print("*******Escolha o seu jogo!*******")
print("*********************************")

print("(1) Forca (2) Adivinhação")
```

Agora vamos capturar a opção do usuário e verificar qual jogo ele escolheu:

```markdown
print("*********************************")
print("*******Escolha o seu jogo!*******")
print("*********************************")

print("(1) Forca (2) Adivinhação")

jogo = int(input("Qual jogo? "))

if (jogo == 1):
    print("Jogando forca")
elif (jogo == 2):
    print("Jogando adivinhação")
```

## Importando arquivos

Ótimo, mas se queremos chamar um arquivo dentro de outro, precisamos importá-lo, algo parecido com o que fizemos com o módulo **`random`**:

```markdown
import forca
import adivinhacao

print("*********************************")
print("*******Escolha o seu jogo!*******")
print("*********************************")

print("(1) Forca (2) Adivinhação")

jogo = int(input("Qual jogo? "))

if (jogo == 1):
    print("Jogando forca")
elif (jogo == 2):
    print("Jogando adivinhação")
```

## O problema do import

Podemos executar para ver como está ficando:

```markdown
*********************************
***Bem vindo ao jogo da Forca!***
*********************************
Fim do jogo
*********************************
Bem vindo ao jogo de Adivinhação!
*********************************
Qual o nível de dificuldade?
(1) Fácil (2) Médio (3) Difícil
Defina o nível:
```

Ué, o que aconteceu? Quando importamos um arquivo no Python, ele o executa! Podemos reparar que ele executou o arquivo **forca.py** e logo depois o **adivinhacao.py**. Mas obviamente não queremos isso, só queremos executar o arquivo quando nós quisermos! 


