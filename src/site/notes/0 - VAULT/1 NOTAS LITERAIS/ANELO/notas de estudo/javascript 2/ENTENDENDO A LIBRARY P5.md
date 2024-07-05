---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-2/entendendo-a-library-p5/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# ENTENDENDO A LIBRARY P5

## criado em: 
-  25-03-2023 - 14:37

### Conteúdo Relacionado
- notas: 
- tags: 
- Fontes & Links: 

---

## P5.js

Ao longo do curso você já deve ter se perguntado “_como a bolinha_ se movimenta na tela?”, ou mesmo “O que é essa tal de function draw() e por qual motivo preciso chamar as funções que construí na function draw()”, não é?!

Para solucionar essas dúvidas, devemos entender um pouquinho sobre a nossa ferramenta. A biblioteca p5.js. Vamos lá?

O p5.js é uma biblioteca JavaScript criada para tornar o desenvolvimento algo acessível e inclusivo para artistas, designers, educadores e iniciantes, ou seja, para qualquer pessoa! Por conta dessa característica, a biblioteca vem com inúmeras funções **”pré-fabricadas”** (algo pré-pronto apenas para você usar), que **facilita** o processo de escrita do código. Sendo assim, a função ****draw()****, ****setup()****, ****preload()**** são alguns exemplos dessas soluções que já estão incluídas na biblioteca para **facilitar a vida do desenvolvedor**.

Ok, mas você deve continuar se perguntando: **_“e os desenhos?”_**

A função própria da biblioteca p5.js responsável por mostrar os desenhos na tela de pré-visualização e atribuir comportamentos ao seu código é a **function draw()**. Além disso, o p5.js utiliza um ****sistema de coordenadas**** que atribui um valor em cada ponto da tela para que possamos identificar o local exato onde os desenhos aparecem.

Mas vamos entender como essa função funciona?

## function draw()

A **function draw()** é a função que faz a "mágica acontecer". Essa função “pré-pronta” do p5.js executa continuamente o seu código, linha por linha. Um aspecto interessante da função é que ela funciona como se possuísse um **loop** (um laço de repetição) , o que faz com que o código escrito em seu escopo seja executado continuamente e por isso que consegue **desenhar** os elementos no ambiente de visualização e fazê-los se movimentar.

Vamos conferir o código da função draw():

```scss
function draw() {
  background(0); //1 - Desenha o background 
  mostraBolinha(); // 2 - Desenha a bolinha
  movimentaBolinha(); // 3 - Movimenta a Bolinha
  verificaColisaoBorda(); // 4 - Verifica Colisão da bolinha

 // 5- Volta para o início da função draw()
}
```

É importante ter em mente que essa leitura é feita de forma muito rápida e por isso não _"sentimos_ essa mudança

Vamos entender um pouco mais?

Logo abaixo você encontra algumas das características principais da function draw() e também formas de fazer um melhor uso dela, vamos conferir:

-   Nós não precisamos construir e declarar a draw() porque ela já está contida na biblioteca do p5.js de forma padrão. :)
-   A draw () é chamada automaticamente após a setup() e nunca deve ser chamada explicitamente;
-   A draw () executa continuamente as linhas de código contidas em seu bloco até que o programa seja interrompido ou noLoop () seja chamada;
-   Dentro da draw() as ações são controladas com noLoop(), redraw() e loop(). Depois que noLoop() interrompe a execução do código em draw(), a redraw() faz com que o código dentro de draw() seja executado uma vez e loop() fará com que o código dentro de draw() retome a execução continuamente;
-   Podemos inserir diretamente o código na draw() ou chamar as funções que apresentam o comportamento desejado (por questões de boas práticas, o instrutor trabalha com funções no curso);
-   Só pode haver uma função draw() para cada sketch, e draw() deve existir se você quiser que o código seja executado continuamente ou para processar eventos como mousePressed();
-   Às vezes, você pode ter uma chamada vazia para draw() em seu programa, (...)”.

## Sistema de coordenadas

Além de todas essas informações, um elemento super importante para compreender o posicionamento dos objetos em tela é o **sistema de coordenadas do p5.js.** Para compreender melhor como funciona, vou deixar um link para o artigo sobre o tema:

-   [**P5.JS: Plano cartesiano**](https://www.alura.com.br/artigos/p5-plano-cartesiano).

Vou deixar também alguns links que redirecionam para a sessão de referência do p5.js:

-   [Reference do p5.js que explica detalhadamente o que é a function draw()](https://p5js.org/reference/#/p5/draw);
-   [Home do p5 com informações sobre a biblioteca](https://p5js.org/).