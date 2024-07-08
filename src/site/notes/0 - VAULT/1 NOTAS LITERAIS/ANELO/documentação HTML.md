---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/documentacao-html/","tags":["HTML","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# documentação HTML

## criado em: 
-  30-03-2023 - 12:01

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/HTML e CSS 1\|HTML e CSS 1]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/layout e tags semânticas\|layout e tags semânticas]]
- tags: #HTML #ANELO 
- Fontes & Links:  https://cursos.alura.com.br/course/html-css-ambiente-arquivos-tags/task/118939

---
## Nessa aula, você aprenderá:

-   A importância da documentação W3S;
-   O que é HTML e porque é considerada uma linguagem de marcação;
-   Estruturar um documento HTML com tags e elementos;
-   A utilidade da introdução `<!DOCTYPE html>`;
-   Diferença entre a metainformação presente no `<head>` e o conteúdo presente no `<body>` de uma página HTML;
-   Criar textos alternativos (alts) para uma imagem;
-   Acessar a Developer Tools (Ferramentas para Desenvolvedores) de um navegador;
-   Quirks mode (modo peculiaridade);
-   Utilizar extensões no Visual Studio Code (Live Server por exemplo).

---

**Rafaella:** Criamos nosso primeiro arquivo HTML. Agora vamos aprender a escrever o texto em HTML.

**Guilherme:** Isso. O que geralmente acontece quando queremos aprender uma linguagem de programação ou uma tecnologia nova? Procuramos o **_manual_**. No nosso caso, procuramos a **_documentação da linguagem_**.

**Rafaella:** Exatamente. Temos manuais de diversas tecnologias. Se quisermos aprender Javascript, procuraremos a documentação. Isso é muito importante.

**Guilherme:** Vamos abrir a documentação. Recomendamos, inicialmente, a **_w3s html intro_**. Vamos digitar esse nome na barra de pesquisa do Google.

Clicaremos no primeiro link retornado na pesquisa, o qual nos direcionará para a [página de introdução do HTML no site W3Schools](https://www.w3schools.com/html/html_intro.asp). Essa página nos mostra o conteúdo em inglês. Vamos colocá-la em português.

No topo da tela há uma barra de menus branca. Abaixo desta, há uma barra secundária de menus na cor preta, onde clicaremos no ícone de planeta denominado "Translate W3Schools", localizado à direita. Neste momento, à esquerda desse ícone, veremos um botão denominado "selecione o idioma", no qual clicaremos e selecionaremos a opção "Português". Após esse procedimento, a página será exibida em português.

# Afinal, o que é HTML?

**Rafaella:** Encontraremos a resposta na página que abrimos. Nela há a seção "O que é HTML?", onde encontramos o seguinte tópico:

-   HTML significa _Hyper Text Markup Language_ (ou "linguagem de marcação de hiper texto").

Ou seja, o HTML é uma **_linguagem de marcação_**. Existe uma polêmica envolvendo o HTML e que alimenta dúvidas sobre o HTML ser uma linguagem de programação ou não. De fato, o HTML é uma linguagem de marcação, e por isso, não se trata de uma linguagem de programação. Utilizamos o HTML para designar as partes do texto.

Retornando ao nosso documento de texto, podemos ver que marcamos a frase "Isso é um título" como um título. No caso do Docs Google, não precisamos escrever _tags_ ou códigos para marcação, pois o programa utilizado facilita esse processo. Já no HTML **_utilizaremos tags_** para marcar títulos, parágrafos e imagens.

**Guilherme:** Voltando à página do HTML, ainda na seção "O que é HTML?" encontramos os dois tópicos abaixo:

-   HTML descreve a estrutura de uma página da Web.
-   Os elementos HTML rotulam partes do conteúdo como "isto é um título", "isto é um parágrafo", "isto é um link", etc.

Isso significa que teremos um local onde rotularemos cada elemento da página: é como se indicássemos "isto será um título", "isto será uma imagem","estes serão dois parágrafos". O objetivo do HTML é **_marcar toda a página Web_**.

É interessante notar que existe um código por trás das páginas com as quais interagimos indicando a função de cada elemento.

**Rafaella:** Abaixo da seção "O que é HTML?" temos a seção "Um Documento HTML Simples" no qual é possível ver um _spoiler_ do que seriam as _tags_:

```xml
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

**Guilherme:** Se olharmos este trecho não vamos entender muita coisa. A melhor forma para aprendermos uma técnica ou linguagem relacionada à tecnologia é **_praticando_**. Não existe outro jeito.

**Rafaella:** Exatamente.

**Guilherme:** Nós criamos um arquivo simples no Docs Google, indicando um título, um parágrafo e uma imagem. Conforme praticamos o HTML, essa tarefa se tornará comum.

Conforme podemos ver no trecho de exemplo, toda propriedade do HTML começa com o sinal `<` e termina com o sinal `>`.

**Rafaella:** No interior destes sinais, temos o rótulo daquela porção da página Web.

**Rafaella:** Exatamente. Vamos criar esse código no VS Code. Criaremos uma _tag_ por vez e entenderemos o que cada uma significa.

**Rafaella:** Perfeito.

A primeira se chama `<!DOCTYPE html>`. Conforme a própria página do HTML define, se trata de uma declaração que define o documento como um documento HTML5. Mesmo que criemos a extensão `.html`, é importante declarar esta _tag_ pois ela define a versão. É possível copiá-la e colar no VS Code, mas vamos escrever do zero para que entendamos melhor.

Retornaremos ao VS Code, criaremos nossos sinais `<` e `>`. Entre eles escreveremos um `!DOCTYPE` em letras maiúsculas, daremos um espaço e escreveremos `html` em letras minúsculas.

```xml
<!DOCTYPE html>
```

**Guilherme:** O que a Rafa comentou é interessante. Essa _tag_ serve para identificar que estamos trabalhando nesse arquivo HTML com a versão 5. Esta será a versão utilizada quando abrirmos este projeto no navegador. Se estamos falando da versão 5, significa que existiram versões diferentes? A resposta é **_sim_**. Faremos um teste sobre isso depois.

**Rafaella:** Retornando à página do HTML, a próxima _tag_ a ser copiada será a `<html>`. Esta _tag_ indica que tudo o que existir dentro dela será o documento HTML.

**Guilherme:** A documentação nos informa que o `<html>` é o elemento raiz de uma página HTML, ou seja, este elemento será a base para tudo o que existir na página.

Vamos retornar ao VS Code e adicioná-la abaixo de `<!DOCTYPE html>`.

```xml
<!DOCTYPE html>
<html>
```

Neste momento, o Visual Studio Code completará automaticamente a _tag_ que abrimos com a _tag_ posterior, ou seja, de fechamento.

```xml
<!DOCTYPE html>
<html></html>
```

O que seria a _tag_ posterior? Temos algumas _tags_ que, para serem implementadas, precisam de uma abertura e de um fechamento.

Se voltarmos à página do HTML no navegador, veremos que existe a _tag_ de fechamento `</html>` no final do trecho, precedida por vários outros elementos. Isso significa que todos os elementos entre `<html>` e `</html>` farão parte desta _tag_.

> Toda _tag_ de fechamento possui uma barra (`/`) após o sinal `<`.

Caso o VS Code não preencha a _tag_ automaticamente, basta escrevê-la manualmente.

Posicionaremos o cursor no meio das _tags_ `<html>` e `</html>` e pressionaremos "Enter" para abrir um espaço onde começaremos a escrever nosso documento.

```xml
<!DOCTYPE html>
<html>

</html>
```

**Guilherme:** Já temos a nossa _tag_ HTML. No caso do `<!DOCTYPE html>` não existe uma _tag_ de fechamento. Isso é um padrão. Não sabemos o motivo exato disso.

**Rafaella:** Exato. Existem _tags_ com fechamento e outras sem. Neste curso veremos todos os tipos de _tags_.

Antes de continuar, salvaremos o código com o atalho "Ctrl + S".

**Guilherme:** O HTML indica que a nossa página abriu. Voltaremos ao navegador e veremos nossa próxima _tag_: `<head>`, a qual, segundo a documentação, contém meta informações sobre a página HTML.

**Rafaella:** O que seriam meta informações? São as informações sobre o próprio documento. São _metatags_. Vamos adicioná-las dentro do tal `<head>`.

Vamos retornar ao VS Code, e entre as _tags_ de abertura e fechamento do `html` adicionaremos a `<head>`.

> **Importante:** Para indentarmos o código — ou seja, para mantê-lo organizado visualmente — devemos pressionar "Tab" a cada _tag_ que abrirmos no interior de outra, criando dessa forma uma distância entre as _tags_ e impedindo que todo o código fique "reto". Após a abertura e o fechamento da `head` pressionaremos "Enter". Dentro do espaço criado da `<head>` escreveremos as meta informações da nossa página.

```xml
<!DOCTYPE html>
<html>
    <head></head>
</html>
```

**Guilherme:** Temos conteúdos na página que podemos visualizar e outros que não vemos diretamente.

**Rafaella:** Exato. Consultando a página do HTML, veremos que a primeira _tag_ de metainformação é o `<title>`. No VS Code, vamos adicioná-la entre as _tags_ do `<head>`, sem esquecer de pressionar "Tab" antes.

```xml
<!DOCTYPE html>
<html>
    <head>
        <title></title>
    </head>
</html>
```

**Guilherme:** Vamos dar um título para a página entre as _tags_ do `title`?

**Rafaella:** Vamos. Pode ser "Portfolio"?

**Guilherme:** Pode.

```xml
<!DOCTYPE html>
<html>
    <head>
        <title>Portfolio</title>
    </head>
</html>
```

**Rafaella:** Salvaremos o arquivo e abriremos no navegador. Para abri-lo, acessaremos o explorador de arquivos do computador, acessaremos o local em que salvamos a pasta do projeto. Abriremos essa pasta e clicaremos duas vezes no arquivo que estamos escrevendo: o `index.html`. Podemos abri-lo com qualquer navegador disponível. Neste caso, abriremos no mesmo navegador que estamos usando.

**Guilherme:** Neste momento o navegador abrirá uma tela em branco. No corpo não tem nada, mas a metainformação que passamos no `<head>` deu um nome para a nossa aba: a aba se chama Portfolio. Ou seja, criamos um arquivo HTML e demos a ele um `title` denominado Portfolio.

A seguir, abordaremos de fato o **_conteúdo_** que queremos criar.

---

## A importância da documentação

**O que é:**

A [documentação](https://www.w3schools.com/html/html_intro.asp) é um guia que toda pessoa desenvolvedora deve levar a sério no dia a dia, é através dela que aprendemos como funcionam as linguagens de programação e também ferramentas e bibliotecas no mundo da tecnologia.

**Sua importância:**

A documentação é muito importante no aprendizado e no desenvolvimento de aplicações. Afinal quem melhor que a pessoa que criou a ferramenta para nos orientar sobre as suas funcionalidades não é mesmo?

**Quando devemos utilizar:**

Devemos ler a documentação sempre que precisamos saber a estrutura de um método, ou quando queremos saber algum comando ou recurso de uma biblioteca, ou até mesmo quando esquecemos certa funcionalidade e precisamos relembrar.

**Outra forma de ajuda:**

Existem também as comunidades de tecnologia e programação que são bem úteis para tirarmos nossas dúvidas e aprendermos mais, como por exemplo a [Stackoverflow](https://stackoverflow.com/) que é uma das maiores comunidades de ajuda sobre programação e tecnologia atualmente, é uma comunidade onde você vai encontrar dúvidas sobre quase todas as linguagens de programação entre outras ferramentas, super recomendável acessá-la.

Aqui na Alura tem um artigo muito legal sobre comunidades, você pode conferir acessando [Comunidades Front-End](https://www.alura.com.br/artigos/principais-comunidades-front-end). Você pode acessar também a documentação do HTML que foi apresentada na aula através do link da w3schools. A [w3schools](https://www.w3schools.com/html/html_intro.asp) também é uma ótima opção para quem precisa aprender algum método novo ou consultar exemplos sobre determinada linguagem, é um site bem completo e de fácil compreensão.

---

**Rafaela:** Temos uma página Web mais bonita, com todos os nossos elementos. Porém, ainda podemos brincar com esse código.

**Guilherme:** Exatamente. Quando seguimos a documentação de uma linguagem, sentimos uma certa desconfiança: será que se tirarmos uma propriedade indicada, conseguiremos ter o mesmo resultado?

Vamos alimentar a nossa curiosidade e mexer no código, tirando e colocando elementos de volta no lugar. Por exemplo, vamos retirar a primeira linha: o `<!DOCTYPE html>`.

**Rafaela:** Vamos. Esta linha foi indicada como importante para indicar a versão do HTML.

**Guilherme:** Isso. Vamos retirá-la e salvar o código.

```xml
<html>
    <head>
        <title>Portfolio</title>
    </head>
    <body>
        <h1>Isso é um título</h1>
        <p>Isso é um parágrafo</p>
        <img src="html.png" alt="Logo do HTML 5">
    </body>
</html>
```

**Rafaela:** Retornaremos ao navegador e atualizaremos a nossa página. Veremos que nada foi alterado. Aparentemente tudo está funcionando.

**Guilherme:** Aparentemente, contudo, houve sim uma alteração.

Existe uma forma de verificar o código HTML e CSS de qualquer página da internet. Para isso, na tela do navegador, clicaremos com o botão direito e selecionaremos a opção "Inspecionar". Neste instante, será aberta uma aba à direita da página Web, onde existe uma barra de menus superior. Nela, selecionaremos o menu "Elements". No interior deste menu será exibido o código-fonte da nossa página `index.html`.

Vamos acessar esse código-fonte e perceber que, quando passamos o cursor por cima de uma _tag_, o navegador realça o elemento correspondente diretamente na página Web. Vamos conferir se todos os elementos que codamos estão na página: `<html>`, `<head>`, `<title>`, `<body>`, `<h1>`, `<p>` e `<img>`.

Aparentemente, está tudo igual. Ou seja, a retirada do `<!DOCTYPE html>` não mudou a parte visual da nossa página. Contudo, **_houve uma alteração na forma como o navegador enxerga essa página_**. Podemos ver a alteração dentro da própria aba "Inspecionar", selecionando o ícone de balão de comentário, localizado à direita da barra de menus superior. Este ícone aponta as _issues_ da página. Após a seleção, será aberta uma aba secundária denominada "_Issues_", na parte inferior da aba "Inspecionar", a qual exibirá a seguinte mensagem:

> _Page layout may be unexpected due to Quirks Mode_

Podemos traduzi-la como "O layout da página pode ser inesperado devido ao Modo Quirks". Ou seja, a página está em "modo peculiaridades". Não sabemos o que isso significa. Vamos clicar nesta mensagem para entender mais a fundo.

Abaixo da mensagem será exibida uma explicação mais detalhada do problema apontado,a qual apresentaremos uma versão resumida e traduzida:

> Um ou mais documentos desta página foram abertos em um modo diferente do esperado. O Modo _Quirks_ existe por razões históricas. Caso ele tenha sido acionado de forma não intencional, [adicione o `<!DOCTYPE html>`](https://developer.chrome.com/pt/docs/lighthouse/best-practices/doctype/) para renderizá-la sem o Modo _Quirks_.

**_Afinal, o que é o Modo Quirks?_** Vamos acessar o link disponibilizado acima, o qual nos direcionará para uma nova página. Na parte superior dela veremos o título "A página não tem o doctype HTML, acionando assim o Modo Quirks". Esta página possui várias informações e links sobre o Modo Quirk, o modo Standards, códigos-fonte, etc. Recomendamos que você a leia posteriormente.

Vamos resumir o problema: antigamente existiam dois grandes navegadores, o NetScape e o Internet Explorer. Quando codávamos, precisávamos informar para qual navegador a página estava sendo construída. Hoje em dia isso não é mais necessário, a não ser que seja algo intencional — como em casos de projetos antigos.

Na [página sobre Quirks Mode e Standards Mode](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Quirks_Mode_and_Standards_Mode) existe a seção "Como os navegadores determinam qual modo usar?", onde há uma explicação sobre a questão da determinação de modos. Nela veremos que, para informarmos ao navegador que utilizaremos o HTML5, precisamos adicionar o `<!DOCTYPE html>`.

**Rafaela:** Atualmente, todos os navegadores sabem utilizar o HTML5.

**Guilherme:** Isso mesmo. Vamos sair do modo peculiaridades.

**Rafaela:** Vamos fechar as abas de explicação e a aba "Inspecionar". Em seguida retornaremos ao VS Code.

**Guilherme:** Para sair desse modo, pressionaremos "Ctrl + Z" para recuperar o DOCTYPE que havíamos deletado.

```xml
<!DOCTYPE html>
<html>
    <head>
        <title>Portfolio</title>
    </head>
    <body>
        <h1>Isso é um título</h1>
        <p>Isso é um parágrafo</p>
        <img src="html.png" alt="Logo do HTML 5">
    </body>
</html>
```

Salvaremos esse código e voltaremos ao nosso projeto aberto no navegador. Nele pressionaremos "F5" para atualizar a página e abriremos novamente a aba "Inspecionar". Veremos que, à direita da barra de menus, não existe mais o ícone de _issues_.

Existe um ponto que incomoda em nossa página: **_a necessidade de atualizá-la sempre que alteramos o código_**.

**Rafaela:** Vamos adicionar uma **extensão** ao nosso editor de código para que ocorram atualizações automáticas na nossa página a cada salvamento. Acessaremos a coluna lateral esquerda do nosso VS Code, onde selecionaremos o ícone "_Extensions_" ("Extensões"). Podemos acessá-lo também por meio do atalho "Ctrl + Shift + X".

Neste momento, o explorador de arquivos será substituído por um campo de busca. Nele digitaremos "_live server_" e faremos a busca. Nos resultados abaixo do campo, buscaremos a opção "_Live Server_", a qual possui milhões de _downloads_.

**Guilherme:** Muitas pessoas a utilizam.

**Rafaela:** Nós, inclusive. Após a seleção, essa extensão será aberta na tela principal do VS Code, onde clicaremos no botão "_Install_". Após o término da instalação, Ela será habilitada automaticamente. Caso contrário, basta clicar no botão "_Enable_". Em seguida fecharemos a aba dessa extensão.

Existem extensões para milhares de tarefas, inclusive para embelezar sintaxes de linguagens específicas. Podemos explorá-las e utilizá-las sempre que quisermos.

**Guilherme:** Como a extensão funciona?

**Rafaela:** Agora temos um botão na barra inferior do VS Code denominado "_Go Live_". Como o arquivo HTML selecionado, clicaremos neste botão. Uma aba de Alerta de Segurança será aberta pelo nosso sistema, na qual selecionaremos a opção "Permitir acesso". Neste momento será aberta uma aba com a nossa página HTML no nosso navegador.

**Guilherme:** Vamos manter as duas abas abertas. Veremos que ambas estão rodando de locais diferentes: a antiga está rodando no local do arquivo, enquanto a nova (com _live server_ ativo) exibe a URL com um número constituído de 10 dígitos.

Retornando ao VS Code, alteraremos o parágrafo adicionando "interessante" ao final da frase.

```css
        <p>Isso é um parágrafo interessante</p>
```

Salvaremos esse código e voltaremos ao navegador. Na aba nova, veremos a nossa alteração.

**Rafaela:** Na aba antiga, a mudança só aparecerá se atualizarmos a página.

**Guilherme:** A principal vantagem do _live server_ é não precisar atualizar a página a todo momento.

**Rafaela:** O único passo necessário é salvar o arquivo no editor.