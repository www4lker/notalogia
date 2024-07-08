---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/js-e-html-colirio-no-olho/","tags":["javascript","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# js e html - colirio no olho

## criado em: 
-  29-03-2023 - 14:53

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/JS e HTML - LOGICA DE PROGRAMAÇÃO -  FINAL\|JS e HTML - LOGICA DE PROGRAMAÇÃO -  FINAL]]
- tags: #javascript  #ANELO 
- Fontes & Links: 

---

Nesta aula aprenderemos a criar um jogo com mais complexidade.

Como podemos observar, na tela branca temos apenas a imagem de um alvo vermelho, formado por três círculos, uma esfera vermelha central, um círculo branco exterior, e por fim, um círculo vermelho.

Este alvo se move aleatoriamente na tela, pulando entre as posições dentro do `<canvas>`. Ou seja, se estamos falando de aleatoriedade, lembrando das aulas anteriores, sabemos que temos o recurso do `Math.random`, com o qual podemos gerar coordenadas para os eixos X e Y.

O alvo, a cada `1` segundo ou milissegundo, é plotado em diversas posições na tela. Sendo assim, há uma função para desenhar o alvo, em determinados intervalos de tempo, e o fará com base em posições aleatórias.

O objetivo do jogo é que o usuário clique no alvo antes que este desapareça. Ao clicar no centro do alvo, surge um pop up com a mensagem "acertou!". Clicando em qualquer outro lugar da tela resulta em erro.

É um jogo simples, no qual utilizaremos o raciocínio lógico e alguns conceitos de elaboração de jogos. Assim, você será capaz de criar suas próprias brincadeiras.

Nas próximas aulas passaremos pelo processo de criação, passo a passo.