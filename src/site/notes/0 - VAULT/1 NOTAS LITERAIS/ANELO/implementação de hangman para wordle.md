---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/implementacao-de-hangman-para-wordle/","tags":["python","chatgpt","gamedev","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# implementação de hangman para wordle

## criado em: 
-  12-05-2023 - 10:38

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/o que é e como usar FLASK\|o que é e como usar FLASK]]
- tags: #python #chatgpt #gamedev #ANELO 
- Fontes & Links: [léxico em portugues br](https://github.com/fserb/pt-br)

---

To make the game more like Wordle and less like Forca (Hangman), you can limit the number of guesses and show partial progress to the player. You can also add more words to the external word file and improve the design to make it more enjoyable to play with friends. Here's an updated version of the code with these improvements:

```python
import random


def jogar():
    abertura_jogo()
    palavra_secreta = carrega_palavra_secreta()
    letras_acertadas = inicializa_letras_corretas(palavra_secreta)

    enforcou = False
    acertou = False
    tentativas_restantes = 6

    print(letras_acertadas)

    while not enforcou and not acertou:
        chute = pede_palpite()

        if chute in palavra_secreta:
            indexa_chute_correto(chute, letras_acertadas, palavra_secreta)
        else:
            tentativas_restantes -= 1
            print(f"Tentativas restantes: {tentativas_restantes}")

        enforcou = tentativas_restantes == 0
        acertou = "_" not in letras_acertadasprint(letras_acertadas)

    if acertou:
        imprime_mensagem_vencedor()
    else:
        imprime_mensagem_perdedor(palavra_secreta)
    

# funções
def abertura_jogo():
    print("*********************************")
    print("***Bem vindo ao jogo da Forca!***")
    print("*********************************")


def carrega_palavra_secreta():
    arquivo = open("palavras.txt", "r")
    palavras = []

    for linha in arquivo:
        linha = linha.strip()
        palavras.append(linha)

    arquivo.close()

    numero = random.randrange(0, len(palavras))
    palavra_secreta = palavras[numero].upper()
    return palavra_secreta


def inicializa_letras_corretas(palavra):
    return ["_" for letra in palavra]


def pede_palpite():
    chute = input("Qual o seu palpite de letra? ")
    chute = chute.strip().upper()
    return chute


def indexa_chute_correto(chute, letras_acertadas, palavra_secreta):
    index = 0
    for letra in palavra_secreta:
        if chute == letra:letras_acertadas[index] = letra
        index += 1


def imprime_mensagem_vencedor():
    print("Você ganhou!!")


def imprime_mensagem_perdedor(palavra_secreta):
    print("Você perdeu!!")
    print(f"A palavra secreta era: {palavra_secreta}")


if __name__ == "__main__":
    jogar()
```

To add more words to the external word file, just open the `palavras.txt` file and add more words, each on a new line. The game will automatically pick up the new words when it starts.

To make the game more enjoyable and shareable, you can create a simple web interface using a web framework like Flask. This will allow you to easily share the game with friends by hosting it on a server or a platform like Heroku. Alternatively, you can create a desktop application using a GUI library like Tkinter or PyQt. This way, you can distribute the game as an executable file that your friends can download and play.

---

Wordle likely uses a curated list of 5-letter words that are common, non-technical, and not obscure, yet challenging enough for the game. To create such a list, you can start with a larger list of words and filter it based on specific criteria.

Here's a possible approach:

1. Obtain a comprehensive list of 5-letter words. You can find several word lists online, such as [SCOWL (Spell Checker Oriented Word Lists)](http://wordlist.aspell.net/).

2. Filter out technical and obscure words using frequency data. You can use resources like the [Google Books Ngram Viewer](https://books.google.com/ngrams) to obtain word frequency data. This will help you identify words that are less common and more likely to be technical or obscure.

3. Remove words with offensive or inappropriate meanings.

4. Manually review and refine the list. It's important to go through the list and remove any words that may not be suitable for the game. This step will help ensure that the list is well-curated and enjoyable for players.

5. Store the curated list in a text file, database, or other formats suitable for your implementation.

In your game implementation, you can then load the curated list of words and randomlychoose one for each game, just like you're doing now with the `palavras.txt` file. The refined list should provide a more enjoyable and challenging experience for players.

Here's an example of how you can filter words using Python:

```python
def filter_words(word_list, min_frequency):
    filtered_words = []
    for word in word_list:
        frequency = get_word_frequency(word)  # Implement this function to get the word frequency
        if frequency >= min_frequency:
            filtered_words.append(word)
    return filtered_words


def get_word_frequency(word):
    # Implement this function using a resource like Google Books Ngram Viewer or another frequency database.
    pass
```

You can use this filtering approach along with other criteria to create a well-curated list of 5-letter words for your Wordle-like game.

---

Here are some simple ideas to improve your game:

1. Display the number of attempts remaining with a visual representation like a hangman image or a progress bar.

2. Allow the player to choose the difficulty level. You could create multiple word lists for different difficulty levels, with easy words having more common letters and hard words having less common letters.

3. Provide hints to the player after a certain number of incorrect guesses. For example, reveal the meaning or a synonym of the secret word.

4. Track the player's score, such as the number of games won or the total number of guesses. You can display the score at the end of the game and store it in a local file to keep a record of the player's performance.

5. Implement a timer to add a time-based challenge to the game. Give the player a limited amount of time to guess the word.

6. Add a "give up" option that allows the player to reveal the secret word and start a new game.

7. Use color-coded text to indicate correct and incorrect guesses. For example, display correct guesses in green and incorrect guesses in red.

8. Allow players to enter full-word guesses. If they guess the entire word correctly, they win the game immediately. If their full-word guess is incorrect, they lose one attempt.

These improvements should be relatively simple to implement and will make your game more enjoyable and engaging for players. Choose the ideas that you find most interesting and start implementing them one by one. As you gain more experience, you can continue to refine and expand your game. Good luck!