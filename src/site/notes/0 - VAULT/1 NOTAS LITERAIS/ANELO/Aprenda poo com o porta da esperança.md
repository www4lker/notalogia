---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/aprenda-poo-com-o-porta-da-esperanca/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# Aprenda poo com o porta da esperança

## criado em: 
- 04-06-2024
- 18:03
## relacionados:
- notas:
1. [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Portas da Esperança\|Portas da Esperança]]
2. [[0 - VAULT/1 NOTAS LITERAIS/ANELO/jogo portas da esperança final\|jogo portas da esperança final]]
- tags: #ANELO
- Fontes & Links: 
---

This code demonstrates the famous Monty Hall problem using a graphical user interface (GUI) created with the tkinter library in Python. Let's break down the main concepts involved:

1. **Class**: The code defines a class called `PortasDaEsperanca`, which represents the game of "Porta da Esperança" (Door of Hope).

2. **Constructor**: The `__init__` method is the constructor of the class. It initializes various instance variables, sets up the GUI window, and creates the necessary widgets.

3. **Widgets**: The game interface consists of labels, buttons, and message boxes. Labels (`Label` widget) display text, buttons (`Button` widget) handle user interactions, and message boxes (`messagebox` module) show informative dialogs.

4. **Lists**: The code uses a list called `door_buttons` to store the buttons representing the doors in the GUI. The buttons are created in a loop and appended to this list.

5. **Loop**: The `for` loop is used to create the door buttons dynamically. It iterates over the range from 0 to 2, creating three buttons in total.

6. **Event Handling**: The `command` parameter in the button creation assigns a function to be called when the button is clicked. It uses a lambda function to pass the loop variable `i` as an argument to the `open_door` method.

7. **Randomness**: The `random` module is used to introduce randomness in the game. The `random.randint()` function is used to randomly assign a prize to one of the three doors, and the `random.choice()` function is used to select a door that Silvio (a character in the game) opens.

8. **Instance Variables**: The class has several instance variables, such as `prize_door`, `player_choice`, `silvio_door`, and various counters (`switch_count`, `stick_count`, `win_count`, `loss_count`, `round_count`). These variables store and update the game state during different stages of the game.

9. **Methods**: The class defines various methods to handle different aspects of the game, such as creating widgets, opening doors, showing dialogs, updating scores, displaying statistics, and more.

10. **Object Creation**: The code creates an instance of the `PortasDaEsperanca` class called `game`. The `mainloop()` function is called on the window to start the game's GUI and event handling.

Overall, this code demonstrates the use of object-oriented programming (OOP) principles in Python, such as encapsulating related data and functionality within a class, creating and manipulating objects of that class, and using class methods to perform specific tasks. It also showcases the use of various Python libraries, such as tkinter for GUI development and random for generating random numbers.