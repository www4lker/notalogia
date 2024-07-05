---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-7-2/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON 7 - 2

## criado em: 
-  30-04-2023 - 16:35

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 7 - 1\|PYTHON 7 - 1]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 8 - 1\|PYTHON 8 - 1]]
- tags: #python #ANELO 
- Fontes & Links: 

---

Com os níveis definidos, vamos agora calcular uma pontuação. Ela funcionará da seguinte maneira, o usuário começa o jogo com 1000 pontos, e a cada rodada que ele não acerta o número secreto, ele perderá pontos. Quanto mais distante for o chute, mais pontos o usuário irá perder. Por exemplo, se o número secreto for 40, e o usuário chutar 20, ele irá perder 20 pontos, que corresponde à distância entre os valores.

Vamos começar definindo a variável com 1000 pontos:

```ini
pontos = 1000
```

Após isso, o usuário irá perder pontos caso ele erre o chute, logo temos que implementar isso dentro da condição **`else`**:

```bash
if (acertou):
    print("Você acertou!")
    break
else:
    if (maior):
        print("Você errou! O seu chute foi maior que o número secreto.")
    elif (menor):
        print("Você errou! O seu chute foi menor que o número secreto.")
```

Vamos definir a variável **`pontos_perdidos`**, que subtrai o chute do número secreto:

```bash
if (acertou):
    print("Você acertou!")
    break
else:
    if (maior):
        print("Você errou! O seu chute foi maior que o número secreto.")
    elif (menor):
        print("Você errou! O seu chute foi menor que o número secreto.")
    pontos_perdidos = numero_secreto - chute
```

Depois, vamos subtrair os pontos perdidos da pontuação total:

```bash
if (acertou):
    print("Você acertou!")
    break
else:
    if (maior):
        print("Você errou! O seu chute foi maior que o número secreto.")
    elif (menor):
        print("Você errou! O seu chute foi menor que o número secreto.")
    pontos_perdidos = numero_secreto - chute
    pontos = pontos - pontos_perdidos
```

Isso funciona caso o usuário chute um número menor que o número secreto, mas e se for maior? Por exemplo, se o número secreto for 40 e o usuário chutar 60, de acordo com o cálculo do nosso código os pontos perdidos serão **-20**, e ao subtrair esse valor da pontuação total, ela irá aumentar!

Então queremos fazer a subtração dos pontos perdidos, mas caso essa subtração tenha como resultado um número negativo, queremos que "esquecer" esse sinal, queremos sempre o **número absoluto**.

E para extrair o número absoluto, existe mais uma função _built-in_, a **`abs()`**:

```python
if (acertou):
    print("Você acertou!")
    break
else:
    if (maior):
        print("Você errou! O seu chute foi maior que o número secreto.")
    elif (menor):
        print("Você errou! O seu chute foi menor que o número secreto.")
    pontos_perdidos = abs(numero_secreto - chute)
    pontos = pontos - pontos_perdidos
```

Por fim, falta exibirmos a pontuação final ao usuário. Vamos alterar a mensagem de acerto do usuário, acrescentando a pontuação total. Faremos uso novamente da interpolação de strings:

```python
if (acertou):
    print("Você acertou e fez {} pontos!".format(pontos))
    break
else:
    if (maior):
        print("Você errou! O seu chute foi maior que o número secreto.")
    elif (menor):
        print("Você errou! O seu chute foi menor que o número secreto.")
    pontos_perdidos = abs(numero_secreto - chute)
    pontos = pontos - pontos_perdidos
```

Com isso chegamos ao final do nosso jogo! No próximo capítulo veremos um pouco sobre linguagens compiladas e interpretadas, entre outros assuntos. Até lá!