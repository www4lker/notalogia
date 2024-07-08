---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-4-1/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# PYTHON 4 - 1
## O laço com while

## criado em: 
-  30-04-2023 - 12:03

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 3 - 1\|PYTHON 3 - 1]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 4 - 2\|PYTHON 4 - 2]]
- tags: #python #ANELO 
- Fontes & Links: 

---

## Transcrição

Queremos dar mais de uma oportunidade para o usuário tentar acertar o número secreto, já que é um jogo de adivinhação. A primeira ideia é repetir o código, desde a função `input` até o bloco do `elif`. Ou seja, para cada nova tentativa que quisermos dar ao usuário, copiaríamos esse código novamente.

Só que copiar código sempre é uma má prática, queremos escrever o nosso código apenas uma vez, e **repeti-lo**. Se queremos repetir o código, faremos um **laço**, ou um **_loop_**. O laço que queremos fazer é:

```python
enquanto ainda há tentativas:
    chute_str = input("Digite o seu número: ")
    print("Você digitou: ", chute_str)
    chute = int(chute_str)

    acertou = numero_secreto == chute
    maior = chute > numero_secreto
    menor = chute < numero_secreto

    if (acertou):
        print("Você acertou!")
    else:
        if (maior):
            print("Você errou! O seu chute foi maior que o número secreto.")
        elif (menor):
            print("Você errou! O seu chute foi menor que o número secreto.")

print("Fim do jogo")
```

Só que o Python não entende português, então vamos traduzi-lo. A palavra **tentativas** será uma variável, chamaremos-a de **`total_de_tentativas`**:

```makefile
total_de_tentativas = 3

enquanto ainda há total_de_tentativas:
    executa o código
```

A palavra **enquanto** no Python é o **`while`**, e assim como o **`if`**, ele recebe uma condição. A diferença é que o **`if`**, caso a condição seja verdadeira, executa apenas uma vez o código do seu bloco, já o **`while`** executa **enquanto** a condição for verdadeira:

```r
total_de_tentativas = 3

while (ainda há total_de_tentativas):
    executa o código
```

Resta agora a expressão **ainda há**. A ideia é que o usuário tenha 3 tentativas, representada no código pela variável **`total_de_tentativas`**. A cada rodada subtraímos **1** do valor dessa variável, até o valor chegar a **0**, que é quando devemos sair do **`while`**, logo vamos executá-lo enquanto a variável _`total_de_tentativas` **for maior que** 0*_:

```python
total_de_tentativas = 3

while (total_de_tentativas > 0):
    chute_str = input("Digite o seu número: ")
    print("Você digitou: ", chute_str)
    chute = int(chute_str)

    acertou = numero_secreto == chute
    maior = chute > numero_secreto
    menor = chute < numero_secreto

    if (acertou):
        print("Você acertou!")
    else:
        if (maior):
            print("Você errou! O seu chute foi maior que o número secreto.")
        elif (menor):
            print("Você errou! O seu chute foi menor que o número secreto.")

print("Fim do jogo")
```

A condição está perfeita, falta, dentro do laço, subtrairmos 1 da variável **`total_de_tentativas`**:

```python
total_de_tentativas = 3

while (total_de_tentativas > 0):
    chute_str = input("Digite o seu número: ")
    print("Você digitou: ", chute_str)
    chute = int(chute_str)

    acertou = numero_secreto == chute
    maior = chute > numero_secreto
    menor = chute < numero_secreto

    if (acertou):
        print("Você acertou!")
    else:
        if (maior):
            print("Você errou! O seu chute foi maior que o número secreto.")
        elif (menor):
            print("Você errou! O seu chute foi menor que o número secreto.")

    total_de_tentativas = total_de_tentativas - 1

print("Fim do jogo")
```

Testamos o código e ótimo, ele funciona! Mas pode ficar ainda melhor.

## Representando a rodada

Vamos imprimir para o usuário qual o número da rodada que ele está jogando, para deixar claro quantas tentativas ele tem. Para isso vamos criar a variável **`rodada`**, que começa com o valor **1**:

```ini
total_de_tentativas = 3
rodada = 1
```

E vamos imprimi-la antes do usuário digitar o seu chute:

```lua
total_de_tentativas = 3
rodada = 1

while (total_de_tentativas > 0):
    print("Tentativa", rodada, "de", total_de_tentativas)
    chute_str = input("Digite o seu número: ")

    # restante do código comentado
```

E para a variável **`total_de_tentativas`** continuar com o valor **3**, não vamos mais subtrair 1 do seu valor, e sim adicionar 1 ao valor da variável **`rodada`**:

```python
total_de_tentativas = 3
rodada = 1

while (total_de_tentativas > 0):
    print("Tentativa", rodada, "de", total_de_tentativas)
    chute_str = input("Digite o seu número: ")
    print("Você digitou: ", chute_str)
    chute = int(chute_str)

    acertou = numero_secreto == chute
    maior = chute > numero_secreto
    menor = chute < numero_secreto

    if (acertou):
        print("Você acertou!")
    else:
        if (maior):
            print("Você errou! O seu chute foi maior que o número secreto.")
        elif (menor):
            print("Você errou! O seu chute foi menor que o número secreto.")

    rodada = rodada + 1

print("Fim do jogo")
```

Por fim, precisamos modificar a condição, como o **`total_de_tentativas`** permanecerá com o valor 3, o código precisa ficar executando enquanto o valor da rodada for menor ou igual ao total de tentativas:

```lua
total_de_tentativas = 3
rodada = 1

while (rodada <= total_de_tentativas):
    print("Tentativa", rodada, "de", total_de_tentativas)
    chute_str = input("Digite o seu número: ")

    # restante do código comentado
```

Agora conseguimos imprimir para o usuário quantas tentativas restantes ele possui!