---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/codigo-do-joguinho-monty-hall-em-python-tkinter/","tags":["python","meth","projeto","tinker","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# codigo do joguinho monty hall em python -  TKINTER

## criado em: 
-  02-06-2023 - 14:04

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/joguinho monty hall em python\|joguinho monty hall em python]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/jogo portas da esperança final\|jogo portas da esperança final]]
- tags: #python #meth #projeto #tinker #ANELO
- Fontes & Links: 
[wikipedia article](https://en.wikipedia.org/wiki/Monty_Hall_problem)
[wired article](https://www.wired.com/story/monty-hall-problem-python/)
**[discussion updated within chatgpt](https://chat.openai.com/share/630c539d-f248-41d3-80af-4508744c36f6)**

---

Certainly! Here's an example code that implements the Monty Hall problem game using the Tkinter library in Python:

```python
import tkinter as tk
import random
from tkinter import messagebox

class MontyHallGame:
    def __init__(self):
        self.window = tk.Tk()
        self.window.title("Monty Hall Problem")
        self.prize_door = None
        self.player_choice = None
        self.monty_door = None

        self.create_widgets()

    def create_widgets(self):
        self.title_label = tk.Label(self.window, text="Monty Hall Problem", font=("Arial", 18, "bold"))
        self.title_label.pack(pady=10)

        self.instructions_label = tk.Label(self.window, text="Choose a door and see if you win the prize!", font=("Arial", 12))
        self.instructions_label.pack(pady=5)

        self.door_frame = tk.Frame(self.window)
        self.door_frame.pack(pady=10)

        self.door_buttons = []
        for i in range(3):
            door_button = tk.Button(self.door_frame, text="Door " + str(i+1), width=10, command=lambda door=i: self.open_door(door))
            door_button.grid(row=0, column=i, padx=5)
            self.door_buttons.append(door_button)

        self.result_label = tk.Label(self.window, text="", font=("Arial", 12, "bold"))
        self.result_label.pack(pady=10)

        self.play_again_button = tk.Button(self.window, text="Play Again", command=self.reset_game)
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

        messagebox.showinfo("Monty Hall Problem", "You chose Door " + str(self.player_choice+1) +
                            "\n\nMonty opens Door " + str(self.monty_door+1) +
                            "\n\nDo you want to switch your choice?")

        for door_button in self.door_buttons:
            door_button.config(state=tk.DISABLED)

        self.result_label.config(text="Player chose Door " + str(self.player_choice+1) +
                                      "\n\nMonty opened Door " + str(self.monty_door+1) +
                                      "\n\nThe prize was behind Door " + str(self.prize_door+1))

        self.show_final_result()

    def show_final_result(self):
        switch = messagebox.askyesno("Monty Hall Problem", "Do you want to switch your choice?")
        if switch:
            self.player_choice = [door for door in range(3) if door != self.player_choice and door != self.monty_door][0]

        if self.player_choice == self.prize_door:
            messagebox.showinfo("Monty Hall Problem", "Congratulations! You won the prize!")
        else:
            messagebox.showinfo("Monty Hall Problem", "Sorry, you did

 not win the prize.")

        for door_button in self.door_buttons:
            door_button.config(state=tk.NORMAL)

if __name__ == "__main__":
    game = MontyHallGame()
    game.window.mainloop()
```

Save the code in a Python file (e.g., `monty_hall_game.py`) and run it. A Tkinter window will appear with three buttons representing three doors. Click on a door to make your initial choice, and then Monty will open one of the other doors. After that, a message box will ask if you want to switch your choice. The final result will be displayed in the window, indicating whether you won or lost the prize.

This code uses Tkinter to create the game interface, handle button clicks, display messages, and reset the game. The logic of the Monty Hall problem is implemented in the `open_door` and `show_final_result` methods.

Note: This code assumes you have Tkinter installed. If you don't have it installed, you can install it using the command `pip install tkinter`.