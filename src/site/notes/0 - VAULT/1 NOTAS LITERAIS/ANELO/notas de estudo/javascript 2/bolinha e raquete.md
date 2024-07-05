---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-2/bolinha-e-raquete/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# bolinha e raquete

## criado em: 
-  25-03-2023 - 11:11

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 2/bolinha e raquete - JAVASCRIPT\|bolinha e raquete - JAVASCRIPT]]
- tags: 
- Fontes & Links: https://cursos.alura.com.br/course/pong-javascript/task/56083

---

Vamos começar a criar nosso jogo de Pong com o Scratch, para fortalecermos nossa lógica de programação! Relembrando que a bolinha atuará em posições aleatórias, e temos que acertá-la, colidindo com ela por meio das raquetes. Acessaremos o [site do Scratch](http://scratch.mit.edu) — caso não esteja logado em sua conta, na etapa anterior há uma explicação de preparação do ambiente, com um passo a passo do que é necessário para criá-la.

Clicaremos em "Criar", no menu superior, e para configurarmos a língua utilizada, poderemos clicar no ícone de globo localizado no menu do topo, e selecionar "Português Brasileiro". No Pong, temos um fundo preto, e a bolinha e as raquetes na cor branca. Vamos deletar o gatinho clicando no "x" do painel inferior direito, ou clicando com o lado direito do mouse e selecionando "Apagar".

Feito isso, clicaremos no painel "Palco", no canto inferior direito, na aba "Cenários" no painel principal, e trocaremos a cor de preenchimento para preto, que será a mesma cor do contorno. Selecionaremos a ferramenta de quadrado e criaremos um que ocupe todo o espaço disponível.

Para criarmos a bolinha, clicaremos no ícone com a face de um gato no canto inferior direito da tela para selecionarmos um **ator**, que pode ser algum próprio da galeria do Scratch. No caso, queremos personalizá-lo, portanto clicaremos na opção "Pintar", o que abrirá um editor bem similar ao que utilizamos para pintar o cenário. Desta vez, tanto a cor quanto o contorno serão em branco. Com a ferramenta de círculo, desenharemos uma bolinha. Alinhe o centro do círculo desenhado à tela do painel, pois a discrepância entre esses pontos pode gerar bugs no jogo como a bolinha pular de posição ou mesmo rebater várias vezes na raquete.

Sobre o painel localizado à direita, para testarmos, clicaremos no ícone de bandeira verde, porém nada acontece. Geralmente, quando jogamos algo, os personagens não ficam posicionados aleatoriamente, tampouco na última posição em que estiveram. Isto é, eles possuem uma posição inicial, e neste jogo não será diferente.

Selecionaremos uma posição inicial para a nossa bolinha clicando em "Eventos", e em "quando [ícone de bandeira verde] for clicado", que arrastaremos ao painel principal. Depois, clicaremos em "Movimento" e em "vá para x: 182 y: -135", que também arrastaremos ao painel principal, encaixando na primeira "peça". Clicaremos nestes valores para os alterarmos para `0` e `0`.

Assim, ao clicarmos no ícone de bandeira verde, teremos que a bolinha começa no centro do jogo. Agora, precisaremos movimentá-la! Clicaremos e arrastaremos "mova 10 passos" para o painel principal, encaixando-a na peça anterior. Clicando no ícone de bandeira verde, a bolinha se locomove um pouco para a direita, mas se clicarmos novamente, nada acontece.

Acontece que, quando nosso jogo se inicia, ele faz o que está definido na segunda peça e logo muda para a terceira, entretanto, isto ocorre apenas uma vez, quando na verdade queremos que a bolinha siga se movimentando. Para isso, clicaremos e arrastaremos outro evento "quando [ícone de bandeira verde] for clicado" para cima de "mova 10 passos", formando um segundo conjunto. E então clicaremos em "Controle" e em "sempre", que arrastaremos ao segundo conjunto, englobando o "mova 10 passos".

Assim, o movimento acontecerá sempre, ou seja, os 10 passos serão adicionados continuamente. Ao testarmos, a bolinha começará no centro e terminará no canto direito da tela, visível pela metade. Para um movimento de vai e volta, existe um código em "Movimento" que verifica essa **colisão** com as bordas da nossa tela, denominada "se tocar na borda, volte", o qual posicionaremos dentro de "sempre", abaixo de "mova 10 passos".

Aumentaremos a velocidade da bolinha aumentando o número de passos para `12`. Entretanto, deste modo o movimento se dará apenas horizontalmente, então, poderemos indicar uma direção para ela, acrescentando "aponte para a direção 90" logo abaixo de "vá para x: 0 y: 0". Reparem que, ao clicarmos no valor, é demonstrado um círculo para demonstrar que o movimento se inicia em 90º. Vamos alterá-lo para `45`.

Desta vez, a nossa bolinha se movimenta em vários sentidos, de acordo com essa angulação. E como é que iremos interagir com este jogo? Teremos raquetes, atores que criaremos a seguir!

---

Renomearemos o novo ator para "bolinha", e pintaremos outro ator, denominado "minha raquete", um retângulo de preenchimento e contorno brancos, para simular uma das raquetes. Na aba "Código", uma vez que queremos que ele comece do lado esquerdo da tela, enquanto a bolinha está no centro, definiremos que quando a bandeira verde for pressionada, queremos que a raquete vá para X `-220` e Y `0`.

Isso, porém, ainda não fará com que a raquete se movimente, pois não programamos nosso jogo para fazer isso. Queremos utilizar nosso teclado para que a raquete se mova verticalmente, e para fazermos isto de forma organizada, arrastaremos outro "quando [ícone de bandeira verde] for clicado" e encaixaremos abaixo dele "se [hexágono] então", existente em "Controle".

De "Sensores", clicaremos e arrastaremos "tecla espaço pressionada?" no espaço onde havia o símbolo de hexágono, e modificaremos "espaço" para "seta para cima". Assim, se a seta para cima for pressionada, a bolinha irá para cima. Sempre que tivermos dúvidas em relação a X e Y, no canto inferior esquerdo do programa podemos clicar em "Selecionar Cenário" e em "Xy-grid", que utilizaremos como gabarito. O X corresponde ao eixo horizontal, enquanto o Y corresponde ao eixo vertical.

Então, assim que a seta para cima for pressionada, queremos que a raquete vá para cima também. Ou seja, adicionaremos um valor para Y, e para tal clicaremos e arrastaremos "adicione 10 a y" dentro de "se [hexágono] então". Ao testarmos, porém, a raquete não se movimenta, já que o código é executado assim que o jogo é ligado, momento em que ainda não estamos com a tecla da seta para cima pressionada, e esta verificação é feita apenas uma vez.

Para resolvermos isso, envolveremos todo o segundo bloco abaixo de "quando [ícone de bandeira verde] for clicado" em outro, "sempre". No entanto, isso fará com que consigamos mover a raquete apenas para cima, portanto duplicaremos o bloco envolvido por "sempre" — clicando com o lado direito do mouse e em "Duplicar" — e substituiremos "seta para cima" por "seta para baixo", e o valor `10` por `-10`.

A bolinha ainda não está colidindo com a raquete, ultrapassando-a e tocando a lateral da tela. Podemos, inclusive, visualizar isto melhor diminuindo a velocidade da bolinha, que queremos que mude de direção assim que tocar na raquete. Podemos criar um bloco para verificar se estamos tocando na borda.

> Para deixar o código organizado, é possível clicar com o lado direito do mouse no painel principal e em "Limpar Blocos".

Continuando, criaremos mais um bloco de código para quando o jogo for iniciado, para verificarmos se a bolinha está tocando a raquete. Teremos, então, "quando [ícone de bandeira verde] for clicado", e logo abaixo, "se [hexágono] então", cujo hexágono será preenchido por "tocando em minha raquete?".

Para invertermos a rota da bolinha, reconhecendo a colisão com a raquete e alterar a direção, inverteremos o valor multiplicando-o por `-1`. De "Movimento", clicaremos e arrastaremos "aponte para a direção 90" para dentro de "se 'tocando em minha raquete?' então". Substituiremos o valor `90` pela opção "direção".

De "Operadores" selecionaremos o bloco verde com "[] * []", e para o primeiro espaço arrastaremos o "direção" que tínhamos movimentado anteriormente, o qual multiplicaremos por `-1`, valor que digitaremos no segundo espaço do bloco. Daí, sim, encaixaremos o bloco final para onde "direção" estava antes, de modo a ficar "aponte para a direção 'direção * -1'".

Porém, mais uma vez, o código só foi executado uma vez, quando o jogo se iniciou. Envolveremos todo o bloco do "se..." em outro, "sempre". Agora, sim, temos o comportamento esperado!