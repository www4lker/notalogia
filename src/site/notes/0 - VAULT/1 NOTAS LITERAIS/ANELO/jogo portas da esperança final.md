---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/jogo-portas-da-esperanca-final/","tags":["python","meth","projeto","tinker","poo","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Jogo Portas da Esperança final

## criado em: 
-  02-06-2023 - 15:04

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/joguinho monty hall em python\|joguinho monty hall em python]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/jogo portas da esperança final\|jogo portas da esperança final]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Portas da Esperança\|Portas da Esperança]]
- tags: #python #meth #projeto #tinker #poo #ANELO 
- Fontes & Links: 
[wikipedia article](https://en.wikipedia.org/wiki/Monty_Hall_problem)
[wired article](https://www.wired.com/story/monty-hall-problem-python/)
**[discussion updated within chatgpt](https://chat.openai.com/share/630c539d-f248-41d3-80af-4508744c36f6)**


---


Here's an explanation of the object-oriented programming (OOP) concepts used in the given code:

1. **Classes and Objects:** The code defines a class called `PortasDaEsperanca`, which represents the game itself. Objects (instances) of this class can be created, such as `game = PortasDaEsperanca()`, to encapsulate the game's state and behavior.

2. **Attributes and Methods:** Within the `PortasDaEsperanca` class, there are attributes (variables) like `prize_door`, `player_choice`, `monty_door`, `switch_count`, `stick_count`, etc., which hold the game's current state. There are also methods (functions) like `create_widgets`, `open_door`, `show_dialog`, `show_final_result`, etc., which define the behavior and actions of the game.

3. **Constructor (`__init__`):** The `__init__` method is a special method that gets called when an object is created. In the code, it initializes the game's state, sets up the initial GUI elements, and initializes various counters.

4. **Encapsulation:** The class encapsulates the game's state and behavior, keeping related attributes and methods together. This helps organize the code and makes it easier to understand and maintain.

5. **Inheritance:** The code does not demonstrate inheritance explicitly. However, in larger projects, you might have multiple classes related to different aspects of the game, such as a `Player` class or a `Door` class, which could inherit common attributes or methods from a base class like `GameObject`.

6. **Event-Driven Programming:** The code uses event-driven programming, where actions are triggered by user interactions (button clicks). The code specifies callback functions (`command`) for buttons, which are executed when the buttons are clicked.

Understanding these concepts will provide a solid foundation for working with this code and developing similar projects using object-oriented programming principles. It's also beneficial to learn about topics like inheritance, polymorphism, and class design patterns, but they are not essential for understanding and extending this specific code.

```python

import tkinter as tk

import random

from tkinter import messagebox

  

class PortasDaEsperanca:

    def __init__(self):

        self.window = tk.Tk()

        self.window.title("Portas da Esperança")

        self.prize_door = None

        self.player_choice = None

        self.monty_door = None

        self.switch_count = 0

        self.stick_count = 0

        self.win_count = 0

        self.loss_count = 0

        self.round_count = 0

  

        self.create_widgets()

  

    def create_widgets(self):

        self.title_label = tk.Label(self.window, text="Portas da Esperança", font=("Arial", 18, "bold"))

        self.title_label.pack(pady=10)

  

        self.instructions_label = tk.Label(self.window, text="Escolha uma porta e veja se ganha o prêmio!", font=("Arial", 12))

        self.instructions_label.pack(pady=5)

  

        self.door_frame = tk.Frame(self.window)

        self.door_frame.pack(pady=10)

  

        self.door_buttons = []

        for i in range(3):

            door_button = tk.Button(self.door_frame, text="Porta " + str(i+1), width=10, command=lambda door=i: self.open_door(door))

            door_button.grid(row=0, column=i, padx=5)

            self.door_buttons.append(door_button)

  

        self.result_label = tk.Label(self.window, text="", font=("Arial", 12, "bold"))

        self.result_label.pack(pady=10)

  

        self.score_label = tk.Label(self.window, text="", font=("Arial", 12))

        self.score_label.pack(pady=5)

  

        self.play_again_button = tk.Button(self.window, text="Jogar Novamente", command=self.reset_game)

        self.play_again_button.pack(pady=5)

  

    def reset_game(self):

        self.prize_door = None

        self.player_choice = None

        self.monty_door = None

        self.result_label.config(text="")

        for door_button in self.door_buttons:

            door_button.config(state=tk.NORMAL)

  

    def open_door(self, door):

        self.player_choice = door

        self.prize_door = random.randint(0, 2)

  

        remaining_doors = [0, 1, 2]

        remaining_doors.remove(self.prize_door)

  

        if self.player_choice in remaining_doors:

            remaining_doors.remove(self.player_choice)

  

        self.monty_door = random.choice(remaining_doors)

        remaining_doors.remove(self.monty_door)

  

        self.door_buttons[self.monty_door].config(state=tk.DISABLED)

  

        tk.messagebox.showinfo("Portas da Esperança", f"Esperança abriu a Porta {self.monty_door + 1}.")

        self.show_dialog()

  

    def show_dialog(self):

        dialog = tk.Toplevel(self.window)

        dialog.title("Mudar Escolha")

  

        message_label = tk.Label(dialog, text="Você quer mudar sua escolha?")

        message_label.pack(pady=10)

  

        yes_button = tk.Button(dialog, text="Sim", command=self.switch_choice)

        yes_button.pack(side=tk.LEFT, padx=10)

  

        no_button = tk.Button(dialog, text="Não", command=self.stick_choice)

        no_button.pack(side=tk.LEFT, padx=10)

  

    def switch_choice(self):

        self.switch_count += 1

        remaining_door = 3 - self.player_choice - self.monty_door

        self.player_choice = remaining_door

        self.window.after(200, self.show_final_result)

  

    def stick_choice(self):

        self.stick_count += 1

        self.window.after(200, self.show_final_result)

  

    def show_final_result(self):

        self.round_count += 1

        won = self.player_choice == self.prize_door

  

        if won:

            self.win_count += 1

        else:

            self.loss_count += 1

  

        self.result_label.config(text="Jogador escolheu Porta " + str(self.player_choice+1) +

                                      "\n\nEsperança abriu a Porta " + str(self.monty_door+1) +

                                      "\n\nO prêmio estava atrás da Porta " + str(self.prize_door+1))

  

        if won:

            tk.messagebox.showinfo("Portas da Esperança", "Parabéns! Você ganhou o prêmio!")

        else:

            tk.messagebox.showinfo("Portas da Esperança", "Desculpe, você não ganhou o prêmio.")

  

        self.update_score()

        if self.round_count == 500:

            self.show_statistics()

  

        for door_button in self.door_buttons:

            door_button.config(state=tk.NORMAL)

  

    def update_score(self):

        score_text = f"Rodadas: {self.round_count}\nVitórias: {self.win_count}\nDerrotas:{self.loss_count}\nTrocas: {self.switch_count}\nManter: {self.stick_count}"

        self.score_label.config(text=score_text)

  

    def show_statistics(self):

        switch_win_percentage = (self.win_count / self.switch_count) * 100

        stick_win_percentage = ((self.win_count - self.switch_count) / self.stick_count) * 100

  

        statistics_text = f"Estatísticas após 500 rodadas:\n\nVitórias com troca: {switch_win_percentage:.2f}%\nVitórias sem troca: {stick_win_percentage:.2f}%"

        tk.messagebox.showinfo("Estatísticas", statistics_text)

  

if __name__ == "__main__":

    game = PortasDaEsperanca()

    game.window.mainloop()


```