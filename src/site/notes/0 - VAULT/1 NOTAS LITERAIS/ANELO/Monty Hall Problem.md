---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/monty-hall-problem/","tags":["python","meth","projeto","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Monty Hall Problem

## criado em: 
-  02-06-2023 - 13:18

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/joguinho monty hall em python\|joguinho monty hall em python]]
- tags: #python #meth #projeto #ANELO 
- Fontes & Links: 
[wikipedia article](https://en.wikipedia.org/wiki/Monty_Hall_problem)
[wired article](https://www.wired.com/story/monty-hall-problem-python/)
**[discussion within chatgpt](https://chat.openai.com/share/630c539d-f248-41d3-80af-4508744c36f6)**

---

Let's break down the two code snippets from the article in a beginner-friendly manner, providing context and storytelling to help understand their meaning and implications.

# first snippet

The first code snippet simulates the Monty Hall problem when the contestant sticks with their original choice and does not switch doors. The code uses a random number generator to simulate the selection of the prize door and the contestant's initial choice. It then compares the two choices, and if they match, it counts it as a win. The process is repeated for a specified number of trials (in this case, 1000), and at the end, the code calculates the win percentage by dividing the number of wins by the total number of trials.

This code aims to show that when the contestant sticks with their initial choice and does not switch doors, the win percentage tends to be around 33%. This result aligns with the theoretical probability of winning, which is 1 out of 3 or approximately 33%. By running this code, it helps us understand that not switching doors in the Monty Hall problem does not improve the chances of winning.

```python

Web VPython 3.2

n = 0
N = 1000


n1win=0

while n<N: 
  prize = int(random()*3)
  choice = int(random()*3)
  if prize==choice:
    n1win = n1win + 1
  n = n + 1

print("number of trials = ",n)
print("win percentage = ",n1win*100/n," percent")

```

## second snippet

Now, let's move on to the second code snippet, which simulates the Monty Hall problem when the contestant switches doors after Monty reveals one of the losing doors. This code introduces more complexity compared to the previous one. It uses functions and additional logic to handle the switching of choices.

```python

Web VPython 3.2

n = 0
N = 1000 #number of trials


#counter for wins
n2win=0

#function to switch choices
def switchy(thing):
  #takes a two element list and switches it
  if thing[0]==1:
    thing[0]=0
    thing[1]=1
  elif thing[1]==1:
    thing[0]=1
    thing[1]=0
  return(thing)

#function to check win
def win(drs, choic):
  #looks at two lists to see if there is a win
  if drs[0]==choic[0]:
    return(True)
  else:
    return(False)


while n<N: 
  #reset doors and choices
  doors =[0,0,0]
  choice=[0,0,0]
  #set the door prize
  prize = int(random()*3)
  doors[prize]=1
  #pick the door
  pick1 = int(random()*3)
  choice[pick1]=1
  
#this picks which door to open
  if prize==choice:
    if prize==0:
      doors.pop(1)
      choice.pop(1)
    if prize==1:
      doors.pop(2)
      choice.pop(2)
    if prize==2:
      doors.pop(0)
      choice.pop(0)
  else:
    for i in range(3):
      if doors[i]==0 and choice[i]==0:
        doors.pop(i)
        choice.pop(i)
        break()

#this is the new choice
  choice2 = switchy(choice)

#check for a win
  if win(doors,choice2):
    n2win = n2win + 1

      
  n = n + 1


print("percent win = ",n2win*100/n)
print("theoretical percent = ",2*100/3)




```

Similar to the first snippet, this code also performs a specified number of trials (again, 1000) to simulate the game. In each trial, it randomly assigns the location of the prize door and the contestant's initial choice. Then, based on these choices, it determines which door Monty should open, following the rules of the game. After Monty opens the door, the code switches the contestant's choice to the remaining unopened door. Finally, it checks if the switched choice corresponds to the door with the prize and counts it as a win if it does.

![Pasted image 20230602135930.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230602135930.png)

By running this code, it demonstrates that when the contestant switches doors after Monty reveals a losing door, the win percentage tends to be around 67%, which is significantly higher than the win percentage in the previous code snippet. This result aligns with the theoretical probability of winning if the contestant switches, which is 2 out of 3 or approximately 67%. Thus, it reinforces the importance of switching choices in the Monty Hall problem to improve the chances of winning.

# conclusion

The significance of these code snippets, along with the contextual understanding of the Monty Hall problem, highlights the importance of being rational and not giving in to biased ideas or intuitive judgments. Our intuition may lead us to believe that sticking with the initial choice or randomly picking between the remaining doors yields the same probability of winning. However, the simulations clearly demonstrate that switching doors provides a higher probability of winning.

These code snippets, therefore, serve as a powerful visual representation of the underlying probabilities involved in the Monty Hall problem. By relying on rational decision-making and understanding the principles of probability, individuals can make informed choices and increase their chances of success, even in situations that may initially seem counterintuitive.
