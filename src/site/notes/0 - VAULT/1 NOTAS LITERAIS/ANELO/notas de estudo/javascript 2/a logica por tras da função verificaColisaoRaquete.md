---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-2/a-logica-por-tras-da-funcao-verifica-colisao-raquete/","tags":["LLM","chatgpt"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# a logica por tras da função verificaColisaoRaquete

## criado em: 
-  26-03-2023 - 15:51

### Conteúdo Relacionado
- notas: 
- tags: #LLM #chatgpt
- Fontes & Links: https://cursos.alura.com.br/course/pong-javascript/task/56100

---

Explain the logic of it: 

```
function verificaColisaoRaquete(){ if (xBolinha - raio < xRaquete + raqueteComp && xBolinha + raio > xRaquete && yBolinha - raio < yRaquete + raqueteAlt && yBolinha + raio > yRaquete){ velocidadeXbolinha *= -1; }
```


The `verificaColisaoRaquete()` function contains a collision detection logic to determine if the ball has collided with the paddle.

The collision detection logic consists of checking if the ball is within the bounds of the paddle.

The first condition `xBolinha - raio < xRaquete + raqueteComp` checks if the left side of the ball is to the left of the right side of the paddle.

The second condition `xBolinha + raio > xRaquete` checks if the right side of the ball is to the right of the left side of the paddle.

The third condition `yBolinha - raio < yRaquete + raqueteAlt` checks if the top side of the ball is above the bottom side of the paddle.

The fourth condition `yBolinha + raio > yRaquete` checks if the bottom side of the ball is below the top side of the paddle.

If all four conditions are true, it means that the ball is within the bounds of the paddle, and a collision has occurred. In this case, the `velocidadeXbolinha` variable is multiplied by -1 to reverse the direction of the ball in the x-axis.