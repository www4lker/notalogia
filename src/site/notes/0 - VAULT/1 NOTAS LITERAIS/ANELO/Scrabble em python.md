---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/scrabble-em-python/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Scrabble em python

## criado em: 
-  24-05-2023 - 09:27

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Scrabble em python 2\|Scrabble em python 2]]
- tags: #ANELO 
- Fontes & Links: 

---
```python

import random

letter_distribution = {
    'A': 14, 'B': 3, 'C': 4, 'Ç': 2, 'D': 5, 'E': 11, 'F': 2, 'G': 2, 'H': 2, 'I': 10,
    'J': 2, 'L': 5, 'M': 6, 'N': 4, 'O': 10, 'P': 4, 'Q': 1, 'R': 6,
    'S': 8, 'T': 5, 'U': 7, 'V': 2, 'X': 1, 'Z': 1, '*': 3 # peças brancas
}

letter_scores = {
    'A': 1, 'B': 3, 'C': 2, 'Ç': 3,'D': 2, 'E': 1, 'F': 4, 'G': 2, 'H': 4, 'I': 1,
    'J': 5, 'L': 2, 'M': 1, 'N': 3, 'O': 1, 'P': 2, 'Q': 6, 'R': 1,
    'S': 1, 'T': 1, 'U': 1, 'V': 4, 'X': 8, 'Z': 8
}

# funções
# Create a function to initialize the player's rack with random letters:

def initialize_rack():
    rack = []
    while len(rack) < 7:
        letter = random.choice(list(letter_distribution.keys()))
        if letter_distribution[letter] > 0:
            letter_distribution[letter] -= 1
            rack.append(letter)
    return rack


# Create a function to calculate the score for a given word:

def calculate_score(word):
    score = 0
    for letter in word:
        score += letter_scores[letter]
    return score


# Set up a loop to keep the game running until a player decides to quit:

while True:
    player_rack = initialize_rack()
    print("Your rack:", player_rack)
    
    word = input("Enter a word (or 'q' to quit): ").upper()
    
    if word == 'Q':
        break
    
    # Check if the letters of the word are present in the player's rack
    
    rack_copy = player_rack.copy()
    valid_word = True
    for letter in word:
        if letter in rack_copy:
            rack_copy.remove(letter)
        else:
            valid_word = False
            break
    
    if not valid_word:
        print("Invalid word. Try again.")
        continue
    
    score = calculate_score(word)
    print("Score:", score)
    
    # Update the player's rack with new letters
    new_letters = initialize_rack()
    player_rack += new_letters
    
    print("New rack:", player_rack)



```

[[0 - VAULT/1 NOTAS LITERAIS/ANELO/Scrabble em python 2\|Scrabble em python 2]]