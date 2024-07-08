---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/o-que-sao-vetores/","tags":["design","illustrator","teoria","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# o que são vetores

## criado em: 
-  15-04-2023 - 09:56

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/curso basico illustrator 1\|curso basico illustrator 1]]
- tags: #design #illustrator #teoria #ANELO 
- Fontes & Links:  https://cursos.alura.com.br/course/adobe-illustrator-conhecendo-ferramenta/task/122785

---

>Vetores são imagens construídas por coordenadas matemáticas. Eles são compostos por pontos âncora ou nós, que são ligados entre si por caminhos que dão forma aos objetos. Cada ponto possui uma posição definida nos eixos x (horizontal) e y (vertical) do plano de trabalho e determinam a direção do caminho. Diferentemente de imagens bitmap, que são compostas por pixels e perdem qualidade ao serem ampliadas, os vetores podem ser ampliados infinitamente sem perder a qualidade da imagem.

No último vídeo abrimos o Illustrator e tivemos o primeiro contato com o programa. Durante a ambientação eu comentei que o software é especializado no **desenho vetorial**. Mas afinal, o que são vetores?

## Imagem digital

Na prática, os desenhos vetoriais são baseados em **caminhos**, que se conectam por meio dos chamados "nós" ou "pontos-âncora". Cada um desses pontos possui uma posição definida nos eixos x (horizontal) e y (vertical) do plano de trabalho e que determinam a direção do caminho.

![Text alt: Imagem de uma letra A desenhada sobre uma malha de pequenos quadrados. Junto aos pontos de início e fim das linhas que constituem a letra há marcações com círculos acompanhados das posições nos eixos X e Y.](https://caelum-online-public.s3.amazonaws.com/2984-illustrator/aula+1/Img1.png)

O desenho de uma letra A, por exemplo, quando feito com vetores é composto por pontos que possuem posições no espaço, nos eixos x e y, levando em conta o início e o fim deles. A partir desses pontos surgem os caminhos que dão forma aos vetores, que neste caso são as linhas verticais inclinadas e a haste horizontal. Ou seja, o que vemos na tela é construído por meio de cálculos matemáticos, que se traduzem em tempo real em instruções para produção de linhas, curvas e formas preenchidas.

Por serem baseados em vetores, esses gráficos geralmente são mais leves (ocupam menos espaço de armazenamento) e não perdem qualidade ao serem ampliados, já que as funções matemáticas adequam-se facilmente à escala, o que não ocorre com gráficos _bitmap_. Além disso, no desenho vetorial é possível trabalhar criando objetos independentes entre si que fazem parte da mesma composição.

![Text alt: Gif animado de uma ilustração vetorial de uma pessoa em pé mexendo no celular. O desenho é separado em diferentes partes que antes estavam sobrepostas umas às outras.](https://caelum-online-public.s3.amazonaws.com/2984-illustrator/aula+1/Img2.gif)

Note como o desenho vetorial acima é a composição de várias partes juntas que podem ser tratadas individualmente.

## Imagem bitmap

Já as imagens _bitmap_ são aquelas mais comuns, que estamos acostumados a interagir no dia a dia, como as fotografias de câmeras de celular. Ao contrário dos vetores, que são feitos por operações matemáticas que desenham caminhos, os _bitmaps_ são compostos de pequenas unidades fixas, chamadas de _pixels_.

![Text alt: Imagem ilustrativa de uma letra A feita de pequenos quadrados preenchidos de rosa, que pertencem a uma malha com outros quadrados.](https://caelum-online-public.s3.amazonaws.com/2984-illustrator/aula+1/Img3.png)

Na representação _bitmap_, a mesma letra A agora ocupa espaços no espaço onde se situam os _pixels_. Por esse motivo, as imagens desse tipo tem uma resolução específica - isto é, uma quantidade de pixels em uma determinada área - e tendem a ocupar muito mais espaço na memória.

![Text alt: Imagem com duas ilustrações simplificadas de um cervo, ambas na cor preta. As duas ilustrações possuem uma aproximação na região da cabeça do animal. Na ilustração da esquerda, a ampliação não prejudica a qualidade. Já na ampliação da direita, pode-se ver com mais detalhes os pequenos quadrados que constituem o desenho do animal.](https://caelum-online-public.s3.amazonaws.com/2984-illustrator/aula+1/Img4.jpg)

Comparativamente, à esquerda temos uma imagem criada em vetor. Nela, não há perda de qualidade quando nos aproximamos, pois os vetores se adaptam às dimensões e podem ser ampliados quase que infinitamente. Já no lado direito, como a imagem é feita de unidades fixas, conseguimos enxergar nitidamente os _pixels_.