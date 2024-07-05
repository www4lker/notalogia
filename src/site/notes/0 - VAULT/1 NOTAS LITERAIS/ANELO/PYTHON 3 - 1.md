---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-3-1/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON 3 - 1
## A condição elif

## criado em: 
-  30-04-2023 - 11:38

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 4 - 1\|PYTHON 4 - 1]]
- tags: #python #ANELO 
- Fontes & Links: 

---

No capítulo anterior começamos a implementar o jogo, vimos como capturar os dados digitados pelo usuário, como converter o valor e como fazer um **`if`** para saber se o usuário acertou ou não.

Nesse capítulo, vamos fazer com que o usuário possa dar vários chutes para tentar acertar o número, já que atualmente ele só tem uma tentativa. Mas antes disso, vamos implementar uma dica para o usuário, dizendo se o número que ele chutou é maior ou menor que o número secreto.

Para isso, precisamos mexer no bloco do **`else`**. Vamos ter que testar novamente, se o número for maior, imprimimos uma mensagem dizendo isso ao usuário, se for menos, diremos ao usuário que o número digitado é menor que o número secreto:

```bash
if (numero_secreto == chute):
    print("Você acertou!")
else:
    if (chute > numero_secreto):
        print("Você errou! O seu chute foi maior que o número secreto.")
    if (chute < numero_secreto):
        print("Você errou! O seu chute foi menor que o número secreto.")
```

Podemos testar e ver que tudo está funcionando perfeitamente.

## else com condição de entrada

Podemos notar que, se o chute não for igual, nem maior que o número secreto, obviamente ele será menor, então o último `if` não é necessário:

```bash
if (numero_secreto == chute):
    print("Você acertou!")
else:
    if (chute > numero_secreto):
        print("Você errou! O seu chute foi maior que o número secreto.")
    else:
        print("Você errou! O seu chute foi menor que o número secreto.")
```

Mas para esses casos, podemos fazer um **`else`** com uma **condição de entrada**, o **`elif`**. Vamos utilizá-lo para deixar o código mais semântico, já que na prática não há diferença:

```bash
if (numero_secreto == chute):
    print("Você acertou!")
else:
    if (chute > numero_secreto):
        print("Você errou! O seu chute foi maior que o número secreto.")
    elif (chute < numero_secreto):
        print("Você errou! O seu chute foi menor que o número secreto.")
```

## Melhorando a legibilidade do código

Podemos melhorar a legibilidade do nosso código, para que outros programadores que possam vir a desenvolver conosco o entendam melhor. Vamos deixar nossas condições mais claras, o que significa **`chute == numero_secreto`**, por exemplo? Que o usuário acertou, logo vamos extrair essa condição para uma variável:

```bash
acertou = chute == numero_secreto

if (acertou):
    print("Você acertou!")
else:
    if (chute > numero_secreto):
        print("Você errou! O seu chute foi maior que o número secreto.")
    elif (chute < numero_secreto):
        print("Você errou! O seu chute foi menor que o número secreto.")
```

Agora a condição **`if`** fica um pouco mais clara. Vamos fazer a mesma coisa para as outras duas condições:

```bash
acertou = chute == numero_secreto
maior = chute > numero_secreto
menor = chute < numero_secreto

if (acertou):
    print("Você acertou!")
else:
    if (maior):
        print("Você errou! O seu chute foi maior que o número secreto.")
    elif (menor):
        print("Você errou! O seu chute foi menor que o número secreto.")
```

Podemos testar e ver que tudo continua funcionando como antes, mas agora com um código um pouco mais legível. No próximo vídeo implementaremos a chance do usuário poder dar vários chutes para tentar acertar o número secreto. Até lá!
