---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/toques-finais-e-nova-pagina/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# toques finais e nova página

## criado em: 
-  03-04-2023 - 11:00

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/HTML e CSS 3\|HTML e CSS 3]]
- [[ aplicando variáveis no css\| aplicando variáveis no css]]
- tags: #ANELO 
- Fontes & Links: 

---
## Nessa aula, você aprendeu como:

-   Fazer a estilização do `header` do portfólio;
-   Criar a nova página HTML “Sobre mim”;
-   Desenvolver a navegação entre as páginas “Home” e “Sobre mim”.

---



**Rafaella:** Já criamos nosso cabeçalho com HTML, mas ainda precisamos estilizá-lo.

Abrindo o arquivo `style.css` no VSCode, inseriremos as classes que já criamos no `index.html`, mas sempre deveremos colocar no momento em que as _tags_ vão aparecendo.

Vamos deslocar o `.titulo-destaque` para depois de `.apresentacao__conteudo__titulo` porque possui a _tag_ `<strong>` que é utilizada logo depois do `<h1>`.

Começaremos a estilização do escrito para depois posicionarmos os elementos, então a classe `"cabecalho__menu__link"` na âncora `<a>` de `index.html` será copiada e colada após o `body` em `style.css`.

Abriremos as chaves de `.cabecalho__menu__link` e dentro colocaremos as propriedades de cor, fonte e tamanho obtidas do projeto do Figma.

**Guilherme:** Primeiro, a `font-family:` é `'Montserrat', sans-serif`, depois o `font-size:` terá o valor de `24px` e, por fim, seu peso `font-weight:` será de `600`.

**Rafaella:** Também precisaremos trocar a cor do texto de cabeçalho para azul claro, e já temos este valor também. Então `color:` será `#22D4FD`. Salvaremos e analisaremos o resultado no navegador.

```css
//código omitido

body {
    /*height: 100vh */
    box-sizing: border-box;
    background-color: #000000;
    color: #F6F6F6;
}

.cabecalho__menu__link {
    font-family: 'Montserrat', sans-serif;
    font-size: 24px;
    font-weight: 600;
    color: #22D4FD;
}

//código omitido
```

**Rafaella:** Com isso, teremos nossos elementos estilizados.

**Guilherme:** Agora precisaremos trabalhar no posicionamento deles.

**Rafaella:** Exatamente, e poderemos usar o cabeçalho para estabelecer a posição de cima para baixo com espaçamento lateral usando `padding:`.

Pegaremos a classe `"cabecalho"` do `<header>` em `index.html` que agrupará toda a barra de navegação que contém as duas _tags_ âncoras para podermos estilizá-las.

Copiaremos o nome dessa `class` e a adicionaremos acima de `.cabecalho__menu__link`, pois aparece antes.

Dentro das chaves, colocaremos o `padding:` para espaçarmos as duas âncoras, e queremos apenas na parte superior e de um lado só. Já aprendemos uma forma de escrevermos dois valores para trabalharmos no sentido vertical e horizontal.

Porém, agora precisaremos espaçar apenas dois lados, e não no sentido vertical e horizontal, e para isso poderemos inserir quatro valores para o `padding:`, o qual possui uma ordem específica.

Analisando a [documentação do `padding:` aqui](https://www.w3schools.com/cssref/pr_padding.php), encontraremos a parte "Se a propriedade _padding_ tiver quatro valores:", que é justamente o que queremos.

O primeiro diz respeito à parte superior do conteúdo.

**Guilherme:** Então, no `padding:` de `.cabecalho`, colocaremos o valor `2%` em porcentagem que é melhor, pois se fixarmos em pixels, pode ser que sofra distorções na tela dependendo do dispositivo que acessará a aplicação.

```css
//código omitido

body {
    /*height: 100vh */
    box-sizing: border-box;
    background-color: #000000;
    color: #F6F6F6;
}

.cabecalho {
    padding: 2%;
}

//código omitido
```

**Rafaella:** Feito isso, notaremos que a porcentagem foi aplicada a todos os quatro lados do conteúdo, pois só colocamos um valor apenas.

De volta à documentação, o espaçamento do lado direito será o segundo valor, que neste caso será `0%`. Já o terceiro valor diz respeito ao espaçamento inferior que também será `0%`. Por fim, o quarto valor do preenchimento do lado esquerdo terá `10%`.

Salvaremos e veremos o resultado no navegador.

```less
//código omitido

.cabecalho {
    padding: 2% 0% 0% 10%;
}

//código omitido
```

**Rafaella:** Com isso, repararemos que o espaçamento já está bem diferente de antes.

**Guilherme:** Mas ainda não está na mesma linha.

**Rafaella:** Isso aconteceu porque colocamos um `padding:` horizontal de `15%` como segundo valor no `main` de `.apresentacao` do `style.css`.

Então, para ficar mais parecido com o Figma, colocaremos o valor de `15%` ao invés de `10%` no `padding:` do `.cabecalho`.

```less
//código omitido

.cabecalho {
    padding: 2% 0% 0% 15%;
}

//código omitido
```

**Rafaella:** Feito isso, o texto já ficará alinhado. Agora, precisaremos afastar um pouco os conteúdos das duas _tags_ âncoras.

No arquivo `index.html`, iremos para a `<nav>` e usaremos o FlexBox, lembrando que sempre jogaremos o `display: flex` no elemento _container_, no elemento-pai.

Copiaremos a classe `"cabecalho__menu"` e colaremos após o `.cabecalho` em `style.css`. Dentro, criaremos a propriedade `display: flex` para inicializarmos o FlexBox.

**Guilherme:** Vamos ver qual é essa distância de `gap:` no Figma.

**Rafaella:** Descobriremos que é de `80px`.

```css
//código omitido

.cabecalho {
    padding: 2% 0% 0% 15%;
}

.cabecalho__menu {
    display: flex;
    gap: 80px;
}

//código omitido
```

**Rafaella:** Feito isso, teremos o espaçamento entre os textos "Home" e "Sobre mim" que queríamos.

Então terminamos nosso cabeçalho, porém ainda não está funcional, ou seja, quando clicamos em algum dos dois links, não nos direcionamos para as respectivas páginas.

**Guilherme:** Ainda tem um detalhe, pois seria interessante subir o bloco de texto que inicia com "Eleve seu negócio digital...".

**Rafaella:** Podemos subir para que fique mais próximo do cabeçalho.

De volta ao `padding:` de `.apresentacao` em `style.css`, substituiremos o valor `8%` por `5%`.

```css
//código omitido

.cabecalho__menu__link {
    font-family: 'Montserrat', sans-serif;
    font-size: 24px;
    font-weight: 600;
    color: #22D4FD;
}

.apresentacao {
    padding: 5% 15%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

//código omitido
```

**Rafaella:** Assim ficou bem melhor e mais parecido com o projeto final no Figma.

**Guilherme:** Então já temos a página inteira feita.

**Rafaella:** Exato, mas ainda não está funcional, porque ao clicarmos ainda não vamos para outra página.

**Guilherme:** O desafio será tornar esse menu funcional para nos direcionarmos à página de "Sobre mim" para depois a desenvolvermos.

---

**Rafaella:** Criaremos uma nova página para deixarmos o menu do cabeçalho funcional, em que poderemos clicar para nos redirecionarmos para outras páginas.

**Guilherme:** Abriremos o VSCode e veremos que, na aba lateral esquerda de "Explorer", teremos a arquitetura das pastas do portfólio em que `"assets"` contém todas as imagens. Ainda teremos os dois arquivos: `index.html` e `styles.css`.

Como criaremos uma nova página, da forma como nosso código está organizado, pode ser que sua manutenção e edição fiquem mais complicadas conforme cresce o número de telas do projeto.

Clicando com o botão direito do mouse sobre a aba "Explorer", escolheremos "New Folder..." ou "Nova pasta..." e nomearemos como "styles" porque é o padrão.

Em seguida, deslocaremos o arquivo `styles.css` para dentro da nova pasta. A partir de agora, qualquer documento `.css` que criarmos deverá ficar nela.

Depois, abriremos a página no navegador e não teremos mais a estilização dos elementos que aplicamos.

Isso aconteceu porque alteramos o lugar do documento de estilos, fazendo com que o `index.html` não o encontrasse mais através do `href` igual a `"styles.css"`.

**Rafaella:** Então precisaremos alterar o endereço que estamos usando, e bastará substituirmos por `"./styles/styles.css"` para indicarmos o caminho de dentro da pasta `"styles"`.

Desta forma, a estilização voltará a ser aplicada na página no navegador.

**Guilherme:** Todos os arquivos relacionados aos estilos dos elementos serão criados na pasta `"styles"`, todas as imagens estarão em `"assets"` e todos os arquivos `.html` ficarão fora na raiz da aplicação.

Clicando com o botão direito na área da aba lateral de pastas, e escolheremos "New File..." ou "Novo Arquivo...".

Geralmente, a página de "Sobre mim" é nomeada como `about.html`, que é "sobre" em inglês.

Neste novo arquivo, usaremos o atalho "ponto de exclamação + Enter" para escrevermos a estrutura básica do HTML automaticamente, que é bastante comum, mas precisaremos alterar alguns detalhes.

**Rafaella:** Também apertaremos as teclas "Alt + Z" para quebrarmos a linha e conseguirmos exibir todo o texto sem cortes da tela.

**Guilherme:** Na segunda linha, mudaremos o idioma oficial de inglês para protuguês brasileiro substituindo lang igual a "en" por "pt-br", e o título da nossa aba será “Sobre mim” dentro da tag `<title>` do `<head>`. Também adicionaremos um `<h1>` dentro de `<body>` contendo o texto “Sobre mim”.

Por enquanto não trabalharemos muito nos elementos desta tela, pois queremos apenas conseguir clicar no link "Sobre mim" do cabeçalho da página principal e nos redirecionar para a nova que criamos.

```xml
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sobre mim</title>
</head>
<body>
    <h1>Sobre mim</h1>
</body>
</html>
```

**Guilherme:** Feito isso, voltaremos ao `index.html` onde temos o menu de navegação, e precisaremos fazer com que nos redirecione através do link `"Sobre mim"`.

Sempre utilizamos o `href` para navegar até uma outra pasta, ou ainda, no caso de imagens, há o `src` que significa "source" ou "fonte" em português.

**Rafaella:** Para navegarmos até outra página com um link, também utilizaremos o `href`.

**Guilherme:** Outro ponto de atenção é que, onde temos a classe de `<a>`, escreveremos o `href` logo após seu nome e antes de fechar a navegação em `>`.

No caso do link `"Home"`, sempre iremos voltar para a página inicial quando clicarmos, que é o `"index.html"`.

**Rafaella:** não colocaremos o `./` antes do nome do arquivo porque já estamos na mesma pasta que ele.

**Guilherme:** Faremos a mesma coisa para a segunda tag âncora, em que `href` será igual a `"about.html"`. Salvaremos e voltaremos à página no navegador.

```xml
<!DOCTYPE html>
<html lang="pt-br">

//código omitido

<body>
    <header class="cabecalho">
        <nav class="cabecalho__menu">
            <a class="cabecalho__menu__link" href="index.html">Home</a>
            <a class="cabecalho__menu__link" href="about.html">Sobre mim</a>
        </nav>
    </header>

//código omitido

</body>
</html>
```

**Guilherme:** Repararemos que os dois links estão sublinhados depois que colocamos os dois `href`s.

**Rafaella:** Mas não queremos que fiquem sublinhados, então vamos retirar isso no arquivo de estilização.

**Guilherme:** Para isso, em `styles.css`, iremos ao seletor `.cabecalho__menu__link` e inseriremos a propriedade `text-decoration: none` ao final do bloco dentro das chaves.

```css
//código omitido

.cabecalho__menu__link {
    font-family: 'Montserrat', sans-serif;
    font-size: 24px;
    font-weight: 600;
    color: #22D4FD;
    text-decoration: none;
}

//código omitido
```

**Rafaella:** Voltando à página no navegador, teremos retirado os sublinhados.

**Guilherme:** Se clicarmos em "Home", iremos apenas recarregar porque já estaremos na página principal, mas se clicarmos em "Sobre mim", iremos à nova tela que criamos.

---

**Rafaella:** Nesta aula, iremos desenvolver a página "Sobre mim" que por enquanto só tem este texto no `<h1>` de `<body>` no `about.html`, que inclusive poderemos apagar pois não o utilizaremos mais.

Vamos lembrar da estrutura inicial mais semântica que sempre utilizamos no HTML.

**Guilherme:** Dentro de `<body>`, usaremos o `<header>`, seguido de `<main>` que é o conteúdo principal da página, e o `<footer>` depois.

Porém, se observarmos a tela de "Sobre mim" no Figma, notaremos que o cabeçalho e o rodapé são exatamente iguais aos da página inicial.

Então poderemos copiar este código de `index.html` com "Ctrl + C" e colar com "Ctrl + V" no `about.html`.

**Rafaella:** No documento da página inicial, usamos as classes `"cabecalho"` em `<header>` e `"cabecalho__menu"` em `<nav>`, e poderemos copiar este bloco para depois estilizarmos.

Dentro do `<body>` que acabamos de colocar em `about.html`, colaremos todo o bloco de `<header>` copiado do `index.html`.

Faremos a mesma coisa com o `<footer>` de classe `"rodape"` do `index.html`, colando-o em `about.html`.

```xml
<!DOCTYPE html>
<html lang="pt-br">

//código omitido

<body>
    <header class="cabecalho">
        <nav class="cabecalho__menu">
            <a class="cabecalho__menu__link" href="index.html">Home</a>
            <a class="cabecalho__menu__link" href="about.html">Sobre mim</a>
        </nav>
    </header>
    <main></main>
    <footer class="rodape">
        <p>Desenvolvido por Alura.</p>
    </footer>
</body>
</html>
```

**Rafaella:** Com isso, já teremos o `<header>` e o `<footer>` da página "Sobre mim" igual aos da página inicial.

Agora precisaremos completar o `<main>`.

**Guilherme:** Vamos salvar e abrir o navegador para analisarmos o resultado.

Por enquanto há apenas os textos do cabeçalho sublinhados em azul porque são clicáveis, e a frase "Desenvolvido por Alura." do rodapé logo abaixo, tudo no canto superior esquerdo do fundo em branco.

Se clicarmos em "Home", nos redirecionaremos para a página inicial porque os links já estão definidos em `<a>`.

**Rafaella:** Ainda não temos os estilos porque não importamos o CSS.

**Guilherme:** Deveremos criar um novo arquivo `style.css` para essa página nova, ou manteremos o que já temos?

**Rafaella:** conseguiremos trazer este documento de estilos para a "Sobre mim", pois estamos utilizando exatamente as mesmas classes da mesma forma.

Por exemplo, se estivéssemos com um menu de cores e formatos diferentes, teríamos que utilizar outras classes ou criar mais arquivos `.css`.

Existem diversas possibilidades quando estamos em ambiente de desenvolvimento e criamos vários documentos para cada página para nos organizarmos, principalmente em grandes projetos.

Porém, na prática, no momento de colocarmos o projeto no ar, o ideal para a performance da nossa página ser boa, é termos o menor número de arquivos `.css` possível.

Então conseguiremos reutilizar nosso arquivo `style.css` em nosso projeto porque é bastante simples, e de fato usamos a mesma estilização.

Portanto, importaremos este documento no código da nova página.

**Guilherme:** Uma dica importante é, se formos em `<title>` com `Sobre mim` no `about.html`, e abaixo escrevermos apenas “link: css” para apertarmos a tecla "Enter" depois, aparecerá a linha de código `<link>` completa.

```xml
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sobre mim</title>
    <link rel="stylesheet" href="styles.css">
</head>

//código omitido

</html>
```

**Rafaella:** O problema é que temos `"style.css"` em `href`, mas havíamos criado uma pasta, então precisaremos corrigir para `"./styles/style.css"`.

Se salvarmos e voltarmos ao navegador, encontraremos os links do cabeçalho e o texto do rodapé já com os estilos corretos.

**Guilherme:** Aparecem ainda muito juntos.

**Rafaella:** É porque ainda não temos nada no `<main>` do `about.html`, e a seguir iremos desenvolver o corpo da página.

---

