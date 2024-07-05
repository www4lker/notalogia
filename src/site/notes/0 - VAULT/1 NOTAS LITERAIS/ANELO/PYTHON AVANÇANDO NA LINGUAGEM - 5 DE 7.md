---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-avancando-na-linguagem-5-de-7/","tags":["python","alura","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON AVANÇANDO NA LINGUAGEM - 5 DE 7
## implementamos o encerramento do jogo

## criado em: 
-  11-05-2023 - 16:19

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON AVANÇANDO NA LINGUAGEM - 1 DE 7\|PYTHON AVANÇANDO NA LINGUAGEM - 1 DE 7]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON AVANÇANDO NA LINGUAGEM - 2 DE 7\|PYTHON AVANÇANDO NA LINGUAGEM - 2 DE 7]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON AVANÇANDO NA LINGUAGEM - 4 DE 7\|PYTHON AVANÇANDO NA LINGUAGEM - 4 DE 7]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON AVANÇANDO NA LINGUAGEM - 6 DE 7\|PYTHON AVANÇANDO NA LINGUAGEM - 6 DE 7]]- 
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Docker e Containers\|Docker e Containers]]
- tags: #python #alura #ANELO 

---
# Estipulando tentativas de erros

Agora vamos dar continuidade ao nosso jogo, pois ele ainda não está totalmente funcional, pois ao acertar a palavra secreta, o jogo ainda fica pedindo que o usuário digite uma letra:

```css
*********************************
***Bem vindo ao jogo da Forca!***
*********************************
['_', '_', '_', '_', '_', '_']
Qual letra? b
['b', '_', '_', '_', '_', '_']
Qual letra? a
['b', 'a', '_', 'a', '_', 'a']
Qual letra? n
['b', 'a', 'n', 'a', 'n', 'a']
Qual letra? 
```

O contrário também acontece, podemos errar várias vezes, até digitar quase o alfabeto inteiro, se quisermos. Ou seja, o usuário possui infinitas tentativas para descobrir a palavra, já que não há um limite de tentativas.

## Encerrando o jogo quando o usuário errar seis vezes

Como os valores das variáveis **`enforcou`** e **`acertou`** nunca mudam, o loop é infinito. Logo, precisamos mudar os seus valores de acordo com situações do jogo.

Vamos começar com a variável **`enforcou`**. Quando é que o usuário se enforca? Vamos definir que é quando o jogador errar 6 vezes, então precisamos contar esses erros. Logo, vamos declarar uma variável **`erros`** e inicializá-la com o valor **`0`**:

```ini
enforcou = False
acertou = False
erros = 0
```

Agora, se o usuário errou, nós incrementamos a variável. Para tal, precisamos realizar um teste. Vamos testar se o chute está na palavra secreta, se estiver nós executamos o código que posiciona a letra na lista, etc. Mas se o chute não estiver na palavra secreta, incrementamos a variável **`erros`**:

```perl
while (not acertou and not enforcou):

    chute = input("Qual letra? ")
    chute = chute.strip()

    if (chute in palavra_secreta):
        index = 0
        for letra in palavra_secreta:
            if (chute.upper() == letra.upper()):
                letras_acertadas[index] = letra
            index = index + 1
    else:
        erros = erros + 1

    print(letras_acertadas)
```

Ao final do **`while`**, vamos verificar se a variável **`erros`** é igual a **6** e atribuir esse booleano (**`true`** ou **`false`**) à variável **`enforcou`**:

```perl
while (not acertou and not enforcou):

    chute = input("Qual letra? ")
    chute = chute.strip()

    if (chute in palavra_secreta):
        index = 0
        for letra in palavra_secreta:
            if (chute.upper() == letra.upper()):
                letras_acertadas[index] = letra
            index = index + 1
    else:
        erros = erros + 1

    enforcou = erros == 6
    print(letras_acertadas)
```

Agora, ao executarmos o jogo e errar 6 vezes, o jogo é encerrado! Para melhorar ainda mais o nosso código, podemos seguir a dica do PyCharm e realizar o incremento das variáveis **`index`** e **`erros`** da seguinte forma:

```lua
while (not acertou and not enforcou):

    chute = input("Qual letra? ")
    chute = chute.strip()

    if (chute in palavra_secreta):
        index = 0
        for letra in palavra_secreta:
            if (chute.upper() == letra.upper()):
                letras_acertadas[index] = letra
            index += 1
    else:
        erros += 1

    enforcou = erros == 6
    print(letras_acertadas)
```

O resultado é o mesmo.

## Palavra secreta e chute sempre em caixa alta

Mas agora, se testarmos um chute com letra maiúscula?

```markdown
*********************************
***Bem vindo ao jogo da Forca!***
*********************************
['_', '_', '_', '_', '_', '_']
Qual letra? B
['_', '_', '_', '_', '_', '_']
Qual letra? 
```

Ué, já não tínhamos resolvido isso? Acontece que no **`if`** que acabamos de escrever, nós não fazemos a comparação do chute com as letras em caixa alta. Para não termos que sempre nos lembrar disso, vamos já definir a palavra secreta e o chute em letra maiúsculas. Assim, nas comparações não precisamos mais deixar todas as letras em caixa alta. O código ficará assim:

```python
def jogar():

    print("*********************************")
    print("***Bem vindo ao jogo da Forca!***")
    print("*********************************")

    palavra_secreta = "banana".upper()
    letras_acertadas = ["_", "_", "_", "_", "_", "_"]

    enforcou = False
    acertou = False
    erros = 0

    print(letras_acertadas)

    while (not acertou and not enforcou):

        chute = input("Qual letra? ")
        chute = chute.strip().upper()

        if (chute in palavra_secreta):
            index = 0
            for letra in palavra_secreta:
                if (chute == letra):
                    letras_acertadas[index] = letra
                index += 1
        else:
            erros += 1

        enforcou = erros == 6
        print(letras_acertadas)

    print("Fim do jogo")
```

Por fim, falta encerrarmos o jogo quando o jogador acertar a palavra.

## Encerrando o jogo quando o usuário acertar a palavra

Uma das maneiras de implementar essa funcionalidade é aproveitar a nossa lista de letras acertadas, já que enquanto o jogador não acertar a palavra, o caractere **`_`** vai existir na lista.

Logo, enquanto a lista possui o **`_`**, significa que a palavra ainda **não** foi totalmente preenchida, já que os **`_`** são substituídos a cada letra acertada. Então vamos adicionar essa verificação abaixo da verificação da variável **`enforcou`**:

```ini
enforcou = erros == 6
acertou = "_" not in letras_acertadas
```

Ao testar, e acertar a palavra, temos o seguinte resultado:

```css
*********************************
***Bem vindo ao jogo da Forca!***
*********************************
['_', '_', '_', '_', '_', '_']
Qual letra? b
['B', '_', '_', '_', '_', '_']
Qual letra? a
['B', 'A', '_', 'A', '_', 'A']
Qual letra? n
['B', 'A', 'N', 'A', 'N', 'A']
Fim do jogo
```

O jogo é encerrado ao acertarmos a palavra! Ótimo, funcionalidade concluída. Falta apenas exibir uma mensagem ao usuário, dizendo se ele acertou ou não a palavra. Após o **`while`**, adicionamos:

```bash
if (acertou):
    print("Você ganhou!")
else:
    print("Você perdeu!")
```

No próximo vídeo iremos melhorar a declaração da quantidade de **`_`** na lista de palavras acertadas, já que por enquanto a mesma está fixa.

# Para saber mais: outra maneira de sair do loop

Vimos nesse capítulo que as variáveis `acertou` e `enforcou` foram usadas para controlar a saída do loop. Enquanto elas não forem verdadeiras, o código dentro do loop será executado. Para que o loop seja encerrado, criamos atribuições para essas variáveis.

```ini
enforcou = erros == 6
acertou = "_" not in letras_acertadas
```

Contudo, essa não é única maneira de sair de um loop. Podemos usar também a palavra reservada **break** que, quando executada, irá encerrar o loop naquele ponto. Como podemos alterar nosso código da forca para utilizar o `break` e sair do _while_?

Uma possível solução seria o código abaixo. Repare que usamos um **loop infinito** (`while(true)`) e por isso temos que usar o comando `break` para interromper o laço:

```scss
def jogar():
    print("*********************************")
    print("***Bem vindo ao jogo da Forca!***")
    print("*********************************")

    palavra_secreta = "maça".upper()
    letras_acertadas = ["_", "_", "_", "_"]


    erros = 0
    print(len(palavra_secreta))
    print(letras_acertadas)

    while(True):

        chute = input("Qual letra? ")
        chute = chute.strip().upper()

        if(chute in palavra_secreta):
            index = 0
            for letra in palavra_secreta:
                if(chute == letra):
                    letras_acertadas[index] = letra
                index += 1
        else:
            erros += 1

        if (erros == 6):
            break
        if ("_" not in letras_acertadas):
            break
        print(letras_acertadas)


    if("_" not in letras_acertadas):
        print("Você ganhou!!")
    else:
        print("Você perdeu!!")
    print("Fim do jogo")
```

# compreensão de lista

Atualmente, a nossa palavra secreta é **banana**, que possui seis letras. Por isso a lista de palavras acertadas possui seis **`_`**. Mas se trocarmos a palavra secreta? Precisamos alterar a quantidade de **`_`** na lista, de acordo com o número de letras da nova palavra.

Meio trabalhoso, né? Então vamos tornar isso mais dinâmico.

## Inicializando a lista de acordo com o número de letras da palavra

Queremos que a inicialização da lista de palavras acertadas seja dinâmica, baseada na quantidade de letras que houver na palavra secreta. Já sabemos implementar isso, podemos criar a lista vazia, e para cada letra na palavra secreta, adicionamos um **`_`** à ela:

```makefile
palavra_secreta = "banana".upper()
letras_acertadas = []

for letra in palavra_secreta:
    letras_acertadas.append("_")
```

Perfeito, está funcionando! Mas há uma forma mais interessante de fazer isso.

## Realizando um laço dentro da inicialização da lista

Quando inicializamos a lista, queremos inicializá-la com um caractere **`_`** para cada letra na palavra secreta. Só que com Python, podemos fazer isso diretamente, dentro da inicialização da lista:

```ini
palavra_secreta = "banana".upper()
letras_acertadas = ["_" for letra in palavra_secreta]
```

#### Para saber mais: inicializando uma lista de números pares

Essa funcionalidade do Python se chama **_List Comprehension_**, em português, _Compreensão de lista_.

O recurso _List Comprehension_ também permite utilizar condições para o preenchimento da lista. Considere o objetivo de inicializar uma lista com os números pares a partir de uma lista de números inteiros qualquer, por exemplo, os números 1,3,4,5,7,8,9. Para descobrir se um número é par, usamos a condição `numero%2 == 0`, que verifica se o resto de uma divisão por 2 é zero. O código abaixo usa um loop para inicializar a lista de pares.

```makefile
inteiros = [1,3,4,5,7,8,9]
pares = []
for numero in inteiros:
    if numero % 2 == 0:
        pares.append(numero)
```

Pesquise como o podemos usar o _List Comprehension_ para fazer o mesmo que o código acima.

---

Dado o código de geração da lista de pares abaixo:

```makefile
inteiros = [1,3,4,5,7,8,9]
pares = []
for numero in inteiros:
    if numero % 2 == 0:
        pares.append(numero)
```

O código usando _List Comprehension_ relativo ficaria muito mais enxuto:

```ini
inteiros = [1,3,4,5,7,8,9]
pares = [x for x in inteiros if x % 2 == 0]
```

Repare o `if` depois do `for` que define a condição! Muito melhor não?

_List Comprehension_ é um dos recursos mais legais da linguagem Python :)