---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-avancando-na-linguagem-1-de-7/","tags":["python","ALURA","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON AVANÇANDO NA LINGUAGEM - 1 DE 7

## criado em: 
-  10-05-2023 - 21:27

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON - COMEÇANDO COM A LINGUAGEM - ALURA\|PYTHON - COMEÇANDO COM A LINGUAGEM - ALURA]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON - 1 de 9\|PYTHON - 1 de 9]]
- tags: #python #ALURA #ANELO 

---
Prontos para começar mais um treinamento sobre **Python 3**?

Nesse curso, vamos implementar mais um jogo, mas dessa vez um **Jogo da Forca**, que é mais desafiador do que o jogo de adivinhação que criamos no treinamento anterior.

Aprenderemos novas estruturas de dados, **listas** e **tuplas**, entre outras sequências. Veremos também **leitura e escrita de arquivos**, além de organizar melhor o nosso código através de **funções**.

Vamos começar?

---

![Pasted image 20230510213259.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230510213259.png)

Agora já temos tudo pronto. Podemos desenvolver o nosso **Jogo da Forca**.

## Conhecendo o jogo

O jogo da forca também é um jogo de adivinhação, mas no caso o usuário deve adivinhar uma **palavra secreta**. No arquivo **forca.py**, já há a função **`jogar`** definida, onde ficará o código do nosso jogo:

```scss
def jogar():
    print("*********************************")
    print("***Bem vindo ao jogo da Forca!***")
    print("*********************************")

    print("Fim do jogo")
```

E caso executemos o programa como programa principal, executamos essa função **`jogar`**. Verificamos isso através de um **`if`**:

```scss
if(__name__ == "__main__"):
    jogar()
```

## Definindo a palavra secreta

Como no jogo devemos adivinhar uma palavra secreta, nada mais justo do que defini-la em uma variável. Por enquanto a palavra será fixa, com o nome de **banana**:

```scss
def jogar():
    print("*********************************")
    print("***Bem vindo ao jogo da Forca!***")
    print("*********************************")

    palavra_secreta = "banana"

    print("Fim do jogo")
```

Mais à frente deixaremos essa palavra secreta mais dinâmica.

## Primeiros passos do jogo

Agora, enquanto o usuário estiver jogando, devemos ficar verificando se o usuário acertou a palavra secreta ou se ele perdeu (se "enforcou"), mas devemos fazer isso em quantas iterações?

O usuário continua jogando enquanto ele não acertar a palavra e enquanto ele ainda tiver tentativas para acertar a palavra, ou seja, enquanto ele não "se enforcar". Para representar esse loop, já conhecemos o **`while`**:

```bash
palavra_secreta = "banana"

while(não acertou E não enforcou):
    print("Jogando...")
```

Mas o que colocamos como condição do `while`, está em português e não existe em Python, logo isso não funcionará.

No caso de se enforcar, podemos ter dois valores, ou o usuário se enforcou, ou não. Logo, podemos ter os valores **verdadeiro** ou **falso**.

## O tipo bool

Nas linguagens de programação, e no Python não é diferente, há um tipo específico para representar esses valores, o tipo **`bool`**. Ele pode ter os valores **`True`** (**Verdadeiro**) e **`False`** (**Falso**). Então vamos definir uma variável **`enforcou`**, que começará com o valor **`False`**:

```python
palavra_secreta = "banana"

enforcou = False

while(não acertou E não enforcou):
    print("Jogando...")
```

Criaremos também a variável **`acertou`**, que representa se o usuário acertou ou não a palavra. Ela também começará com o valor **`False`**, pois quando o jogo começa, o usuário ainda não acertou a palavra secreta:

```python
palavra_secreta = "banana"

enforcou = False
acertou = False

while(não acertou E não enforcou):
    print("Jogando...")
```

Agora podemos modificar a condição do **`while`**, mas a condição é **não** acertar a palavra e **não** se enforcar. Para representar o **não**, no Python existe a palavra chave de negação, o **`not`**. E para representar o **`E`**, existe o operador lógico **`and`**:

```python
palavra_secreta = "banana"

enforcou = False
acertou = False

while(not acertou and not enforcou):
    print("Jogando...")
```

Então, enquanto não acertamos a palavra e enquanto não nos enforcamos, continuamos jogando.