---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-2/p5-do-que-se-trata/","tags":["javascript"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# p5, do que se trata

## criado em: 
-  25-03-2023 - 14:28

### Conteúdo Relacionado
- notas: [[ ENTENDENDO A LIBRARY P5\| ENTENDENDO A LIBRARY P5]]
- tags: #javascript 
- Fontes & Links: 

---
# P5 no Vscode

![P5 no Vscode](https://www.alura.com.br/artigos/assets/p-5-no-vscode/p-5-no-vscode.jpg)


Guilherme Lima

09/12/2021


## P5 no VScode: Passo a passo

O p5.js é uma biblioteca de animação desenvolvida usando a [linguagem de programação Javascript](https://www.alura.com.br/artigos/javascript). Ele é projetado para artistas, desenvolvedores e conhecedores de mídia para criar arte interativa, jogos, visualizações de dados e animações.

Como o p5.js é escrito em Javascript, ele funciona muito bem na web e pode aproveitar as tecnologias existentes baseadas na web, como som, vídeo, entrada de webcam, entre outros.

Podemos [criar nossas animações utilizando o editor de código do p5 online](https://editor.p5js.org/), sem a necessidade de configuração do ambiente. Além disso, podemos usar o p5 no [VSCode](https://code.visualstudio.com/). O Visual Studio Code é um editor de código-fonte desenvolvido pela Microsoft para Windows, Linux e macOS.

### Usando o p5.js no VSCode

A forma mais simples para usar o p5 no VSCode, é através [desta extensão](https://marketplace.visualstudio.com/items?itemName=samplavigne.p5-vscode):

![Imagem da página principal da extensão p5.vscode.](https://www.alura.com.br/artigos/assets/p-5-no-vscode/imagem1.png)

Clicando no ícone verde para instalar, uma caixa de texto será exibida informando que o marketplace deseja abrir este aplicativo. Podemos escolher a opção `Abrir Visual Studio Code`.

![Imagem com a inscrição “Abrir Visual Studio Code”.](https://www.alura.com.br/artigos/assets/p-5-no-vscode/imagem2.png)

O VSCode será aberto nesta página e podemos selecionar a opção `instalar`, como ilustra a imagem abaixo:

![Imagem com a opção instalar para a extensão p5.vscode.](https://www.alura.com.br/artigos/assets/p-5-no-vscode/imagem3.png)

Após a instalação, para criar um novo projeto p5, vamos:

-   Abrir a Paleta de comandos (com command-shift-p no Mac ou ctrl-shift-p no Windows) e, a seguir, comece a digitar p5.js
-   Vamos escolher a opção Criar um projeto com p5.js

![Tela do p5.js](https://www.alura.com.br/artigos/assets/p-5-no-vscode/imagem4.png)

Crie uma nova pasta com o nome que desejar e selecione a opção abrir.

### Estrutura do Projeto

Ao carregar o projeto, observe que toda estrutura do p5.js estará configurada em seu VSCode.

![Tela do p5.js.](https://www.alura.com.br/artigos/assets/p-5-no-vscode/imagem5.png)

O arquivo `index.html` já faz o import do arquivo `sketch.js` (linha 16 do arquivo index.html), assim como as bibliotecas necessárias para o p5.js.

### Live Preview

Para editar o código e visualizar as alterações assim como acontece na versão do editor online do p5, vamos [instalar uma extensão chamada live-server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer). Com ela, todas as alterações no código serão exibidas em tempo real.

Para ativar o Live Server, clique com o botão direito do mouse sobre o arquivo `index.html` e selecione a opção `Abrir com Live Server`, como ilustra a imagem abaixo.

![Tela do p5.js.](https://www.alura.com.br/artigos/assets/p-5-no-vscode/imagem6.png)

### 1, 2, 3 Testando...

Vamos criar uma elipse que segue o ponteiro do mouse e visualizar seu movimento em tempo real com Live Server com o seguinte código no arquivo `sketch.js`:

```
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  ellipse(mouseX,mouseY,50);
}
```

![Tela do p5.js.](https://www.alura.com.br/artigos/assets/p-5-no-vscode/imagem7.gif)

## Conclusão

A principal vantagem de usar o p5.js com VSCode, é que não dependemos da internet para criar ou editar nossos projetos. Quer aprender mais sobre Javascript? Então veja a:

-   [Formação Javascript - A linguagem mais querida](https://www.alura.com.br/cursos-online-front-end/javascript) :)
