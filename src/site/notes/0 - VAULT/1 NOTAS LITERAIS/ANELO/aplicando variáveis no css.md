---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/aplicando-variaveis-no-css/","tags":["css","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# aplicando variáveis no css

## criado em: 
-  03-04-2023 - 11:46

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/HTML e CSS 3\|HTML e CSS 3]] 
- tags: #css #ANELO
- Fontes & Links: https://cursos.alura.com.br/course/html-css-cabecalho-footer-variaveis-css

---
## Nessa aula, você aprendeu como:

-   Adicionar conteúdo a uma nova página;
-   O que são variáveis CSS;
-   Como customizar o projeto aplicando variáveis CSS.

---

**Rafaella:** Já temos nosso cabeçalho e nosso rodapé. Falta adicionarmos o conteúdo principal da página "Sobre mim". Podemos ver no Figma quais elementos existem dentro do nosso `main`:

-   o título "Sobre mim";
-   abaixo dele, dois parágrafos;
-   à direita destes, a mesma imagem que usamos na página inicial.

Retornaremos ao VS Code e acessaremos o arquivo `about.html` para inserir estes elementos. Buscaremos o nosso `<main>` vazio e nele criaremos uma `<section>` para armazenar todos os elementos da página. Abaixo da `<section>` adicionaremos uma `<img>`.

Lembrando que já realizamos esse procedimento no nosso índice. A `<section>` será o elemento visualizado à esquerda da página, enquanto a `<img>` ficará à direita.

```xml
// Código omitido

        </nav>
    </header>

    <main>
        <section>

        </section>
        <img>
    </main>

    <footer class="rodape">
        <p>Desenvolvido por Alura.</p>
    </footer>
</body>
</html>
```

O que temos dentro dessa `<section>`?

**Guilherme:** Temos o `<h1>` com o texto "Sobre mim", e dois `<p>`s.

> **Dica:** Para adicionarmos os dois parágrafos de uma vez, iremos até a linha vazia abaixo do `<h1>` e digitaremos o atalho `p*2`, seguido do "Enter".

```xml
// Código omitido

        </nav>
    </header>

    <main>
        <section>
            <h1>Sobre mim</h1>
            <p></p>
            <p></p>
        </section>
        <img>
    </main>

    <footer class="rodape">
        <p>Desenvolvido por Alura.</p>
    </footer>
</body>
</html>
```

**Rafaella:** Voltaremos ao Figma, onde copiaremos o "Lorem ipsum" dos dois parágrafos, um por vez. Voltaremos ao nosso código e colaremos esses conteúdos no interior das suas respectivas _tags_.

```xml
// Código omitido

        </nav>
    </header>

    <main>
        <section>
            <h1>Sobre mim</h1>
            <p>At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga.</p>
            <p>Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus. Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint et molestiae non recusandae. Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias consequatur aut perferendis doloribus asperiores ipsum delis forum birol parela maxime infena. Excepteur sint occaecat cupidatat non.</p>
        </section>
        <img>
    </main>

    <footer class="rodape">
        <p>Desenvolvido por Alura.</p>
    </footer>
</body>
</html>
```

**Guilherme:** Agora precisamos da imagem. Ela possui as mesmas propriedades da imagem anterior. Podemos copiar o conteúdo do `index.html` e colá-lo no `about.html`. O código a ser copiado está disponível abaixo.

```xml
<img src=".assets/imagem.png" alt="Foto da Joana Santos programando">
```

O resultado será este:

```xml
// Código omitido

        </nav>
    </header>

    <main>
        <section>
            <h1>Sobre mim</h1>
            <p>At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga.</p>
            <p>Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus. Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint et molestiae non recusandae. Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias consequatur aut perferendis doloribus asperiores ipsum delis forum birol parela maxime infena. Excepteur sint occaecat cupidatat non.</p>
        </section>
        <img src=".assets/imagem.png" alt="Foto da Joana Santos programando">
    </main>

    <footer class="rodape">
        <p>Desenvolvido por Alura.</p>
    </footer>
</body>
</html>
```

**Rafaella:** Salvaremos o nosso código.

**Guilherme:** Vamos ver como ficou no navegador. Abaixo do cabeçalho, temos os três textos e a imagem no canto esquerdo da página, dispostos na vertical. No topo temos o título "Sobre mim". Abaixo dele temos o primeiro parágrafo, e logo abaixo deste temos o segundo parágrafo. Por fim, abaixo dos textos, temos a imagem.

**Rafaella:** Por que as nossas configurações de CSS não estão funcionando no `main`?

**Guilherme:** **_Porque não atribuímos classes a elas_**. Vamos adicionar as seguintes classes:

-   no `<main>`, a `class="apresentacao"`;
-   na `<section>`, a `class="apresentacao__conteudo"`;
-   no `<h1>`, a `class="apresentacao__conteudo__titulo"`;
-   nos dois `<p>`s, a `class="apresentacao__conteudo__texto"`.

> **Dica 1:** Podemos copiar os nomes das classes diretamente do `index.html`. Esse procedimento é muito comum no início da criação de páginas Web.

> **Dica 2:** Para adicionar a mesma classe em dois locais de uma vez — como no caso dos nossos dois parágrafos —, basta clicar no primeiro local, segurar o botão "Alt" e clicar nos próximos locais em que deseja escrever. Desta forma, **_todos os locais selecionados serão editados simultaneamente_**.

```xml
// Código omitido

        </nav>
    </header>

    <main class="apresentacao">
        <section class="apresentacao__conteudo>
            <h1 class="apresentacao__conteudo__titulo">Sobre mim</h1>
            <p>At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga.</p>
            <p>Et harum quidem rerum facilis est et expedita distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est, omnis dolor repellendus. Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint et molestiae non recusandae. Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias consequatur aut perferendis doloribus asperiores ipsum delis forum birol parela maxime infena. Excepteur sint occaecat cupidatat non.</p>
        </section>
        <img src=".assets/imagem.png" alt="Foto da Joana Santos programando">
    </main>

    <footer class="rodape">
        <p>Desenvolvido por Alura.</p>
    </footer>
</body>
</html>
```

**Rafaella:** Salvaremos nosso código e veremos o resultado no navegador. Abaixo do cabeçalho, agora temos o conteúdo centralizado na tela e dividido em dois blocos: o da esquerda possui o título, seguido abaixo pelos textos, enquanto o bloco da direita possui somente a imagem.

![Tela "Sobre mim" no navegador. No topo da tela existe um cabeçalho na cor ciano com dois textos: "Home" e "Sobre mim". Abaixo dele, existem dois blocos de conteúdo, lado a lado, centralizados sobre fundo preto. O bloco esquerdo possui um texto que se divide em duas partes: um título e dois parágrafos. O título apresenta o texto em negrito "Sobre mim" na cor branca. Os parágrafos são na cor branca, e exibem um texto "Lorem ipsum". Já o bloco direito se constitui de uma fotografia em preto e branco representando Joana Santos, uma mulher desenvolvedora, sentada em frente a um notebook aberto. A fotografia também conta com um desenho em ciano de uma linha circulando Joana e seu notebook três vezes e terminando em uma estrela. Abaixo dos dois blocos, temos um rodapé constituído de uma faixa ciano que atravessa horizontalmente a parte inferior da tela, do canto direito ao canto esquerdo. Dentro dele há o texto "Desenvolvido por Alura", na cor preta.](https://cdn1.gnarususercontent.com.br/1/1319057/627c3c38-c71b-45ba-9dce-5e8f395cc2be.png)

---

## variáveis css

**Rafaella:** O nosso projeto está sensacional! Conseguimos:

-   navegar entre as páginas;
-   acessar o "Sobre mim";
-   visualizar o rodapé, o cabeçalho e todos os conteúdos da tela;
-   voltar para o "Home" e
-   visualizar o efeito _Hover_ quando passamos o mouse pelos botões.

O projeto está visualmente incrível, contudo existem alguns detalhes que podemos alterar em relação ao nosso **_código_**.

**Guilherme:** Vamos analizar **_as cores_** do nosso projeto. Temos três cores principais:

-   a cor preta de fundo `000000`, que é a cor principal;
-   o branco `F6F6F6`, utilizado em vários elementos e
-   o azul ciano `22D4FD`, uma cor terciária que utilizamos para dar destaque.

Utilizamos essas cores diversas vezes no nosso CSS. Vamos abrir o arquivo `style.css` por meio do VS Code. Pressionaremos "Ctrl + F" e pesquisaremos a cor terciária, digitando "22D4FD" no campo de pesquisa. Constataremos que essa cor foi utilizada **_quatro vezes_** ao longo do projeto. Pesquisaremos em seguida a cor do fundo, digitando "000000" no campo de pesquisa. Perceberemos que ela foi utilizada **_duas vezes_**.

Ou seja, somando somente as duas cores, repetimos o nosso código **_seis vezes_**. Na prática, repetimos uma **_propriedade sensível_** oito vezes. Isso significa que, caso precisarmos alterar alguma das três cores principais do nosso projeto, teríamos que alterá-la em oito partes diferentes.

**Rafaella:** Esse processo de mudança de cor é muito comum. Muitas empresas decidem alterar as suas identidades visuais em algum ponto de sua trajetória.

**Guilherme:** Como poderemos reutilizar um único código de cor em partes diferentes da nossa aplicação?

**Rafaella:** Utilizaremos **_variáveis no CSS_**. Se você conhece alguma outra linguagem de programação, deve saber que elas são muito utilizadas. As variáveis são **_endereços na nossa memória_** reservados para armazenar um valor. Elas precisam ser nomeadas.

É possível criar, por exemplo, uma variável chamada `azul-claro` e armazenar nela a nossa cor, informando o valor hexadecimal `#22D4FD`. Com isso, podemos utilizar somente a variável ao invés de declarar o valor da cor diretamente em todas as partes do código. Além disso, poderemos alterar este valor sempre que precisarmos.

**Guilherme:** Com esse processo, podemos realizar alterações na cor do nosso projeto recorrendo a um único local, o qual enviará a alteração para todos os outros locais em que for inserido. Vamos entender as variáveis acessando a documentação.

**Rafaella:** Buscaremos no Google "variables css" (ou "variáveis no css"). No resultado da pesquisa, selecionaremos o link que nos guiará para a [página do Developer Mozilla sobre variáveis do CSS, em português](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Using_CSS_custom_properties).

**Guilherme:** Selecionamos o Developer Mozilla pois nele temos um exemplo prático. Na seção "Uso básico", somos informados da possibilidade de **_criar variáveis para um escopo global ou para um escopo local_**. Voltaremos ao VS Code para demonstrar os dois processos.

Começaremos entendendo a variável de **_escopo local_**. Ela consiste em uma variável que poderá ser utilizada diversas vezes, mas que funcionará apenas em um bloco de código definido — como por exemplo, o `body {}` do nosso arquivo `style.css`.

**Rafaella:** Não temos nenhum caso desse em nosso código.

**Guilherme:** Não temos esse caso nem no código nem no nosso projeto. Portanto, faz mais sentido criarmos para o **_escopo global_**. Essa técnica consiste em definir as nossas variáveis dentro de um local por meio do qual possamos utilizá-las em vários blocos diferentes, seja o `body`, o `header`, ou outro qualquer.

**Rafaella:** Podemos encontrar esta técnica no segundo exemplo que nos é dado no site Developer Mozilla. A técnica consiste em utilizar a pseudoclasse `root` para que a variável possa ser aplicada globalmente no documento HTML. Podemos consultar o exemplo mencionado abaixo:

```css
:root {
    --main-bg-color: brown;
}
```

Neste exemplo declaramos uma variável dentro das chaves do `root`, utilizando a sintaxe `--nome: valor`. O `brown` ilustra um procedimento que já realizamos anteriormente. No lugar do nome da cor, adicionaremos o seu valor hexadecimal.

Retornando ao VS Code, ainda no interior do arquivo `style.css`, adicionaremos na linha 3, acima de todos os blocos de código, a pseudoclasse `:root {}` como se ela fosse um seletor.

**Guilherme:** Um seletor para utilizarmos ao longo de todo o nosso documento, ou seja, de forma global.

```css
@import url('https://fonts.googleapis.com/css2?family=Krona+One&family=Montserrat&display=swap');

:root {

}

* {
        margin: 0;
        padding: 0;
}
```

No interior de suas chaves, criaremos nomes para as três variáveis de cor:

-   a cor principal se chamará `--cor-primaria`;
-   a cor secundária se chamará `--cor-secundaria` e
-   a cor terciária ou de destaque, chamaremos de `--cor-terciaria`.

Para definir a `--cor-primaria`, utilizaremos `: #000000`, seguido de ponto e vírgula. Faremos o mesmo para as outras cores, alterando o valor hexadecimal da `--cor-secundaria` para `#F6F6F6`, enquanto o valor da `--cor-terciaria` será `#22D4FD`.

```css
:root {
    --cor-primaria: #000000;
    --cor-secundaria: #F6F6F6;
    --cor-terciaria: #22D4FD;
}
```

**Rafaella:** Por enquanto, nada mudou no projeto, pois **_apenas declaramos essas variáveis._**

**Guilherme:** Exatamente. Nós criamos um local onde definimos que temos três cores, e atribuímos um valor para cada uma delas. Nosso próximo desafio será **_utilizar esses elementos_** no nosso projeto.

## Um armário cheio de gavetas!

Imagine que você trabalhe em uma sala de arquivos, que possui um armário muito grande e cheio de gavetas. Todos os dias, pessoas trazem seus objetos para que você guarde em uma gaveta para eles e para isso, te entregam uma etiqueta com um nome que será colado nessa gaveta que armazenará o objeto da pessoa.

Ana te entregou uma caneta e uma etiqueta com o nome: `canetaDaAna`, e você guardou a caneta dela em uma gaveta, onde colou a etiqueta. Ela escolheu o nome `canetaDaAna`, mas poderia ser qualquer outro nome e seu conteúdo poderia ser qualquer um também, como um livro, por exemplo, e não uma caneta.

Quando Ana precisar da caneta, ela irá te chamar e pedir pela `canetaDaAna`, e você a entregará o conteúdo da gaveta, ou seja, a caneta.

## E como isso se relaciona com as variáveis?

Seu armário de gavetas no exemplo acima representa a memória do computador. Quando criamos uma variável, estamos solicitando ao computador que reserve uma “gavetinha” em sua memória para que guarde algo que precisaremos usar futuramente, e fazemos isso atribuindo um nome de variável que poderemos chamar a qualquer momento e que retornará o conteúdo que guardamos dentro dela. Esse nome pode ser um nome qualquer, no entanto sempre que solicitado ele trará como resposta aquilo que você armazenou nele.

## O que são variáveis?

Variáveis são elementos que permitem que valores sejam manipulados ao longo da execução de seu código, através da definição de um nome para armazenar um valor que será usado repetidas vezes. Essa definição do nome e do conteúdo que será contido nele é o que nós chamamos de **declaração**.

Esse valor pode ser alterado ao longo do código, por isso o nome “váriavel”.

Observe o seguinte exemplo:

```css
:root{
     --tamanho-da-fonte:  24px;
}
```

Criamos no `:root`, ou seja, no escopo global de um código, uma variável que foi declarada com o nome `--tamanho-da-fonte` e seu valor foi atribuído como `24px`. Toda vez que chamarmos pelo nome `--tamanho-da-fonte`, iremos obter como retorno o valor `24px`.

Variáveis são utilizadas diariamente pelas pessoas desenvolvedoras para que consigam manipular e reutilizar valores em seu código e estão presentes nas mais diversas linguagens de programação, pois são elementos base ao criar qualquer código que tenha a mínima funcionalidade. Portanto, conforme você evoluir em seus conhecimentos no desenvolvimento é certo que irá lidar muito com variáveis.

Para saber mais sobre as variáveis em CSS, você pode conferir a [documentação](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Using_CSS_custom_properties).

Para que continue praticando HTML e CSS, é importante que siga desenvolvendo novos projetos para aprimorar seus conhecimentos. Trouxemos algumas sugestões legais para você:

## Página-presente

Imagine utilizar seus conhecimentos em HTML e CSS para presentear alguém!

Você pode criar uma página homenageando alguém que você goste e presentear essa pessoa.

É possível fazer uma galeria com fotos suas, escrever um texto bem legal e adicionar links para coisas que a pessoa goste.

Essas páginas também são frequentemente feitas como presente de aniversário.

Você pode embarcar nessa temática trazendo recursos como vídeos, imagens e até músicas para o projeto.

Assim, você evolui seu conhecimento e ainda faz alguém feliz!

![Tela com exemplo de página presente, composta por um cabeçalho rosa escuro com os textos “Home”, “Carta” e “Nossas Fotos” em verde claro dispostos lado a lado no canto esquerdo. Abaixo há o conteúdo principal com fundo cinza claro, na primeira seção há o texto “Essa página é um presente para você: Feliz Aniversário!” escrito em rosa escuro ao lado esquerdo e do lado direito há uma ilustração com três pessoas comemorando um aniversário. Na seção abaixo há o texto centralizado “Uma carta para você” e abaixo dele um parágrafo de texto “lorem ipsum”, ambos em rosa escuro. Abaixo há outra seção com o título “Nossas Fotos”, seguido de 6 ilustrações simulando fotos de pessoas, essas ilustrações estão distribuídas em 2 linhas e 3 colunas. Todas possuem pontos com tons de verde menta. Abaixo há o rodapé do projeto, também com fundo rosa escuro com os textos “Criado em janeiro de 2023” e “People ilustrations by storyset” escritos em branco.](https://caelum-online-public.s3.amazonaws.com/2811-html-css-cabecalho-footer-variaveis-css/aula5-img3.png)

## Lojinha

Que tal soltar a criatividade e inventar uma lojinha de algo que você goste?

Você pode criar uma página para exibir produtos de uma marca fictícia que ache interessante e assim treinar `display: flex` compondo a exibição dos seus produtos na página, por exemplo.

![gif com exemplo de página de “lojinha” de plantas feita com HTML e CSS](https://caelum-online-public.s3.amazonaws.com/2811-html-css-cabecalho-footer-variaveis-css/aula5-img4.gif)

## Página de favoritos

Por último, um dos projetos preferidos das pessoas estudantes de HTML e CSS: Criar uma página de favoritos!

Esse projeto é muito divertido pois permite que você crie uma página com as coisas que você mais gosta. Podem ser filmes, séries, músicas, animes, jogos, produtos entre outros.

Aqui você pode escolher um único tema ou então criar seções para cada tema favorito.

Adicione imagens, links para visualizar seus favoritos, vídeos sobre eles e etc.

Você pode abusar da criatividade nesse projeto: Se você escolher músicas, por exemplo, crie links para navegação em outras páginas contando a história da música que escolheu, ou de quem compôs, ou até mesmo o porque é uma favorita.

![imagem com exemplo de página de filmes favoritos feita com HTML e CSS](https://caelum-online-public.s3.amazonaws.com/2811-html-css-cabecalho-footer-variaveis-css/aula5-img5.png)

Você também encontra várias outras ideias de projeto nesse vídeo no canal da Rafa Ballerini: https://youtu.be/y4ltLH9iK8E

Enfim, não deixe de praticar e evoluir seu conhecimento. Bons estudos, até a próxima!