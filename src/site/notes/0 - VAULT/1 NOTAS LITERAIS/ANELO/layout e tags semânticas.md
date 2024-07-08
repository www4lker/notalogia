---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/layout-e-tags-semanticas/","tags":["HTML","figma","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# layout e tags semânticas

## criado em: 
-  30-03-2023 - 12:35
 
### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/HTML e CSS 1\|HTML e CSS 1]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/estilizando o projeto com CSS\|estilizando o projeto com CSS]]
- [[ux ui\|ux ui]]
- tags: #HTML #figma #ANELO 
- Fontes & Links: 
- https://cursos.alura.com.br/extra/alura-mais/como-front-end-utiliza-o-figma-c858

---
## Nessa aula, você aprendeu:

-   Como consultar o layout do projeto no Figma;
-   Escrever o código base do arquivo HTML, usando as tags semânticas que fazem parte da estrutura básica do arquivo;
-   A função de cada tag meta.

---

As próximas aulas serão baseadas no Figma, que é uma ferramenta de prototipagem de interfaces, onde vamos construir o layout da página do Portfólio. Para acessá-lo, clique [aqui](https://www.figma.com/file/4EKKCbr5rS93RWP7kRjXIz/Portfolio---Curso-1?node-id=0%3A1&t=l5RuWCe75yFNoWEr-0).

Para ter a mesma visualização que a da aula, primeiramente é necessário criar uma conta ou fazer login em uma existente. Para isso, entre no site do [Figma](https://www.figma.com/) e clique em _Log In_ (caso já tenha conta) ou em _Sign Up_ (para cadastrar nova conta).

Depois de estar com uma conta conectada, é a hora de criar uma cópia do layout para a sua conta do Figma, assim garantindo o acesso de edição. Para fazer isso, entre no link do layout original que está acima e no menu superior da plataforma, clique no nome do arquivo: Portfolio - Curso 1. Irão abrir algumas opções, clique em _“Duplicate to your drafts”_.

![Tela do Figma com uma lista de opções aparecendo no topo](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula3-img1.png)

![Tela inicial do Figma ao entrar com a conta conectada](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula3-img2.png)

Fazendo um duplo clique nele você conseguirá abrir o projeto. É com esse arquivo que você irá acompanhar as aulas.

E para demonstrar como uma pessoa desenvolvedora Front-end utiliza o Figma, separamos [esse Alura+ com a Rafa Ballerini](https://cursos.alura.com.br/extra/alura-mais/como-front-end-utiliza-o-figma-c858) onde você aprenderá tudo o que é necessário para analisar um documento do Figma para transformá-lo em código, desde a exportação de imagens e ícones até a estilização com CSS.

---

**Rafaella:** Já temos todas as ferramentas para começarmos nosso projeto de fato, pois até agora só fizemos testes, aprendemos como escrever títulos e configuramos o VSCode para nosso desenvolvimento.

Como pessoas desenvolvedoras, criamos uma página de portfolio com estilos de cores e fontes próprias, ou nos baseamos em algum modelo pronto?

**Guilherme:** Geralmente, o mercado e o cotidiano de quem trabalha com desenvolvimento é dividido em dois tipos de profissionais: Há a pessoa que faz o **desenho da página** e indica onde estarão as imagens, ícones, cores e tamanhos, e que passa para a segunda pessoa que irá **codificar o _design_** com HTML, CSS, React, JavaScript e etc.

**Rafaella**: Em nosso caso, somos este segundo tipo de profissional que recebe um projeto já desenhado e tem a tarefa de _codar_ a página _web_.

A pessoa que desenha a página "do zero" faz toda uma **pesquisa** sobre ideias e direções para construir o _design_, estudando os porquês de cada elemento possuir uma cor e um formato com base na importante Experiência do Usuário ou **UX/UI**.

**Guilherme:** A Isa, nossa _designer_ aqui da Escola de Front-End da Alura produziu o _layout_ que estamos trabalhando, e ela de fato desenhou e pesquisou bastante para isso.

**Rafaella:** Na prática, existem várias ferramentas que essas pessoas utilizam para construir páginas e que servem como base para profissionais de desenvolvimento.

Uma das mais utilizadas é o **Figma**, justamente o que estamos usando para desenvolver.

A Isa já nos enviou o [link do projeto no Figma](https://www.figma.com/file/4EKKCbr5rS93RWP7kRjXIz/Portfolio---Curso-1?node-id=0%3A1&t=l5RuWCe75yFNoWEr-0) e conseguimos ter todo o acesso às informações necessárias para _codificarmos_ as páginas neste curso.

![Projeto no Figma. Temos dois blocos de conteúdo, lado a lado, centralizados sobre fundo preto. O bloco esquerdo possui um texto que se divide em duas partes: título e subtítulo. O título apresenta um texto em negrito dividido em duas cores: "Eleve seu negócio digital a outro nível" em branco, seguido de "com um Front-end de qualidade!" em ciano. O subtítulo está na cor branca, e exibe o texto de apresentação da Joana Santos. Abaixo do subtítulo, temos dois botões na cor ciano, lado a lado: no botão esquerdo temos o texto "Instagram" e no direito o texto "Github". Já o bloco direito se constitui de uma fotografia em preto e branco representando Joana Santos, uma mulher desenvolvedora, sentada em frente a um notebook aberto. A fotografia também conta com um desenho em ciano de uma linha circulando Joana e seu notebook três vezes e terminando em uma estrela.](https://cdn1.gnarususercontent.com.br/1/308174/db4f8189-1eec-4323-949e-bcb20030e7d9.png)

**Guilherme:** Se observarmos a tela inicial, os espaçamentos, a imagem, as cores e os demais elementos foram elaborados a partir de estudos.

> Se quisermos saber mais sobre _layouts_, sobre o Figma, criação de telas e outros assuntos das áreas de **Experiência de Usuário** e **Interface de Usuário**, ou _User Experience_ (UX) e _User Interface_ (UI) em inglês, há diversos cursos em formações muito interessantes aqui da **Alura**.

Nosso desafio é o segundo passo do processo, pois alguém já fez o _design_ da página e sua estrutura, mas como podemos trabalhar a partir das informações do Figma?

**Rafaella:** Primeiramente, quando abrirmos o projeto através do link disponibilizado neste curso, precisaremos ter o cadastro na plataforma para acessar todos os dados.

Além de conseguirmos visualizar a página já montada, pegaremos as informações ao clicarmos nos elementos. Por exemplo, clicando no botão de "Instagram", abriremos uma aba lateral direita contendo três abas no topo: "Design", "Protótipo" ou "_Prototype_" e "Inspecionar" ou "_Inspect_".

Basicamente utilizaremos mais a primeira e a última aba durante nosso trabalho.

Na aba de "Design", encontraremos informações sobre largura em "W:" e altura em "H:", o formato do botão, as cores que são utilizadas, entre outras.

Já na aba "Inspect", teremos outras formas de valores para as mesmas propriedades. Inclusive, na parte "Code", há um código CSS, mas não veremos isso agora.

Portanto, conseguiremos obter todos os dados necessários nesta ferramenta chamada Figma.

**Guilherme:** Nosso desafio é _codar_ o HTML das telas já construídas.

**Rafaella:** Exatamente, as transformaremos em **páginas _web_** utilizando tanto o **HTML** quanto o **CSS**.

Faremos a **estrutura dos elementos** com o primeiro, e aplicaremos a **estilização** com o segundo, adicionando cores, formatos, fontes, posicionamento e etc.

Pensando de fato no HTML e observando a página inicial no Figma, teremos o título principal no topo do bloco de código à esquerda. Abaixo, há um parágrafo seguido de dois botões, além da foto de nossa desenvolvedora da Alura à direita, mas é interessante termos uma imagem própria para nosso portfólio.

**Guilherme:** Inclusive poderemos alterar o conteúdo textual, as cores e outras propriedades se quisermos.

A seguir, vamos começar a trabalhar com o HTML!

---

**Rafaella:** Iremos iniciar nosso projeto e **transformar o design do Figma em código**.

**Guilherme:** Vamos abrir o arquivo `index.html` no VSCode. Sempre que criarmos uma página HTML, devemos escrever `<!DOCTYPE html>`, `<html>`, `<head>`, `<body>` e fechá-los?

**Rafaella:** Existem alguns atalhos que nos permitem iniciar um documento `.html` com essa estrutura básica.

Para entendermos, excluiremos todo o conteúdo do arquivo, salvaremos e notaremos que não há mais nada da página no navegador, lembrando que ainda estamos rodando o Live Server.

Em seguida, digitaremos apenas um ponto de exclamação `!` na primeira linha do documento e exibiremos uma janela de título "Emmet Abbreviation" contendo todo um código. Quando simplesmente apertarmos a tecla "Enter", toda a estrutura básica do HTML aparecerá.

```xml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

</body>
</html>
```

Também perceberemos que há mais coisas do que antes, como as três informações `<meta>` e `lang="en"`. Entenderemos o que são essas novas _tags_.

**Guilherme:** Isso é tão comum que criaram este atalho para gerar o texto automaticamente.

Fazendo uma primeira leitura, ao posicionarmos o cursor sobre `lang="en"`, exibiremos uma caixa de diálogo com um texto explicando que este trecho define a língua oficial do elemento que estamos trabalhando, que neste caso está em inglês.

**Rafaella:** Utilizaremos em português e escreveremos o conteúdo usando os acentos específicos que não são usados com `"en"`, então substituiremos por `"pt-br"` para especificar que é do Brasil.

**Guilherme:** Na quarta linha, encontraremos a primeira tag `<meta>` seguido de `charset="UTF-8"`.

**Rafaella:** O **`UTF-8`** é a **codificação dos caracteres** mais usada no mundo, pois consegue trazer todos os acentos que comentamos, além de interpretar corretamente as outras línguas.

**Guilherme:** É **Unicode**, como se fosse um grande dicionário de caracteres que usaremos na aplicação.

**Rafaella:** Se não utilizarmos o `UTF-8`, pode ser que não consigamos exibir acentos como `~` ou circunflexo `^` corretamente em alguns navegadores.

**Guilherme:** Entendi! E na quinta linha com a segunda `<meta>` que tem `http-equiv="X-UA-Compatible"` e `content="IE=edge"`, é algo para o **Microsoft Edge**?

**Rafaella:** Exato, esta é uma configuração para sempre utilizarmos sua versão mais recente neste navegador especificamente.

Caso estejamos rodando o código no Edge, é importante que coloquemos esta informação `<meta>`, além de que a pessoa usuária final que vai usar nossa aplicação pode estar rodando nele também, principalmente se forem versões anteriores.

**Guilherme:** Já na sétima linha, temos o `<title>` que já conhecemos, contendo `Document`. Na sexta linha com o terceiro `<meta>` que tem `name="viewport"` e o `content` que inclusive fica com a parte final encoberta pelo limite da tela do VSCode.

Se apertarmos as teclas "Alt + Z" com o cursor sobre esta linha, iremos fazer com que este trecho passe para a linha seguinte e fique totalmente visível dentro do espaço de texto.

Aparentemente, o conteúdo de `content` parece dizer respeito à largura e ao tamanho da imagem.

**Rafaella:** Exato, o nome `"viewport"` é o próprio **dispositivo** que acessará nossa página, e obtém sua **largura** com `width=device-width` para depois gerar a **escala** da página com `initial-scale`, que sempre iniciará com `1.0` com base na tela, seja de celular, Ipad, computador, entre outras.

Com isso, não teremos o problema dos elementos ficarem posicionados de forma errada e nem da fonte ter um tamanho desproporcional.

**Guilherme:** Cientes disso, poderemos começar alterando o conteúdo do `<title>`.

**Rafaella:** Escreveremos `Portfolio` mesmo, que é o nosso projeto. Salvaremos e abriremos o navegador para exibirmos este nome na aba. Como é uma **metainformação**, não aparecerá no corpo da página. Agora começaremos a desenvolver todos os elementos dela.

**Guilherme:** Mas só iremos escrever HTML diretamente?

**Rafaella:** Talvez sim, e há pessoas que fazem isso apesar de **não** ser recomendado, pois sempre teremos que pensar e planejar o que iremos desenvolver em nossa página _web_.

Por exemplo, é interessante analisarmos o Figma e separar nossas tarefas em partes, como pelo cabeçalho da página no topo, ou o rodapé na base, e há também o conteúdo principal no centro da tela, como no nosso caso.

No HTML, utilizamos algumas _tags_ de maneira **semântica** para separarmos de fato os elementos da página conforme as estruturas que temos. A que seguiremos será pelo cabeçalho, conteúdo principal e o rodapé.

**Guilherme:** Se acessarmos a própria plataforma da Alura, encontraremos esses elementos. Temos o _menu_ onde fazemos o _login_, o conteúdo principal ao centro e o _footer_ na base.

**Rafaella:** Às vezes precisaremos descer ou _scrollar_ para o final da página, mas este é o básico.

**Guilherme:** Então vamos criar esta estrutura! Como cada um desses elementos são feitos por _tags_ que possuem conteúdos internos, elas devem ser abertas com `<` e fechadas com `/>`.

**Rafaella:** Como são _tags_ estruturais, sim.

Primeiramente, no topo da página, teremos o menu com **`<header>`** que significa "cabeçalho", que é **diferente** de `<head>`. A inseriremos dentro de `<body>`, abrindo e fechando na mesma linha.

Em seguida, teremos o conteúdo principal em **`<main>`** na linha seguinte, que é a própria tradução do inglês.

Dentro desta _tag_, iremos colocar o título, o parágrafo, os botões e a imagem.

Na linha seguinte, teremos o `<footer>` relativo a "rodapé", também abrindo e fechando.

```xml
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
</head>
<body>
    <header></header>
    <main></main>
    <footer></footer>
</body>
</html>
```

**Guilherme:** Com isso, teremos a estrutura básica do HTML, e vamos começar com o `<main>`.

--
**Rafaella:** Vamos **começar a _codar_** dentro do nosso **`<main>`**.

O primeiro passo é **entender** o que precisamos fazer em nossa página _web_ e **planejar** o que iremos estruturar.

**Guilherme:** Observando a tela inicial do projeto no Figma, notaremos dois blocos de texto um em cima do outro, dois botões lado a lado logo abaixo de "Instagram" e "GitHub", e uma imagem à direita desses elementos.

**Rafaella:** Uma boa sugestão é começar a trabalhar com os elementos **da esquerda para direita, de cima para baixo**. Então começaremos pelo título, depois pelo parágrafo, seguido pelos botões, e por fim colocaremos a foto.

Vamos fazer isso no nosso arquivo `index.html` no VSCode.

Abriremos uma nova linha dentro da _tag_ `<main>` e começaremos com o título usando **`<h1>`**, em que "h" remete a "_heading_".

Voltaremos ao Figma e clicaremos várias vezes sobre o texto para o selecionarmos inteiro, para depois copiarmos o escrito com "Ctrl + C" e colarmos dentro de `<h1>` com "Ctrl + V".

```xml
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
</head>
<body>
    <header></header>
    <main>
        <h1>Eleve seu negócio digital a outro nível com um Front-end de qualidade!</h1>
    </main>
    <footer></footer>
</body>
</html>
```

**Rafaella:** Outro detalhe importante é que, ainda na parte do título, o trecho "com um Front-end de qualidade!" possui uma cor diferente que o destaca do começo do texto.

Para fazer essa diferenciação, existe uma _tag_ semântica em nosso próprio HTML que indica ao navegador que deve destacar essa parte.

**Guilherme:** É para deixarmos este trecho mais em forte evidência mesmo.

**Rafaella:** Para isso, antes desta parte de destaque, aplicaremos a **`<strong>`**, que é justamente a palavra em inglês para "forte", e a fecharemos antes do fechamento da `<h1>`, pois a _tag_ está dentro dela.

```xml
<!DOCTYPE html>
<html lang="pt-br">

//código omitido

<body>
    <header></header>
    <main>
        <h1>Eleve seu negócio digital a outro nível<strong>com um Front-end de qualidade!</strong></h1>
    </main>
    <footer></footer>
</body>
</html>
```

**Rafaella:** Salvaremos esse código e veremos o resultado no navegador.

![Página do projeto no navegador, em que o nome da aba é "Portfólio" e a url é "127.0.0.1:5500/index.html". No corpo da página, aparece somente o texto "Eleve seu negócio digital a outro nível com um Front-end de qualidade!" em uma linha única, escrito em preto com fonte serifada e em um fundo branco.](https://cdn1.gnarususercontent.com.br/1/308174/6d8ed07a-d723-43f9-b29f-87cf4ee1ad02.png)**Guilherme:** Visualmente, não há diferença entre os trechos, mas o navegador já sabe que a parte importante deve ser destacada.

**Rafaella:** Trabalharemos com essas questões visuais quando entrarmos na parte de **estilização**.

Em seguida, observando o Figma, teremos o nosso parágrafo que também copiaremos e, logo abaixo da `</h1>` no `index.html`, adicionaremos a _tag_ **`<p>`** de "parágrafo" que já conhecemos para então colarmos o texto dentro dela.

```xml
<!DOCTYPE html>
<html lang="pt-br">

//código omitido

<body>
    <header></header>
    <main>
        <h1>Eleve seu negócio digital a outro nível<strong>com um Front-end de qualidade!</strong></h1>
        <p>Olá! Sou Joana Santos, desenvolvedora Front-end com especialidade em React, HTML e CSS. Ajudo pequenos negócios e designers a colocarem em prática boas ideias. Vamos conversar?</p>
    </main>
    <footer></footer>
</body>
</html>
```

**Guilherme:** Lembrando que o escrito pode mudar, afinal nem todo mundo se chama "Joana Santos". Vamos salvar e ver o resultado.

![Mesma página do projeto no navegador de antes, porém, no corpo da página abaixo do texto anterior de título, há o parágrafo em menor tamanho escrito em uma linha única, na cor preta com fonte serifada e em um fundo branco.](https://cdn1.gnarususercontent.com.br/1/308174/cb1b3050-9bb6-4022-8e4e-bb72274cc682.png)

**Rafaella:** Com isso, já teremos as duas partes de texto em nossa página, e agora vamos colocar os dois botões. Mas o que são de fato?

**Guilherme:** Excelente pergunta; quando clicamos em "Instagram" ou "GitHub", o esperado é que nos redirecionem para outro lugar. Mas esta questão de **redirecionamento** para outra página geralmente **não é o comportamento de um botão**.

Existe uma _tag_ do HTML chamada `<Botao>` que é usada quando estamos trabalhando com formulário, por exemplo. Semanticamente, neste nosso caso, usaremos a _tag_ âncora **`<a>`**.

**Rafaella:** Certo, então a adicionaremos após `</p>` e sabemos que ela abre e fecha também. Mas o que colocamos como conteúdo?

**Guilherme:** Colocaremos o _link_. Se voltarmos ao código, o que escrevermos dentro dela como um texto é o que será exibido na tela, ou seja, `Instagram`. Inseriremos outra _tag_ `<a>` abaixo e adicionaremos `Github` para salvarmos e vermos o resultado.'

```xml
<!DOCTYPE html>
<html lang="pt-br">

//código omitido

<body>
    <header></header>
    <main>
        <h1>Eleve seu negócio digital a outro nível<strong>com um Front-end de qualidade!</strong></h1>
        <p>Olá! Sou Joana Santos, desenvolvedora Front-end com especialidade em React, HTML e CSS. Ajudo pequenos negócios e designers a colocarem em prática boas ideias. Vamos conversar?</p>
        <a>Instagram</a>
        <a>Github</a>
    </main>
    <footer></footer>
</body>
</html>
```

**Guilherme:** Na página no navegador, notaremos que aparece o texto "Instagram Github".

**Rafaella:** Mas não está clicável, e parece apenas um outro parágrafo.

**Guilherme:** Está exatamente igual, e não é esse comportamento que esperamos, pois queremos poder clicar e nos redirecionar para o Instagram ou o Github.

Poderemos colocar o Instagram da Rafaella para exemplificar.

**Rafaella:** A _tag_ âncora é bastante semelhante à propriedade que estávamos colocando de imagem com **`src`**, que vem de _source_ ou "fonte", e que ser para buscar o caminho para encontrá-la.

Em `<a>`, vamos usar um _hiperlink_ que nos permite clicar e ir para outra pagina. Escrevendo **`href`** entre `a` e `>` na abertura da primeira _tag_, e já exibiremos uma caixa com uma descrição.

Depois do sinal de igual `=`, escreveremos a URL de destino entre aspas para onde vamos nos redirecionar. Neste exemplo, será `"https://instagram.com/rafaballerini"`, depois salvaremos e veremos o que vai acontecer.

```xml
<!DOCTYPE html>
<html lang="pt-br">

//código omitido

<body>
    <header></header>
    <main>

//código omitido

        <a href="https://instagram.com/rafaballerini">Instagram</a>
        <a>Github</a>
    </main>
    <footer></footer>
</body>
</html>
```

![Mesma página do projeto no navegador contendo o título e parágrafo, porém, abaixo dele, está escrito "Instagram" sublinhado em azul ao lado de "GitHub" escrito em preto com a mesma fonte serifada dos demais textos.](https://cdn1.gnarususercontent.com.br/1/308174/55987566-934a-435a-9ecf-d0ddc02ce6ed.png)

**Guilherme:** Já mudou e visualmente está diferente.

**Rafaella:** Já se tornou um elemento clicável com o destaque sublinhado em azul, e quando clicamos, nos redirecionaremos para a página do Instagram que colocamos em `href`.

**Guilherme:** No botão de "Github", pode colocar o meu mesmo como exemplo para vermos.

**Rafaella:** Teremos o mesmo formato usando `href` igual a `"https://github.com/guilhermeonrails"`. Vamos salvar e ver o resultado no navegador.

```xml
<!DOCTYPE html>
<html lang="pt-br">

//código omitido

<body>
    <header></header>
    <main>

//código omitido

        <a href="https://instagram.com/rafaballerini">Instagram</a>
        <a href="https://github.com/guilhermeonrails">Github</a>
    </main>
    <footer></footer>
</body>
</html>
```

**Rafaella:** Quando clicarmos em "Github" também já clicável e sublinhado em azul, iremos para a página do GitHub do Guilherme.

**Guilherme:** Revisando o que fizemos, construímos tudo isso dentro do `<main>` até agora.

Na _tag_ `<strong>`, pegamos o texto em destaque no Figma, mas visualmente não há diferença no navegador. Mesmo não tendo alterado nada, já indicou que é algo a ser destacado.

Também criamos o parágrafo com `<p>`, além dos dois _links_ que redirecionam para o Instagram e GitHub, que não são literalmente dois botões.

Deixaremos essas duas âncoras `<a>` para outros sites com aparência de botão apenas, como está na tela no Figma.

**Rafaella:** Exatamente. Nosso último passo é inserir a fotografia da direita, e conseguimos fazer seu _download_ direto do Figma, afinal não a encontraremos no Google.

Mas poderemos usar qualquer outra imagem que tivermos salvas no computador.

Para pegarmos direto do Figma, clicaremos sobre o elemento que queremos baixar e, na aba lateral direita chamada "Design", teremos a opção de "Export" onde clicaremos no botão de "Export Imagem" para fazermos o _download_.

Abriremos a pasta em que o arquivo foi salvo e poderemos renomear se quisermos, como apenas "imagem" mesmo para padronizarmos.

Clicando e arrastando a imagem para dentro do VSCode, criaremos o arquivo `imagem.png` na lista lateral esquerda chamada "Explorer", da mesma forma que fizemos com o HTML 5.

Para a adicionarmos no código, inseriremos a _tag_ **`<img>`** que já conhecemos e sabemos que é única, então não precisamos abrir e fechar.

A propriedade usada para encontrar a imagem é a **`src`** que será igual a `"imagem.png"` entre aspas, pois já está na mesma pasta do projeto, bastando só escrever o nome do arquivo.

Além disso, usaremos outra importante propriedade chamada **`alt`** que diz respeito ao texto alternativo que descreve a imagem, como `"Foto da Joana Santos programando"` por exemplo.

Vamos Salvar e ver o resultado no navegador.

```xml
<!DOCTYPE html>
<html lang="pt-br">

//código omitido

<body>
    <header></header>
    <main>

//código omitido

        <a href="https://instagram.com/rafaballerini">Instagram</a>
        <a href="https://github.com/guilhermeonrails">Github</a>
        <img src="imagem.png" alt="Foto da Joana Santos programando">
    </main>
    <footer></footer>
</body>
</html>
```

![Mesma página do projeto no navegador contendo o título, o parágrafo e os links de "Instagram" e "GitHub" sublinhados em azul com a mesma fonte serifada dos demais textos. Ao lado deles, está a fotografia em preto e branco representando Joana Santos, uma mulher desenvolvedora, sentada em frente a um notebook aberto. A imagem também conta com um desenho em ciano de uma linha circulando Joana e seu notebook três vezes e terminando em uma estrela.](https://cdn1.gnarususercontent.com.br/1/308174/3727c664-fc1e-4c63-b16f-876661f8727e.png)

**Rafaella:** Ainda não está como o projeto do Figma porque ainda temos muito o que estilizar, e é o que faremos a seguir.

---

# Para saber mais: tags semânticas


Quando começamos um arquivo HTML, há uma estrutura padrão que é usada em qualquer projeto. É importante saber quais são as tags que precisam ser implementadas e entender suas funções dentro do código. Para facilitar esse processo, utilizamos as **tags semânticas**, que são tags descritivas sobre o conteúdo que armazenam, como é o caso das tags `<header>`, `<main>` e `<footer>`, que conhecemos nessa aula. Elas servem tanto para otimizar a leitura pelos navegadores, como pelas pessoas desenvolvedoras que vão fazer a manutenção do código.

Para aprender mais sobre as tags que fazem parte da base de um arquivo HTML, você pode ler a documentação MDN [“Semântica”](https://developer.mozilla.org/pt-BR/docs/Glossary/Semantics) e conhecer outros elementos semânticos disponíveis para tornar o seu código mais claro, seja para outras pessoas programadoras, para navegadores ou mecanismos de buscas.