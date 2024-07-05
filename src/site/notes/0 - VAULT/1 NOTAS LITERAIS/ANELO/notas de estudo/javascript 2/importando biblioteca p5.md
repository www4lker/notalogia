---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-2/importando-biblioteca-p5/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# importando biblioteca p5

## criado em: 
-  26-03-2023 - 15:57

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 2/LP 03 Criando minha raquete\|LP 03 Criando minha raquete]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 2/implementando o codigo com ajuda do chatgpt\|implementando o codigo com ajuda do chatgpt]]
- tags: 
- Fontes & Links: https://cursos.alura.com.br/course/pong-javascript/task/56101
- solução no github https://github.com/bmoren/p5.collide2D


---

Implementamos a colisão da bolinha com a raquete, e obtivemos um comportamento esperado, a mudança de direção da bolinha sempre que isto acontece. Será que outras pessoas já não passaram por este mesmo problema utilizando o p5 e o JavaScript? Será que elas não compartilharam as soluções encontradas para que outras pessoas pudessem usá-las também? A resposta é sim!

Na documentação do p5, há em _Libraries_ algumas bibliotecas contendo soluções ou implementações que podemos adicionar em nosso projeto, feitas por outras pessoas. Escolheremos, por exemplo, "p5.collide2D", que ao ser clicado abrirá uma página do GitHub, plataforma que serve para hospedar código, seja de projetos pessoais ou profissionais.

Neste caso, a página exibe o funcionamento das funções contidas nesta biblioteca. Em nosso projeto, na função `mostraRaquete()` temos o `rect()`, e em `mostraBolinha()` temos `circle()`. Similarmente, na biblioteca existe a função `collideRectCircle()`, exatamente o que precisaríamos para o nosso projeto.

Na explicação sobre como ela funciona existe um trecho de código. Será que basta adicioná-la em nosso projeto para que funcione conforme gostaríamos?

Na verdade, uma biblioteca é composta por uma série de códigos, portanto, inicialmente iremos baixá-los, clicando no botão "Clone or download > Download ZIP", no GitHub. O arquivo que iremos utilizar é o `p5.collide2d.js`; no p5, do lado esquerdo do painel que contém nosso código, existe um `>` que, ao ser clicado, exibe todas as pastas e arquivos que compõem o projeto: `index.html`, `style.css` e `sketch.js`.

Clicaremos no símbolo `v` ao lado de "project-folder", e em "Add file" para adicionar o arquivo recém baixado. Segundo a documentação, a função `collideRectCircle()` cria uma variável `hit` para verificar se há colisão ou não, com `var hit = false`. Em nosso projeto, o `var` corresponde a `let`. Vamos criar uma variável similar:

```bash
let colidiu = false;
```

E então, todo o código referente à colisão é inserida na função `draw()`, que em nosso código é bem específica e contém uma função para cada ação tomada. Vamos acrescentar a função `colisaoMinhaRaqueteBiblioteca()` e comentar a linha que vem acima, com `verificaColisaoRaquete()`, uma vez que queremos utilizar a solução encontrada por outra pessoa, isto é, `colisaoMinhaRaqueteBiblioteca()`, que criaremos no fim do nosso código:

```scss
function colisaoMinhaRaqueteBiblioteca() {
    collideRectCircle(200, 200, 100, 150, mouseX, mouseY, 100);
}
```

O que significam estes parâmetros?

Os quatro parâmetros iniciais se referem ao nosso retângulo, que é a raquete, os quais podem ser substituídos por `xRaquete`, `yRaquete`, `raqueteComprimento` e `raqueteAltura`, respectivamente. Os demais parâmetros têm a ver com o círculo, e os trocaremos por `xBolinha`, `yBolinha` e `raio`.

Para identificarmos se de fato há colisão, ou não, atribuiremos o resultado desta função à variável `colidiu`, e implementaremos uma condição para quando esta variável for `true`, a direção do movimento da bolinha se inverta.

```csharp
function colisaoMinhaRaqueteBiblioteca() {
    colidiu = collideRectCircle(xRaquete, yRaquete, raqueteComprimento, raqueteAltura, xBolinha, yBolinha, raio);
    if (colidiu) {
        velocidadeXBolinha *= -1;
    }
}
```

Ao testarmos, obteremos um erro, e de acordo com o console, `collideRectCircle` não está definido. Acontece que não referenciamos o novo arquivo em nosso código! Faremos isto em `index.html`, entre as tags de abertura e fechamento de `<body>`:

```xml
<body>
    <script src="sketch.js"></script>
    <script src="p5.collide2d.js"></script>
</body>
```

Desta vez, ao testarmos, teremos o resultado que gostaríamos. Então, quando precisamos de uma solução, poderemos nos perguntar se ela não existe, se alguém já não passou por isso. Muito provavelmente a resposta será sim, e podemos pesquisar por muitas alternativas na internet.

Estamos utilizando a solução de outra pessoa, e quando pressionamos o botão de play, o console exibe `### p5.collide ###`. Isto não foi escrito por nós, sendo proveniente do código que baixamos, em `console.log("### p5.collide ###")`. Para que nada seja exibido no console, basta deletarmos toda esta linha. Isto nos mostra que, mesmo quando pegamos uma possível solução alheia, é possível alterá-la.
