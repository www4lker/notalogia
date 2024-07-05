---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-8-3/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON 8 - 3

## criado em: 
-  30-04-2023 - 17:09

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 9 - 1\|PYTHON 9 - 1]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/def inindo funções\|def inindo funções]]
- tags: #python #ANELO 
- Fontes & Links: 

---

Não conseguimos mais jogar diretamente cada jogo porque o seu próprio arquivo não chama a sua função **`jogar()`**. Então, depois da função, vamos chamá-la:

```python
# adivinhacao.py

import random

def jogar():
    # código omitido

jogar()
```

Isso resolve o problema de jogar o jogo diretamente mas voltamos ao problema do vídeo anterior! Ao executarmos o arquivo **jogos.py**, como o próprio arquivo **adivinhacao.py** chama a função **`jogar()`**, ela será executada sem que queiramos isso.

Precisamos dar um jeito para que, quando executarmos o jogo de adivinhação diretamente, a função **`jogar()`** deve ser chamada, mas quando só o importamos, não queremos que a função seja chamada.

## Programa principal vs Programa importado

Quando rodamos diretamente um arquivo no Python, ele internamente cria uma variável e a preenche. E através dessa variável podemos fazer uma consulta, pois se ela estiver preenchida, significa que o arquivo foi executado diretamente, mas se a variável não estiver preenchida, então significa que o arquivo só foi importado.

Essa variável é a **`__name__`**, e ela é preenchida com o valor **`__main__`** caso o arquivo seja executado diretamente. Vamos então fazer **`if`** para verificar se ela está preenchida ou não:

```cpp
# adivinhacao.py

import random

def jogar():
    # código omitido

if (__name__ == "__main__"):
    jogar()
```

Podemos agora testar os dois casos, executar o arquivo diretamente e executar o arquivo **jogos.py**. Os dois estão funcionando, exatamente como queríamos. Falta fazermos a mesma coisa com o jogo da forca:

```ruby
# forca.py

def jogar():
    # código omitido

if (__name__ == "__main__"):
    jogar()
```

E com o arquivo **jogos.py**, colocando o seu código dentro da função **`escolhe_jogo()`** e chamando-a caso o programa seja o programa principal:

```markdown
import forca
import adivinhacao

def escolhe_jogo():
    print("*********************************")
    print("*******Escolha o seu jogo!*******")
    print("*********************************")

    print("(1) Forca (2) Adivinhação")

    jogo = int(input("Qual jogo? "))

    if (jogo == 1):
        print("Jogando forca")
        forca.jogar()
    elif (jogo == 2):
        print("Jogando adivinhação")
        adivinhacao.jogar()

if (__name__ == "__main__"):
    escolhe_jogo()
```

Com isso vimos como diferenciar se o programa é o principal ou não, se ele está sendo executado diretamente ou só sendo importado. Na hora de importar um arquivo, ele lê o código da função, mas não o executa, pois ele não é o arquivo principal