---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/posicionando-elementos/","tags":["css","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# posicionando elementos

## criado em: 
-  30-03-2023 - 15:10

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/classes CSS\|classes CSS]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/estilos de texto e fontes\|estilos de texto e fontes]]
- tags: #css #ANELO 
- Fontes & Links:  https://cursos.alura.com.br/course/html-css-classes-posicionamento-flexbox/task/118640
- https://css-tricks.com/snippets/css/a-guide-to-flexbox/
- https://www.alura.com.br/artigos/guia-de-unidades-no-css
- https://developer.mozilla.org/pt-BR/docs/Learn/HTML/Introduction_to_HTML/Getting_started

---

## Nessa aula, você aprendeu:

-   Padrões de projetos CSS com height e box-sizing;
-   Unidade Viewport;
-   Hierarquia entre elementos pai e filho;
-   Formas e parâmetros de posicionamento;
-   Flexbox.

---
**Guilherme:** No nosso código CSS, aplicamos o `margin: 0` e o `padding: 0`. Existem outros padrões para adicionarmos e desenvolvermos nosso projeto de uma forma legal, Rafa?

É bom sabermos esses padrões desde o começo. Por exemplo, existe alguma forma de garantirmos que nossa página ocupará 100% do tamanho da tela? Porque isso é bem importante.

Vamos voltar ao [Figma do projeto](https://cursos.alura.com.br/course/html-css-classes-posicionamento-flexbox/task/118640) para eu mostrar uma coisa para você. Nesse Figma, toda nossa aplicação fica em uma tela. Não temos scroll, está tudo em uma tela só.

![Projeto do Figma. Temos dois blocos de conteúdo, lado a lado, centralizados sobre fundo preto. O bloco esquerdo possui um texto que se divide em duas partes: título e subtítulo. O título apresenta um texto em negrito dividido em duas cores: "Eleve seu negócio digital a outro nível" em branco, seguido de "com um Front-end de qualidade!" em ciano. O subtítulo está na cor branca, e exibe o texto de apresentação da Joana Santos. Abaixo do subtítulo temos dois botões na cor ciano, lado a lado: no botão esquerdo temos o texto "Instagram" e no direito o texto "Github". Já o bloco direito se constitui de uma fotografia em preto e branco representando Joana Santos, uma mulher desenvolvedora, sentada em frente a um notebook aberto. A fotografia também conta com um desenho em ciano de uma linha circulando Joana e seu notebook três vezes e terminando em uma estrela.](https://cdn1.gnarususercontent.com.br/1/935581/49e15161-1a46-4440-9cb5-6a66625f046d.png)

Tem alguma propriedade do CSS que nos permite informar que ocupamos todo tamanho dessa tela e como vermos que não está ocupando?

**Rafaella:** Tem sim, vamos descobrir como. Abrindo o "Inspecionar" do nosso projeto de portfólio, e aqui eu vou diminuir o zoom, porque está em 155%, ao passarmos o mouse sobre o código `body`, na coluna da direita.

Lembrando que o `body` contém todo nosso conteúdo e, ao observamos a seleção, notamos que ele não ocupa toda página. Na verdade ele termina praticamente na metade da página.

O que conseguimos fazer é usar um padrão inicial no qual sempre conseguimos usar 100% da altura da tela. Para isso, voltaremos ao arquivo `style.css` no VS Code e, dentro das chaves do `body`, adicionaremos o valor de `height` (**altura**).

> **Lembrete:** É comum confundir a posição do "T" em **_height_**, para isso, fica o lembrete que o T é **no final**.

E definiremos uma altura para o nosso _body_

**Guilherme:** Lembrem que o "T" de **_height_** fica no final, pessoal, para não se confundirem!

**Rafaella:** E nós vamos definir uma altura para o nosso `body`, ou seja, todo corpo da página. E o valor que vamos atribuir é de `100vh`.

```css
body {
    height: 100vh;
    background-color: #000000;
    color: #F6F6F6;
}
```

E o que é esse **vh**?

**Guilherme:** Nós demos um _spoiler_ sobre isso quando fizemos o `index.html`, certo, Rafa?

**Rafaella:** Sim! Vou até voltar para o arquivo do `index.html`, onde criamos uma `meta` informação na linha 6 chamada `viewport`. Essa é a tela onde estamos acessando nosso projeto.

Então no CSS nós definimos a altura dessa tela equivalente a **100% do _viewport_**, ou seja, da tela do nosso projeto no navegador.

**Guilherme:** E isso já mudou no navegador?

**Rafaella:** Vamos ver. Vamos recarregar a tela do nosso projeto no navegador e com o Inspecionar ainda aberto, vamos passar o mouse sobre o código do elemento `body`. Feito isso, toda tela fica azul, que é a cor desse elemento, então estamos ocupando 100% da tela!

**Guilherme:** Bem legal!

**Rafaella:** E esse é um padrão que podemos utilizar sempre, no começo dos nossos códigos. Além disso, tem outro padrão interessante de adicionarmos.

**Guilherme:** Nós informamos que a altura máxima será equivalente a toda a tela do dispositivo, agora precisamos garantir que nada fique de fora dessa tela.

**Rafaella:** O que o Guilherme está tentando dizer é que às vezes temos uma imagem cuja margem à esquerda fica tão grande que ela sai do `body`. Então precisamos garantir que os elementos "filhos", que estão dentro das tags maiores, como a tag "pai" `<body>`, ou seja, uma tag que está abaixo de outra não saia da tela.

Para isso, temos uma propriedade, que veremos agora na documentação. Para acessar a documentação, vamos pesquisar pelo nome da propriedade, que é "**_box sizing_**". E para ela eu gosto muito de usar como referência o Mozilla, porque tem um exemplo mais visual.

Então acessaremos a página [box-sizing do Mozilla](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing) e traduziremos o texto para o Português. No começo da página já encontramos **três exemplos** de _box sizing_ no centro esquerdo da página, e o efeito deles no conteúdo do lado direito.

Inicialmente temos o valor do `content-box`, e ele declara o `width` (largura) de 100%. No segundo exemplo também tem um `content-box` ao qual é adicionado uma borda e um _padding_, que já aprendemos o que são. Por fim, tem um `box-sizing` com o valor `border-box`.

```css
box-sizing: content-box;
width: 100%;

box-sizing: content-box;
width: 100%;
border: solid #5B6DCD 10px;
padding: 5px;

box-sizing: border-box;
width: 100%;
border: solid #5B6DCD 10px;
padding: 5px;
```

A cada exemplo que clicamos, observamos como o conteúdo vai se alterando no lado direito. Então com o primeiro momento o elemento "filho" tem 100% da largura, então ele fica completamente dentro do elemento "pai". Pensando no nosso projeto, se deixássemos a imagem com `width: 100%`, ela ocuparia toda a largura do `body`.

No segundo exemplo temos uma borda e um padding. Se quiséssemos aplicar isso à imagem do nosso projeto, ou seja, adicionar uma borda colorida e deixar um espaçamento entre essa borda e o conteúdo, a imagem iria sair do nosso `body`, como aconteceu conteúdo do exemplo.

Com o valor `content-box` no `box-sizing` pode acontecer isso, e não é o que queremos. O que queremos é o valor `border-box`, porque com ele conseguimos criar, por exemplo, uma borda e um padding, ou o que quisermos, e o conteúdo será encolhido para sempre ser mantido dentro do elemento "pai".

Pode não parecer legal encolher esse conteúdo, mas é isso que faz com que tenhamos controle de como todos os elementos estão funcionando, já que é muito frustrante estar fazendo uma alteração no elemento "filho" e ele sair do "pai. Outro exemplo no nosso projeto: temos como "filho" o destaque do título, imagina se ele sai do elemento "pai".

Então precisamos desse controle do "filho" dentro do "pai", e para isso conseguimos usar como padrão o `box-sizing: border-box`. Sendo assim, vamos copiar esse código e adicioná-lo ao `body` do CSS.

```css
body {
    height: 100vh;
    box-sizing: border-box;
    background-color: #000000;
    color: #F6F6F6;
}
```

Vamos salvar e atualizar a página do projeto no navegador.

**Guilherme:** Visualmente não notamos nenhuma diferença, mas agora nada vai sair da nossa página.

**Rafaella:** E essa é uma ótima prática para vocês aplicarem em todos os projetos que criarem, caso a intenção seja evitar que a imagem saia do body, ou seja, evitar que o elemento "filho" saia do elemento "pai".

---

### O que é Viewport?

Em computação gráfica, a viewport é a porção de área visível de um plano e é utilizada como unidade de medida no CSS para criar páginas Web 100% responsivas. Em outras palavras, a viewport varia de dispositivo para dispositivo, por exemplo em computadores, tablets e celulares, cada tela possui dimensões diferentes e enquanto uma página não responsiva apresentaria os elementos desproporcionais, uma página responsiva utilizando viewport teria seus elementos adequados a cada proporção.

Se você demonstrou interesse pelo assunto e quer se aprofundar mais, recomendamos que leia o artigo [Guia de Unidades no CSS](https://www.alura.com.br/artigos/guia-de-unidades-no-css). Através dele você vai conhecer não só a Viewport, mas também outras unidades e conceitos muito utilizados no dia a dia de Dev Front-end.

---

**Guilherme:** Rafa, por favor, eu preciso da sua ajuda, porque ele não está bonito! As cores estão legais e a imagem também, mas como mudamos o posicionamento desses elementos?

Não precisa ficar lindo, mas seria legal ter os textos de um lado e a imagem do outro.

**Rafaella:** Existem várias formas de posicionarmos esses elementos na página. Podemos usar posições fixas e definir quanto pixels queremos de margem, por exemplo, 300px na margem superior do título, empurrando todo conteúdo para baixo.

Entretanto definir um número fixo não é uma boa prática, porque podemos usar várias telas para abrir nosso projeto, e assim ele não ficará da mesma forma como imaginamos.

**Guilherme:** Vou até usar um exemplo. Você define uma margem de 300px e eu abro no celular, que não tem todo esse espaço, então vai ficar muito estranho. Ou então eu abro em um super monitor gamer de 34 polegadas e o espaço ficará minúsculo.

**Rafaella:** Vai ficar horroroso. Então podemos utilizar esse posicionamento específico em alguns pontos específicos. Porém quando temos dois elementos grandes para posicionar, como observamos no Figma do nosso projeto, e queremos posicionar em relação um ao outro, conseguimos usar tecnologias que já foram criadas para facilitar a resolver esse problema.

No caso, temos vários elementos para posicionar na nossa página, mas eu me referi a dois elementos porque temos uma seção principal, com o texto e os botões do lado esquerdo, e a imagem, do lado direito. Portanto são dois grandes elementos que queremos centralizar na página, mas deixá-los lado a lado.

![Projeto do Figma visto no vídeo passado. Temos dois blocos de conteúdo, lado a lado, centralizados sobre fundo preto. O bloco esquerdo possui um texto que se divide em duas partes: título e subtítulo. Abaixo do subtítulo temos dois botões na cor ciano, lado a lado: no botão esquerdo temos o texto "Instagram" e no direito o texto "Github". Já o bloco direito se constitui de uma fotografia em preto e branco representando Joana Santos.](https://cdn1.gnarususercontent.com.br/1/935581/49e15161-1a46-4440-9cb5-6a66625f046d.png)

Uma das tecnologias que usaremos agora no nosso projeto é o **_Flexbox_**. E como tudo que já fizemos, buscaremos a documentação dele.

**Guilherme:** Podemos reparar que essa é uma prática constante. Sempre que vamos aprender algo novo, conferimos a documentação. Estamos tentando guiar vocês à uma documentação mais fácil e que tenha uma tradução em português.

Podemos até abrir a [documentação do Mozilla sobre _Flexbox_](https://developer.mozilla.org/pt-BR/docs/Learn/CSS/CSS_layout/Flexbox) e ao traduzir para o português somos informados que se trata de "uma nova tecnologia" e que a ideia deles é "centralizar blocos de conteúdo verticalmente dentro do seu pai". Inclusive já aprendemos que o "pai" seria o elemento que contém outros elementos dentro.

Eu recomendo que vocês leiam essa documentação com calma, mas ela é bastante técnica. Porém existe um "atalho" que vamos passa, certo, Rafa?

**Rafaella:** Exato, é um **guia do _Flexbox_** com imagens, sendo muito mais tranquilo de conhecerem: o chamado [**_A Complete Guide to Flexbox_**](https://css-tricks.com/snippets/css/a-guide-to-flexbox/). Também traduziremos essa página para o português e, ao rolar por essa página, nos deparamos com várias imagens.

Agora nós tentaremos entender como iniciar a utilização do Flexbox. O **primeiro ponto** é que existe uma propriedade que precisamos definir para o elemento "pai", e ela indica quando começaremos a usar o _flexbox_ para posicionar nossos elementos. O nome dessa propriedade, como mostra o primeiro exemplo, é o [**display: flex**](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-display).

```
.container {
  display: flex; /* or inline-flex */
}
```

Nesse caso, podemos chamar a tag "pai" de container, mas sempre precisamos adicionar essa propriedade. Então vou copiar e voltar para o nosso código `index.html` no VS Code.

Comparando o Figma com o `index.html`, conseguimos analisar que o elemento "pai" dos elementos que queremos posicionar, ou seja, o container que fica o envolve, é o `<main>`. Tudo está dentro do `<main>`, portanto é nele que vamos codar a propriedade que informa onde usaremos o Flexbox, como informou o _Complete Guide_.

E para conseguirmos estilizar nosso `main`, criaremos uma classe para ele. Como nomeamos essa classe?

**Guilherme:** Como estamos mostrando o texto e a imagem, pode ser "apresentação".

**Rafaella:** Então será `"apresentacao"`, por isso nossa linha 12 fica:

```
<main class="apresentacao">
```

**Guilherme:** Rafa, em nenhum momento das classes que estamos criando você escreve com acentuação. Nós não usamos acento, certo?

**Rafaella:** Não, porque é uma boa prática e é mais fácil de não ter erros. Como comentamos, existe a questão de a máquina interpretar o acento como uma série de códigos, o que não é legal. Por isso escrevemos sem acento.

E agora, no `style.css`, após o fechamento de chaves do `.titulo-destaque {}` e pressionamos "Enter" duas vezes e codamos, a partir da linha 17:

```
.apresentacao {
    display: flex;
}
```

Colamos dentro dessa classe a propriedade que vimos na documentação. Agora, voltando para o navegador, observamos que nosso conteúdo de texto está à esquerda enquanto a imagem está à direita da página.

**Guilherme:** Ele mudou! Diz se eu entendi, Rafa. Ele está dizendo que o `main`, que é o "pai" será `display: flex`, então ele coloca todos os elementos do `main` na mesma linha.

**Rafaella:** Na verdade, o Flexbox faz isso por padrão, ou seja, deixa os elementos no sentido de linha, que em inglês é **_Row_**, mas isso **é configurável**. Não necessariamente queremos que nossos elementos fiquem em uma linha, e eles podem ficar na posição de coluna; Essa é outra propriedade que podemos inserir no código: a **`flex-direction`**, como mostra o _Complete Guide_.

```
.container {
  flex-direction: row | row-reverse | column | column-reverse;
}
```

Contudo, o padrão do nosso projeto é horizontal, ou seja, do lado esquerdo fica o texto e do direito a imagem. Então não precisamos alterar esse padrão, ou seja, não precisamos alterar a propriedade [**_flex-direction_**](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-flex-direction) e determinar se será coluna ou linha. Inclusive podemos escrever como `flex-direction: row`, mas ele já está fazemos o que gostaríamos.

**Guilherme:** Então por _default_ (padrão) ele já tem algumas configurações.

**Rafaella:** Sim, por isso já ficou automaticamente em forma de linha.

**Guilherme:** Vamos voltar no nosso projeto no navegador, Rafa, porque tem algo que achei interessante. Tiramos a margem e, quando deixamos no `display: flex` ele deixou na mesma linha.

Conseguimos centralizar esse conteúdo? Porque é um segundo passo grande vencido.

**Rafaella:** Descendo na documentação do _Complete Guide_, encontramos a propriedade [**Itens de alinhamento**](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-align-content). Nela temos 5 imagens que representam a disposição dos itens na página.

[![Representação gráfica dos itens de alinhamento, presente na documentação. Na imagem há cinco figuras de retângulos roxos com retângulos laranjas no seu interior. Os retângulos roxos estão dispostos em três linhas. Na primeira linha há dois retângulos de medidas iguais lado a lado. O do lado esquerdo está sob o título "flex-start" e dentro dele os retângulos laranjas estão alinhados horizontalmente na parte superior. Já o retângulo roxo da direita está sob o título "flex-end", e os retângulos laranjas estão alinhados horizontalmente na parte inferior. Na segunda linha de figuras, também há dois retângulos roxos, lado a lado, e ambos possuem a mesma medida. O da esquerda está sob o título "center" e os retângulos laranjas estão alinhados horizontalmente no centro do retângulo roxo. Já a figura da direita está sobre o título "stretch" e os retângulos laranjas no seu interior possuem as mesmas medidas de altura e largura, sendo que a altura do retângulo roxo e dos retângulos laranjas são iguais. Na terceira linha há apenas um retângulo roxo, cuja largura é o dobro dos retângulos anteriores, portanto ele ocupa toda extensão da linha de figuras. Ele está sob o título "baseline". Dentro dele os retângulos laranjas possuem tamanhos diferentes de altura e largura, mas a disposição deles ocupa toda largura do retângulo roxo. Dentro de cada um dos retângulos laranjas está escrito "text" em seu interior. Uma linha horizontal amarela passa por todos os retângulos laranjas, exatamente abaixo do "text text”, indicando que os textos estão alinhados.](https://css-tricks.com/wp-content/uploads/2018/10/align-items.svg)](https://css-tricks.com/wp-content/uploads/2018/10/align-content.svg)

```
.container {
  align-items: stretch | flex-start | flex-end | center | baseline | first baseline | last baseline | start | end | self-start | self-end + ... safe | unsafe;
}
```

Temos os itens na forma de `flex-start`, que é o valor da propriedade inicial, como está a página do nosso projeto. Além disso, podemos deixar todos os conteúdos no final da página, com `flex-end`, mas o que você falou para fazermos é deixá-lo no centro, então no valor da propriedade vamos codar `align-items: center`, como a documentação está informando para nós.

```
.apresentação {
    display: flex;
    align-items: center;
}
```

Quando salvamos e voltamos para observar nossa página no navegador, vemos que os conteúdos de texto estão centralizados, mas nossos elementos não estão no centro da página.

**Guilherme:** Parece que está no centro da imagem.

**Rafaella:** É justamente isso. Na verdade o `align-items` alinha os itens de acordo com o próprio alinhamento deles. Então temos a imagem, que é o elemento de maior altura, e ela que define qual será o ponto central do alinhamento. Então todos os alinhamentos estão alinhados conforme a imagem.

---

#### Guia completo do Flexbox

Durante a aula foi apresentado o [Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/). Ele é recomendado, pois simplifica e abrange tudo sobre o layout CSS Flexbox, explicando sobre as diferentes propriedades para o elemento pai e os elementos filhos. Ele também inclui histórico, demonstrações, padrões e um gráfico de suporte do navegador.

##### Material Alura

Se você quiser mergulhar de vez nesse assunto, você pode explorar o nosso curso [CSS: Flexbox e layouts responsivos](https://cursos.alura.com.br/course/css-flexbox-layouts-responsivos) e também recomendamos que busque por [CSS: Flexbox](https://cursos.alura.com.br/search?query=flexbox) aqui na escola. Contamos com diversos outros materiais entre cursos, artigos e Alura+ para estruturar e complementar seus estudos.

---
### estilizando o texto

**Guilherme:** Se compararmos a expectativa com a realidade, veremos que o texto da nossa aplicação está posicionado. Entretanto, o tamanho desses elementos...

**Rafaella:** Dessa seção, né.

**Guilherme:** Isso! Dessa seção. A linguagem está ficando mais técnica.

**Rafaella:** Exato.

**Guilherme:** O tamanho da nossa seção de texto está diferente do Figma, onde ela possui um tamanho específico.

**Rafaella:** Exatamente. É possível definir um tamanho para que todos os elementos caibam dentro da seção. Para isso, utilizaremos uma propriedade dentro do arquivo CSS.

Precisamos de uma `class` para definir essa `section` localizada no `index.html`, assim como ocorre com a classe `main`. Portanto vamos adicioná-la entre os sinais de menor e maior da tag `<section>`. Qual será o nome dessa classe, Gui?

**Guilherme:** Estamos no elemento pai que é o `main`, cuja `class` é `apresentacao`. Embaixo criaremos uma nova seção, na qual colocaremos primeiro o nome do pai: `apresentacao`.

> **Dica:** Por padrão, para nomear elementos filhos, as pessoas utilizam o nome do elemento pai junto ao sinal `__` e junto ao nome que será criado para o elemento filho.

Já que se trata do conteúdo — ou seja, o `h1`, o texto e os links — vamos chamá-lo de `conteudo`, pode ser?

**Rafaella:** Vamos. Será `apresentacao__conteudo`.

```javascript
    <main class="apresentacao">
    <section class="apresentacao__conteudo">
        <h1>Eleve seu negócio digital a outro nível <strong class="titulo-destaque">com um Front-end de qualidade!</strong></h1>
        <p>Olá! Sou Joana Santos, desenvolvedora Front-end com especialidade em React, HTML e CSS. Ajudo pequenos negócios e designers a colocarem em prática boas ideias. Vamos conversar?
        </p>
        <a href="https://instagram.com/rafaballerini">Instagram</a>
        <a href="https://github.com/guilhermeonrails">Github</a>
    </section>
    <img src="imagem.png" alt="Foto da Joana Santos programando">
```

Acessaremos o nosso `style.css` e adicionaremos abaixo das chaves de `.apresentacao{}` uma nova seção chamada `.apresentacao__conteudo{}`.

```css
.apresentacao {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.apresentacao__conteudo{

}
```

Definiremos uma largura para essa `section`. De onde retiraremos esse valor?

**Guilherme:** Não vamos tirar da nossa cabeça, e sim da cabeça de quem fez o Figma!

**Rafaella:** Exatamente.

**Guilherme:** Vamos acessar o [Figma do projeto](https://www.figma.com/file/4EKKCbr5rS93RWP7kRjXIz/Portfolio---Curso-1?node-id=0%3A1) para procurar o valor dessa largura.

**Rafaella:** A pessoa que fez o Figma inseriu e agrupou os elementos. Podemos clicar neles e ver as informações sobre cada seção de elementos no canto direito da tela. Nele buscaremos a aba "Design", onde veremos um valor `W`. O que seria esse valor?

**Guilherme:** É _width_, ou seja, a largura.

**Rafaella:** Exatamente, `W` é a largura e `H` é altura, ou _height_.

**Guilherme:** Uma dica que eu dou: o W é mais largo e lembra a largura, enquanto o H é mais alto e lembra a altura. Isso me ajuda.

**Rafaella:** Interessante. Gostei.

Vamos clicar no valor de `W` e copiá-lo — ele corresponde a `615`. Voltaremos ao nosso código e dentro das chaves de `.apresentacao__conteudo{}` vamos adicionar um `width:` e colar o valor copiado.

Este `615` corresponde a qual unidade?

**Guilherme:** Pixel.

**Rafaella:** Exatamente. Portanto adicionaremos `px` e salvaremos o código.

```css
.apresentacao__conteudo{
    width: 615px;
}
```

Voltaremos ao navegador. O que aconteceu?

**Guilherme:** O bloco de texto não está mais tão comprido, existe um limite.

**Rafaella:** Exato. Quando o conteúdo chega no limite dessa `width` que configuramos, ele é quebrado para a linha de baixo.

**Guilherme:** Então eu sugiro um próximo passo, Rafa. Vamos aumentar o tamanho do nosso título? Se verificarmos o Figma, ele é grande.

**Rafaella:** Sim. O título é bem maior.

**Guilherme:** Podemos selecioná-lo isoladamente no Figma?

**Rafaella:** Podemos.

**Guilherme:** Este título tem um tamanho de 36 pixels. Podemos localizar esta informação na seção "Text" na coluna lateral direita do Figma. Vamos colocar esse tamanho no código.

Este conteúdo é novo, nós nunca havíamos alterado o tamanho de uma fonte.

**Rafaella:** Exato. Retornaremos ao nosso código e acessaremos o arquivo `index.html`. Em seu interior buscaremos a tag `<h1>` e entre os sinais de menor e maior adicionaremos uma `class`. Qual será o nome dessa classe?

**Guilherme:** Podemos chamá-la de `apresentacao__conteudo__titulo`.

**Rafaella:** Pode ser.

```javascript
    <main class="apresentacao">
    <section class="apresentacao__conteudo">
        <h1 class="apresentacao__conteudo__titulo">Eleve seu negócio digital a outro nível <strong class="titulo-destaque">com um Front-end de qualidade!</strong></h1>
        <p>Olá! Sou Joana Santos, desenvolvedora Front-end com especialidade em React, HTML e CSS. Ajudo pequenos negócios e designers a colocarem em prática boas ideias. Vamos conversar?
        </p>
        <a href="https://instagram.com/rafaballerini">Instagram</a>
        <a href="https://github.com/guilhermeonrails">Github</a>
    </section>
    <img src="imagem.png" alt="Foto da Joana Santos programando">
```

Salvaremos o código e abriremos o arquivo `style.css`para utilizar esse nome de classe.

**Guilherme:** Boa.

**Rafaella:** No arquivo CSS, abaixo das chaves de `.apresentacao__conteudo{}`, criaremos a `.apresentacao__conteudo__titulo{}`.

```css
.apresentacao {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.apresentacao__conteudo{
    width: 615px;
}

.apresentacao__conteudo__titulo{

}
```

**Guilherme:** Como alteraremos o tamanho da fonte, Rafa?

**Rafaella:** Temos uma propriedade chamada `font-size`, onde `font` corresponde à fonte e `size` ao tamanho. Vamos adicioná-la dentro das chaves de `.apresentacao__conteudo__titulo{}`. em seguida adicionaremos o valor `36px` que coletamos do Figma.

```css
.apresentacao__conteudo__titulo{
    font-size: 36px;
}
```

Salvaremos e retornaremos ao navegador para conferir a mudança no tamanho da fonte do título.

**Guilherme:** Está ficando bem legal.

**Rafaella:** Está. Vamos alterar também o conteúdo do subtítulo, ou seja, do parágrafo. Ele possui um tamanho específico que também podemos extrair do Figma: 24 pixels.

Retornaremos ao arquivo `index.html` e buscaremos a tag `<p>`. Entre os sinais de menor e maior dela criaremos uma `class`. Qual será o nome dela?

**Guilherme:** Pode ser `apresentacao__conteudo__texto`?

**Rafaella:** Pode ser.

```javascript
    <main class="apresentacao">
    <section class="apresentacao__conteudo">
        <h1 class="apresentacao__conteudo__titulo">Eleve seu negócio digital a outro nível <strong class="titulo-destaque">com um Front-end de qualidade!</strong></h1>
        <p class="apresentacao__conteudo__texto">Olá! Sou Joana Santos, desenvolvedora Front-end com especialidade em React, HTML e CSS. Ajudo pequenos negócios e designers a colocarem em prática boas ideias. Vamos conversar?
        </p>
        <a href="https://instagram.com/rafaballerini">Instagram</a>
        <a href="https://github.com/guilhermeonrails">Github</a>
    </section>
    <img src="imagem.png" alt="Foto da Joana Santos programando">
```

Salvaremos o código e acessaremos o arquivo `style .css`. Abaixo das chaves de `.apresentacao__conteudo__titulo{}` adicionaremos um `apresentacao__conteudo__texto{}`. Em seu interior adicionaremos um `font-size: 24px`.

```css
.apresentacao {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.apresentacao__conteudo{
    width: 615px;
}

.apresentacao__conteudo__titulo{
    font-size: 36px;
}

.apresentacao__conteudo__texto{
    font-size: 24px;
}
```

Salvaremos esse código e voltaremos ao navegador, onde veremos os textos com os tamanhos certos.

**Guilherme:** Está ficando cada vez melhor.

---

## importando fontes tipográficas

**Rafaella:** Já temos os tamanhos de fonte do nosso título e do parágrafo. Porém, existe uma grande diferença entre o Figma e a nossa página. Acessaremos o [Figma do projeto](https://www.figma.com/file/4EKKCbr5rS93RWP7kRjXIz/Portfolio---Curso-1?t=6dfeFknOinJA1UCL-0) e veremos que a fonte de ambos os textos é mais arredondada, é diferente.

Se clicarmos no elemento `h1` (o título) pelo Figma, veremos na coluna à direita, na seção "_Text_", o nome da fonte utilizada nesse trecho: _Krona One_. Clicaremos também no parágrafo e veremos na mesma coluna o nome da sua fonte: _Montserrat_. Como utilizaremos essas fontes diferentes do Figma em nosso projeto?

**Guilherme:** Precisaremos trazer para o projeto essas fontes de alguma forma. Importar.

**Rafaella:** Importar, exatamente.

**Guilherme:** Essas fontes já estão em um lugar: o **_Google Fonts_**.

**Rafaella:** Exatamente! Acessaremos o site do Google e na barra de pesquisa digitaremos "google fonts". Clicaremos no primeiro link, o qual nos direcionará para o [página inicial do Google Fonts](https://fonts.google.com/). Essa página abrirá com diversas opções de fontes e línguas.

**Guilherme:** Se quisermos alterar a fonte do projeto, nós podemos.

**Rafaella:** Podemos. É possível personalizar da forma que quisermos!

Como vamos importar as fontes? Por meio do Figma, copiaremos o nome da fonte "Kroma One" e colaremos no campo de pesquisa denominada "Search fonts", localizada no topo esquerdo da página do Google fonts. Após pressionarmos "Enter", a fonte que pesquisamos será exibida como resultado abaixo do campo de pesquisa. Clicaremos no resultado e seremos direcionados para a [página da fonte Krona One](https://fonts.google.com/specimen/Krona+One?query=krona+one). Vamos descê-la até a seção "Styles", onde veremos os estilos dessa fonte.

As fontes podem ter pesos diferentes: podem vir com **negrito**, com _itálico_ ou com regular. No caso dessa fonte, temos apenas a opção "Regular 400". É justamente essa que estamos utilizando no Figma. Dentro da seção "Regular 400" temos um exemplo visual da fonte neste formato e neste peso. No canto direito deste exemplo, temos um botão intitulado "_Select Regular 400_" ("Selecione Regular 400"). Vamos clicar nele. Em seguida clicaremos no ícone denominado "_View selected families_" (ou "Ver famílias selecionadas"), localizado no canto superior esquerdo da página.

Neste momento uma nova coluna será aberta à direita da página, nos informando que temos a família de fontes _Kroma One_ selecionada. Em seu interior veremos a seção "_Use on the web_" ("use na web"). Nela veremos, lado a lado, dois botões de _radio_ denominados `<link>` e `@import`, respectivamente. Eles nos permitem copiar a fonte para utilizarmos em nossas páginas web. A opção "" exibe uma _tag_ HTML para ser inserida em um link. Já a opção "@import" nos permite inserir um `@import` no CSS. Vamos selecionar a segunda opção, pois é a que normalmente utilizamos.

Após essa seleção, copiaremos o trecho de código que colaremos no CSS, exibido abaixo dos botões radio:

```xml
<style>
@import url('https://fonts.googleapis.com/css2?family=Krona+One&display=swap');
</style>
```

Deste trecho, qual parte devemos copiar?

**Guilherme:** Este trecho possui um `<style>`, porém esse `<style>` já é o arquivo CSS em que estamos.

**Rafaella:** Exato. O `<style>` está em formato de _tag_ HTML. No HTML é possível adicionarmos um trecho de CSS por meio dessa _tag_. Contudo, **_esta não é uma prática comum nos projetos_**. Se o projeto crescer de tamanho, queremos ser capazes de implementar vários estilos e criar uma ou mais folhas de estilo. Além de editá-las, se necessário.

Portanto, vamos copiar somente o trecho de CSS, sem a _tag_ `<style>`.

```less
@import url('https://fonts.googleapis.com/css2?family=Krona+One&display=swap');
```

**Guilherme:** É só copiar e colar mesmo.

**Rafaella:** Exatamente. O código trará a URL dessa fonte acompanhada do peso selecionado. Basta copiar e colar.

**Guilherme:** Os arquivos dessa fonte estão em algum lugar. Estamos falando para o CSS buscar o local dessa fonte com o `@import` e trazer para o arquivo.

**Rafaella:** Retornando ao código, acessaremos o arquivo `style.css` e na linha 1 pressionaremos "Enter" duas vezes para descer o restante do código. Em seguida, colaremos o trecho copiado no topo do arquivo.

```css
@import url('https://fonts.googleapis.com/css2?family=Krona+One&display=swap');

*{
    margin: 0;
    padding: 0;
}
```

Acabamos de importar nossa fonte.

**Guilherme:** Vamos ver o nosso código.

**Rafaella:** Acessaremos o navegador e veremos que não mudou nada. Por que isso ocorre, Gui?

**Guilherme:** Uma coisa é trazer a fonte para o projeto. Outra coisa é informar o local onde se deve aplicá-la.

**Rafaella:** Exatamente. Trouxemos a fonte, mas não estamos usando-a, de fato. Para utilizar uma fonte adicionaremos uma propriedade no elemento onde ela será aplicada. Nós a queremos no título da página, especificamente. Qual a classe desse título?

**Guilherme:** Vamos acessar o arquivo `index.html` para confirmar. Nele temos o `<h1>` cuja classe se chama `apresentacao__conteudo__titulo`.

**Rafaella:** Exato. Retornaremos ao arquivo CSS e buscaremos a seção `.apresentacao__conteudo__titulo{}`. Dentro de suas chaves, abaixo de `font-size`, adicionaremos a propriedade `font-family` para trazer a fonte trazida pelo _Google Fonts_.

```css
.apresentacao__conteudo__titulo{
    font-size: 36px;
    font-family: ;
}
```

Adicionaremos qual valor dentro de `font-family`? Retornaremos ao navegador, na página da fonte que acabamos de importar. Na coluna de "Selected Family", abaixo da seção "_Use on the web_", encontraremos a seção "_CSS rules to specify families_" (ou "regras do CSS para especificar famílias") na qual veremos o código CSS para implementar a nossa fonte.

```css
font-family: 'Krona One', sans-serif;
```

Copiaremos o trecho `'Krona One', sans-serif`, retornaremos ao arquivo CSS e o colaremos à direita do nosso `font-family`.

```css
.apresentacao__conteudo__titulo{
    font-size: 36px;
    font-family: 'Krona One', sans-serif;
}
```

Salvaremos o código e retornaremos ao navegador, onde veremos a fonte _Krona One_ aplicada ao título. Estamos bem mais próximos do que temos no Figma.

**Guilherme:** Vamos realizar o mesmo processo no parágrafo de forma bem rápida?

**Rafaella:** Vamos. No parágrafo aplicaremos a fonte _Montserrat_. Retornaremos à página inicial do _Google Fonts_ no navegador e digitaremos "Montserrat" no campo de pesquisa. A página retornará diversas opções abaixo, dentre as quais selecionaremos aquela denominada simplesmente "Montserrat".

Desceremos a página até a seção "Styles" e veremos que esta fonte possui mais de um estilo. Vamos conferir o estilo desejado acessando o Figma, selecionando o texto a ser editado e acessando a coluna à direita. No topo dela, selecionaremos a aba "Inspect". Em seu interior acessaremos a seção "CSS", a qual possui as informações da nossa fonte.

Neste caso, não vale a pena copiar e colar o código CSS diretamente do Figma.

**Guilherme:** Vai dar errado.

**Rafaella:** No Figma podemos ver o peso da fonte no atributo `font-weight` dentro da aba "Inspect": 400. Retornando à página do _Google Fonts_, é interessante observar que temos muitas opções. Na seção "Styles" buscaremos ao lado direito dos exemplos visuais de fonte o botão "_Select Regular 400_" e clicaremos nele.

Acessaremos a coluna "_Selected families_", buscaremos e selecionaremos a opção "@import". Em seguida, copiaremos o trecho entre as _tags_ de `<style>`.

```xml
<style>
@import url('https://fonts.googleapis.com/css2?family=Krona+One&family=Montserrat&display=swap');
</style>
```

**Guilherme:** Este link acoplou as duas fontes.

**Rafaella:** Exato. Voltando ao código, no arquivo CSS substituiremos o nosso `import` antigo pelo copiado. Agora estamos importando com o mesmo comando as duas fontes, _Krona One_ e _Montserrat_.

```css
@import url('https://fonts.googleapis.com/css2?family=Krona+One&family=Montserrat&display=swap');

*{
    margin: 0;
    padding: 0;
}
```

Retornaremos à coluna lateral do _Google Fonts_ onde encontraremos o código das fontes _Krona One_ e _Montserrat_, disponíveis na seção "_CSS Rules to specify families_".

```css
font-family: 'Krona One', sans-serif;
font-family: 'Montserrat', sans-serif;
```

Copiaremos o trecho da fonte a ser importada: `'Montserrat', sans-serif`, e colaremos dentro das chaves de `.apresentacao__conteudo__texto{}`, abaixo de `font-size`.

```css
.apresentacao__conteudo__texto{
    font-size: 24px;
    font-family: 'Montserrat', sans-serif;
}
```

Salvaremos nosso código e retornaremos à página da nossa aplicação no navegador, onde veremos as fontes aplicadas corretamente.

**Guilherme:** Já está muito legal.

**Rafaella:** Já.