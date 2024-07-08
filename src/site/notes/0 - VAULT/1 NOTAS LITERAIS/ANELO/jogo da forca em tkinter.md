---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/jogo-da-forca-em-tkinter/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# jogo da forca em tkinter

## criado em: 
- 04-06-2024
- 18:44
## relacionados:
- notas:
1. [[0 - VAULT/1 NOTAS LITERAIS/ANELO/JOGO DE PALAVRAS EM PYTHON\|JOGO DE PALAVRAS EM PYTHON]]
- tags: #ANELO 
- Fontes & Links: 
---

[[Aprenda poo com o porta da esperança \|Aprenda poo com o porta da esperança ]]

Claro! Vou explicar passo a passo como criar um jogo da forca em Python usando a biblioteca Tkinter para a interface gráfica. Aqui está um exemplo básico de implementação:

Passo 1: Configurando o ambiente
Certifique-se de ter o Python instalado em seu computador. Você também precisará instalar o Tkinter se ainda não tiver. Você pode fazer isso usando o gerenciador de pacotes pip. Abra o terminal e execute o seguinte comando:

```
pip install tkinter
```

Passo 2: Importando as bibliotecas
Vamos começar importando as bibliotecas necessárias: `Tkinter` para a interface gráfica e `random` para selecionar uma palavra aleatória do banco de palavras.

```python
import tkinter as tk
import random
```

Passo 3: Definindo as variáveis
Agora, vamos definir as variáveis que serão usadas no jogo:

```python
window = tk.Tk()
canvas = tk.Canvas(window, width=400, height=400)
canvas.pack()

# Palavras do banco de palavras
palavras = ['python', 'programacao', 'jogo', 'computador', 'teclado']

# Palavra selecionada para o jogo
palavra_secreta = random.choice(palavras)
letras_descobertas = ['_'] * len(palavra_secreta)

tentativas = 0
max_tentativas = 6
```

Passo 4: Criando as funções
Agora, vamos criar algumas funções para o jogo:

```python
def atualizar_palavrar_letra(letra):
    global tentativas
    if letra in palavra_secreta:
        for i in range(len(palavra_secreta)):
            if palavra_secreta[i] == letra:
                letras_descobertas[i] = letra
        atualizar_palavra()
    else:
        tentativas += 1
        atualizar_forca()

    if '_' not in letras_descobertas:
        lbl_mensagem['text'] = 'Parabéns! Você venceu!'
        desabilitar_teclado()

def atualizar_forca():
    if tentativas == 1:
        canvas.create_line(50, 350, 150, 350, width=5)
    elif tentativas == 2:
        canvas.create_line(100, 350, 100, 100, width=5)
    elif tentativas == 3:
        canvas.create_line(100, 100, 200, 100, width=5)
    elif tentativas == 4:
        canvas.create_line(200, 100, 200, 150, width=5)
    elif tentativas == 5:
        canvas.create_oval(180, 150, 220, 190, width=5)
    elif tentativas == 6:
        canvas.create_line(200, 190, 200, 250, width=5)
        lbl_mensagem['text'] = 'Game Over! A palavra era: ' + palavra_secreta
        desabilitar_teclado()

def desabilitar_teclado():
    for btn in botoes:
        btn['state'] = 'disabled'
```

Passo 5: Criando a interface gráfica
Agora, vamos criar a interface gráfica do jogo:

```python
lbl_palavra = tk.Label(window, text=' '.join(letras_descobertas),