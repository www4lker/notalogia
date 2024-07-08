---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/codigo-do-joguinho-monty-hall-em-python-raw/","tags":["python","meth","projeto","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# codigo do joguinho monty hall em python -  RAW

## criado em: 
-  02-06-2023 - 14:06

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/joguinho monty hall em python\|joguinho monty hall em python]]
- tags: #python #meth #projeto #ANELO
- Fontes & Links: 
[wikipedia article](https://en.wikipedia.org/wiki/Monty_Hall_problem)
[wired article](https://www.wired.com/story/monty-hall-problem-python/)
**[discussion within chatgpt](https://chat.openai.com/share/630c539d-f248-41d3-80af-4508744c36f6)**

---

Certainly! Here's an example code that implements the Monty Hall problem game without using any graphical user interface (GUI):

```python
import random

def play_monty_hall():
    print("Welcome to the Monty Hall Problem!")
    print("Choose a door and see if you win the prize!")
    print("----------------------------------------")

    doors = ["Goat", "Goat", "Goat"]  # The three doors with goats behind them
    prize_door = random.randint(0, 2)  # Randomly select the door with the prize

    # Player makes their initial choice
    player_choice = int(input("Choose a door (1, 2, or 3): ")) - 1

    # Monty opens a door with a goat
    monty_door = 0
    while monty_door == player_choice or monty_door == prize_door:
        monty_door += 1

    print("You chose Door", player_choice + 1)
    print("Monty opens Door", monty_door + 1)
    print()

    # Player decides whether to switch their choice
    switch = input("Do you want to switch your choice? (yes/no): ").lower()

    if switch == "yes":
        remaining_door = 3 - player_choice - monty_door
        player_choice = remaining_door

    # Display the final result
    print("Player chose Door", player_choice + 1)
    print("The prize was behind Door", prize_door + 1)

    if player_choice == prize_door:
        print("Congratulations! You won the prize!")
    else:
        print("Sorry, you did not win the prize.")

play_monty_hall()
```

To play the game, simply run the code. The program will prompt you to choose a door (1, 2, or 3). After you make your choice, Monty will open a door with a goat. Then, you will be asked if you want to switch your choice. Finally, the program will reveal the location of the prize and indicate whether you won or lost.

This code is a console-based version of the Monty Hall problem game. It uses the `random` module to select the prize door and simulate Monty's behavior. The player's choices and the game's results are displayed through console output.

Feel free to experiment with the code and run the game multiple times to see the probabilities in action!