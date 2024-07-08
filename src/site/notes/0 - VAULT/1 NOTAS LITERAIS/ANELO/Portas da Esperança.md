---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/portas-da-esperanca/","tags":["python","meth","projeto","tinker","poo","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# Portas da Esperança

## criado em: 
-  02-06-2023 - 15:33

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/readme  PdE\|readme  PdE]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/joguinho monty hall em python\|joguinho monty hall em python]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/jogo portas da esperança final\|jogo portas da esperança final]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Portas da Esperança\|Portas da Esperança]]
- tags: #python #meth #projeto #tinker #poo #ANELO 
- Fontes & Links: 
[wikipedia article](https://en.wikipedia.org/wiki/Monty_Hall_problem)
[wired article](https://www.wired.com/story/monty-hall-problem-python/)
**[discussion updated within chatgpt](https://chat.openai.com/share/cbb57177-f22e-4481-8046-182433f1f400)**
[codigo no github](https://github.com/www4lker/portas_da_esperanca)

---

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

        self.learn_more_button = tk.Button(self.window, text="Aprenda mais", command=self.show_learn_more)
        self.learn_more_button.pack(pady=5)

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
        score
        _text = f"Rodadas: {self.round_count}\nVitórias: {self.win_count}\nDerrotas: {self.loss_count}\nTrocas: {self.switch_count}\nManter: {self.stick_count}"
        self.score_label.config(text=score_text)

    def show_statistics(self):
        switch_win_percentage = (self.win_count / self.switch_count) * 100
        stick_win_percentage = ((self.win_count - self.switch_count) / self.stick_count) * 100

        statistics_text = f"Estatísticas após 500 rodadas:\n\nVitórias com troca: {switch_win_percentage:.2f}%\nVitórias sem troca: {stick_win_percentage:.2f}%"
        tk.messagebox.showinfo("Estatísticas", statistics_text)

    def show_learn_more(self):
        learn_more_window = tk.Toplevel(self.window)
        learn_more_window.title("Aprenda mais")

        explanation = (
            "O problema de Monty Hall é um problema de probabilidade que demonstra a importância "
            "de atualizar as probabilidades ao receber novas informações. A situação envolve três portas, "
            "atrás de uma das quais está um prêmio e atrás das outras duas, não há nada.\n\n"
            "Depois de escolher uma porta, Monty Hall (Esperança), que sabe o que está atrás de cada porta, abre uma "
            "das outras duas portas que não têm o prêmio. Em seguida, você tem a opção de manter sua escolha original "
            "ou mudar para a outra porta fechada restante.\n\n"
            "A ideia contraintuitiva é que trocar de porta aumenta suas chances de ganhar. "
            "Inicialmente, sua chance de escolher a porta correta é de 1/3, e há uma chance de 2/3 de estar atrás das outras duas portas. "
            "Quando Monty abre uma porta sem o prêmio, a probabilidade de 2/3 ainda se aplica às outras portas. "
            "Então, trocar sua escolha aumenta suas chances de ganhar para 2/3, enquanto manter sua escolha original tem apenas 1/3 de chance."
        )

        explanation_label = tk.Label(learn_more_window, text=explanation, justify=tk.LEFT, wraplength=450)
        explanation_label.pack(padx=15, pady=15)

if __name__ == "__main__":
    game = PortasDaEsperanca()
    game.window.mainloop()
	

```
