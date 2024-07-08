---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/classes-css/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# classes CSS

## criado em: 
-  30-03-2023 - 14:05

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/HTML e CSS 2\|HTML e CSS 2]]
- [[reset CSS - o que é \|reset CSS - o que é ]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/posicionando elementos\|posicionando elementos]]
- tags: #ANELO
- Fontes & Links: 
- https://cursos.alura.com.br/course/html-css-classes-posicionamento-flexbox/task/118638

---

**Rafaella:** Estamos em uma situação na qual queremos determinar uma cor específica para tag `strong` sem que essa formatação passe para todos os elementos que a utilizam. E existe uma maneira para fazermos isso.

No arquivo `style.css`, estamos usando as tags `body` e `strong` como **seletores** do CSS, o que significa que conseguimos escrever o nome da tag, as chaves (`{}`) e o que queremos que altere nela dentro dessas chaves. No caso do `body`, é a cor do fundo e da letra.

Contudo, essa não é a única forma de seletor, e uma dela que é muito utilizada no dia a dia é o **seletor de classe** que consegue resolver justamente esse problema. Portanto, vamos aprender como utilizá-lo.

Para isso, acessaremos o Google.

**Guilherme:** Podemos escrever, por exemplo, "classes CSS W3C". Inclusive o correto é "W3S", mas o Google conseguiu achar para nós como "W3C". Podemos abrir o primeiro resultado, que é o [CSS .class Selector - W3Schools](https://www.w3schools.com/cssref/sel_class.php).

Nessa página ele tem um exemplo e uma definição, que está em inglês. Vamos alterar para o português, clicando na opção de tradução do google tradutor, que fica no canto direito da barra de endereço.

> **Dica:** Inclusive pode aparecer uma janela flutuante com a opção de tradução no lado inferior direito da barra de endereços. O idioma inglês estará selecionado e, ao lado dele, aparecerá a opção "português". Basta clicar nela.

Então na seção "**Definição e Uso**" descobrimos que um seletor `.class` irá selecionar elementos com os atributos de uma classe específica. Essa explicação ficou um pouco confusa, mas o que ela quer dizer é que conseguimos selecionar partes para o CSS estilizar. Para selecionar cada elemento de uma classe específica, devemos escrever o ponto (referindo-se ao ponto final, ou seja, `.`).

Voltando para o nosso CSS, Rafa, repara que todas as nossas tags estão exatamente com o nome delas.

**Rafaella:** Exato!

**Guilherme:** O `body` e o `strong`, mas poderia ser também o `h1`, `h2`, `h3`, `h4` e assim por diante. Basta escrevermos na estrutura `nomeDaTag {}` e dentro das chaves escrevermos as configurações.

Quando trabalhamos com classes, é diferente. Para criarmos classes no CSS, primeiramente vamos ao HTML e especificamos que a tag possui uma classe específica.

**Rafaella:** Então, no Explorador, abriremos o arquivo `index.html` e na linha 13, onde temos a `<strong>` adicionaremos a propriedade `class` (classe). Essa propriedade fica realmente dentro da tag, como descobrimos com as imagens e com a âncora.

Portanto para definir uma classe para qualquer tag, basta escrever `class=""` e entre as aspas o nome da classe que queremos, tudo isso dentro da tag, no caso, `<strong class="">`.

```javascript
//código suprimido
<strong class="">com um Front-end de qualidade!</strong></h1>
//código suprimido
```

Essa estrutura se aplica a **qualquer tag** para qual queiramos definir uma classe.

**Guilherme:** Boa, Rafa. Eu vou apenas fechar o Explorador para conseguirmos visualizar o código melhor.

E como funciona a **nomeação da classe**? Pode ser qualquer nome?

**Rafaella:** Existem diversos padrões que podemos seguir, mas nesse começo, recomendo sempre escrevermos algo que deixa bem óbvio do que se trata. Por exemplo, estamos no título da nossa página, e o `strong` é um **destaque** desse título, então seria bom nomearmos a classe como "titulo-destaque" ou "destaque-titulo".

**Guilherme:** Então sempre nomeamos de uma forma que faça sentido para aquele elemento.

**Rafaella:** Isso mesmo. Depois aprenderemos também um padrão que podemos seguir, por exemplo, estamos usando a classe "titulo-destaque", então para classe do título podemos escrever apenas "titulo". Então conseguimos encontrar padrões de nomes.

**Guilherme:** E aprenderemos isso com o passar do tempo.

**Rafaella:** Vamos então nomear como `class="titulo-destaque"`.

**Guilherme:** Descobrimos também que para selecionar esse `titulo-destaque` precisamos usar o ponto (`.`) . Portanto voltaremos para o arquivo `style.css` e, no lugar do `strong`, escreveremos `.titulo-destaque`.

```css
body {
    background-color: #000000;
    color: #F6F6F6;
}

.titulo-destaque {
    color: #22D4FD;
}
```

Reparem que agora estamos em um momento diferente. Sempre que criamos uma classe CSS, selecionamos essa classe com o ponto final.

**Rafaella:** É a forma que informamos para o CSS que se trata de uma classe e não apenas de uma tag do HTML.

**Guilherme:** Temos outro desafio agora, Rafa. Pelo que fizemos, apenas o `titulo-destaque` estará na cor azul, enquanto o segundo `strong`, que está na linha 14 e que removeremos depois, porque foi apenas um exemplo, não estará com uma cor diferente.

**Rafaella:** Exato. É apenas para o `strong` do título estar azul.

**Guilherme:** Quando abrimos nosso projeto no navegador, observamos que funcionou. Conseguimos deixar a mesma tag, mas com uma classe específica, o que é bem comum, certo Rafa?

**Rafaella:** Isso! A classe é como um agrupamento de tipo. E podemos perceber que mesmo assim o trecho "**React, HTML e CSS**", na segunda linha, ficaram em destaque, mas apenas em negrito.

Isso ocorre porque o `strong` faz essa alteração quando é inserido em uma tag `<p>`. Portanto não se assustem, não é nenhuma configuração fora do normal ou alteração do CSS que fizemos, é porque utilizamos o `<strong>` que, por padrão, deixa o trecho em negrito dentro do parágrafo.

Porém podemos remover essa tag da linha 14, porque esse destaque não existe no modelo do [nosso Figma](https://www.figma.com/file/EjGLdArvshxGrwP9YDTZzT/Forma%C3%A7%C3%A3o-HTML-e-CSS?node-id=378%3A863&t=AnPDzv24lI2M8UXg-1). Ao retornarmos à página, observamos que o destaque sumiu no parágrafo, mas se manteve no título.

Agora aprendemos a utilizar classes no CSS e já podemos criá-las e utilizá-las em outras partes do projeto.

---

# Class

Agora você já sabe que o atributo `class` permite ao CSS selecionar e acessar elementos específicos através dos seletores de classe, mas para entender de forma mais clara e objetiva, você pode acessar a documentação oficial [MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Global_attributes/class) para tirar dúvidas.

# Nomes de classes no CSS

Quer entender as boas práticas para dar um nome nas classes do CSS? Recomendamos a leitura do artigo [Nomes de classes no CSS](https://www.alura.com.br/artigos/nomes-de-classes-no-css), que aborda de forma simples e prática esse conceito.

---
## reset css


**Guilherme:** Estamos com nosso layout um pouco desorganizado. Conseguimos adicionar as cores com hexadecimal, mas o posicionamento não está legal, Rafa.

Se observarmos, nosso título está grudado à lateral esquerda e parece que ele ocupa uma linha inteira, como também acontece com o parágrafo. O interessante é que , se rolamos a página um pouco para baixo, os links e a imagem parem também aparecer na mesma linha

A sensação que eu tenho é que, sem configurarmos, um estilo já foi aplicado.

**Rafaella:** Exatamente. Já existe um padrão quando estamos desenvolvendo em HTML e CSS, e justamente por isso, como pessoas desenvolvedoras Front-End, nós utilizamos a **modularidade**, através do "reset CSS".

Então resetamos o padrão que já existe, como uma decoração nos nossos links ou o espaçamento enorme que existe entre o início da nossa página e o título. No Figma, todo conteúdo está no centro da página, e para termos o controle de posicionamento desse título, não podemos contar com esse espaço do começo, que nem sabemos de quanto é.

**Guilherme:** Sendo que esse espaço não é padrão para todos os navegadores, certo?

**Rafaella:** Ainda tem esse ponto, **os navegadores têm padrões um pouco diferentes**.

**Guilherme:** Mudando a cor ou o tipo do link, por exemplo. Então realmente temos um problema, que é, temos um estilo e precisamos removê-lo.

**Rafaella:** Precisamos resetá-los para termos o controle de todos eles.

E podemos usar diversos tipos de reset para o CSS, desde gigantes, que resetam várias tags, e nem descobriremos tão cedo na nossa carreira, até os mais simples, com os quais conseguimos restar as tags mais usadas. Por exemplo, conseguimos resetar o espaçamento da página, ajustando **a margem e o _padding_**, que são duas propriedades que entenderemos agora como funcionam no CSS.

**Guilherme:** Antes disso, conseguimos ver esse espaçamento, Rafa?

**Rafaella:** Consegue!

**Guilherme:** Pessoal, o teste é o seguinte. Clicamos com o botão direito do mouse na página e selecionamos "Inspecionar", abrindo uma coluna na metade direita da janela com as **_DevTools_**.

Na parte superior dessa coluna pode aparecer a opção "_Switch DevTools to Portuguese_", e nós podemos clicar nela para mudar para o idioma das DevTools para o português. Na aba "Elementos" das _DevTools_ há duas divisões na parte superior: na direita está a área do código e na área esquerda está a área de "**Estilos**".

Sendo assim, vamos clicar no botão "Selecionar Elemento" representado pelo ícone de um quadrado com o cursor do mouse no canto inferior direito. Esse botão está no canto superior esquerdo da _DevTools_, mas também podemos usar o atalho "Ctrl + Shift + C" para ativá-lo.

Feito isso, deixaremos o mouse no elemento do título, que está na metade esquerda da janela. Ao selecionar o título, a sensação que eu tenho, Rafa, é que tem o texto e em cima e embaixo tem algo envolvendo o texto.

Ao observarmos na aba "Estilos" da _DevTools_, na parte inferior temos vários retângulos um dentro do outro, cada vez menores em cores diferentes. Esses retângulo são:

-   _margin_ (margem): o maior e mais externo retângulo, que está na cor laranja-claro;
-   _border_ (borda): está dentro do retângulo da margem, sendo proporcionalmente menor a ele, e é da cor amarelo claro;
-   _padding_ (espaçamento): retângulo verde-claro que está dentro do retângulo da borda, também proporcionalmente menor a ele;
-   conteúdo: um retângulo azul-claro que está dentro do retângulo de espaçamento e é proporcionalmente menor que ele.

![Modelo com os retângulos em "Elementos > Estilos" da DevTools". Nele os retângulos estão dispostos como na descrição acima](https://cdn1.gnarususercontent.com.br/1/935581/0741f5c5-fe88-439a-924a-e1d1c5b6518f.png)

Na aba "Estilos", ao passarmos o mouse sobre o retângulo da margem, percebemos que no título da página, na metade esquerda da janela, observamos essa margem em destaque também, mudando a cor. Rafa, minha pergunta agora é um pouco estanha, mas vamos abrir a documentação para descobrirmos o que está acontecendo?

**Rafaella:** Ótima ideia! Vamos abrir outra aba e pesquisar no W3S, que já estávamos consultando, por "**_Box Model_**" (modelo de caixa). Sendo assim, vamos pesquisar no Google "w3s _box model_" e abrir a página correspondente ao resultado, que é o primeiro link.

Abrindo a [página de _box model_ no W3S](https://www.w3schools.com/css/css_boxmodel.asp), encontramos a documentação com a mesma estrutura que vimos na aba "Estilos".

**Guilherme:** Porém as informações estão mais detalhadas, certo?

**Rafaella:** Estão. Eu vou traduzir a página e percebemos que esse é o **modelo de caixa CSS**, então cada elemento que estamos adicionando à página, ou seja, o título, o parágrafo e a imagem, todos são elementos do CSS.

Então quando voltamos para nossa página do projeto e passamos o mouse por cada um dos elementos, na aba "Estilos" constatamos que todos seguem o modelo de caixa. Da mesma forma, visivelmente enxergamos uma borda amarela em cima e embaixo do conteúdo no qual deixamos o mouse em cima. Essa borda representa a **margem**.

Nós não adicionamos nenhuma informação sobre margem na nossa página, então é isso que estávamos conversando. Existe um padrão que é criado automaticamente nas nossas páginas.

Voltando para documentação, descobrimos que existem, na verdade, três propriedades que conseguimos definir para o nosso elemento. O primeiro é a **margem**, que é mais externa, seguido da **borda**, que não está visível no nosso projeto, mas ela existe.

E dentro da borda existe o **_padding_**, que é o espaçamento da borda até o conteúdo. Então conseguimos encolher o conteúdo em relação à borda com o _padding_, enquanto da borda em relação aos elementos externos temos outro espaçamento, que é a _margin_.

**Guilherme:** Eu gostei até da explicação presente no W3S, Rafa. Nós temos o conteúdo, que é a parte visível, e temos várias outras coisas invisíveis que não sabemos que estão acontecendo.

Sabemos que existe um espaço ali, que agora sabemos que é a margem, além disso exista a borda, e o W3S explica que se trata do contorno do preenchimento do conteúdo, seja imagem ou texto.

**Rafaella:** O conteúdo e o padding.

**Guilherme:** Então Rafa, acho que nosso primeiro passo é tirar a margem de todos os elementos.

**Rafaella:** Vamos remover essa margem e também o _padding_, para garantirmos que não teremos esse espaçamento.

E voltando para o VS Code, no CSS existe uma forma de nos referirmos a todos os elementos da nossa página HTML.

**Guilherme:** Então não precisamos escrever todas as tags e classes, correto?

**Rafaella:** Não precisa. No nosso arquivo `style.css`, podemos fazer isso digitando apenas um asterisco (`*`). Assim ele pega todos os elemento da página. Em seguida, como em todos os elementos, abrimos chaves e, dento delas escrevemos `margin: 0` e `padding: 0`.

```css
* {
    margin: 0;
    padding: 0;
}
```

Essa é a configuração padrão que mais utilizamos, pessoal. Existem outros resets CSS que retiram a decoração, entre outras coisas, mas usaremos só esses no nosso projeto, que é bem mais tranquilo. Feito isso, vamos salvar e conferir o resultado no navegador.

Com isso conseguimos notar que todo espaço que tínhamos entre o conteúdo e a página desapareceu. Inclusive podemos clicar para Inspecionar a página, sendo que às vezes a aba "Estilos" muda de posição. Dessa vez ela está em uma divisão abaixo do código, então vamos analisar o modelo de caixas.

Quando ativamos o seletor de elementos, pressionando "Ctrl + Shift + C" e passamos o mouse sobre os elementos da nossa página, reparamos que realmente não tem mais aquela margem padrão. Isso nos ajuda a ter muito mais controle dos elementos da nossa página.