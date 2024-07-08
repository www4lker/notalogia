---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/superestilizando-o-seu-css/","tags":["css","ANELO",808080,"ffffff",800000,"ff0000"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# superestilizando o seu css

## criado em: 
-  30-03-2023 - 13:31

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/HTML e CSS 1\|HTML e CSS 1]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/HTML e CSS 2\|HTML e CSS 2]]
- tags: #css #ANELO 
- Fontes & Links: 

---
## Nessa aula, você aprendeu como:

-   Utilizar as cores no CSS;
-   Utilizar as cores hexadecimais no CSS;
-   Utilizar paleta de cores de terceiros;
-   Alterar as cores de fundo e dos textos;
-   Extrair a cor do Figma para utilizar no CSS;
-   Destacar o texto e alterar a cor do texto em destaque.
---

**Guilherme:** Já conseguimos alterar tanto a cor de fundo quanto a cor do texto, mas ainda há um detalhe importante.

No Figma, será que a cor branca que colocamos com `white` é realmente esta?

Abrindo o projeto no Figma e selecionando o bloco de texto, notaremos que há duas cores: um valor `22D4FD` para azul claro e `F6F6F6` para o branco, e não `white`.

Mas isso tem uma diferença, afinal não faz sentido dizermos no cotidiano que outros objetos de cor branca são da cor "F6F6F6", como uma camisa por exemplo, dizemos que é "branca". Mas para o computador, faz sentido.

**Rafaella:** Vamos usar esses valores obtidos do Figma em nossas propriedades no arquivo `style.css`. Copiaremos "F6F6F6" e colaremos no lugar de `white` em `color:` para salvarmos e vermos o resultado.

```css
body {
    background-color: black;
    color: F6F6F6;
}
```

No navegador, notaremos que o texto está em preto, da mesma cor que o fundo, e não ficou visível.

**Guilherme:** Sabemos que o texto ainda está no corpo da página quando selecionamos com o cursor do mouse.

**Rafaella:** Está com a cor padrão que é preto igual ao fundo, do mesmo jeito que estava antes de aplicarmos estilos no CSS. Ou seja, apenas o que escrevemos de valor para a cor branca não está funcionando.

**Guilherme:** Não reconheceu porque temos que adicionar um sinal quando queremos representar cores de outra forma, que é a cerquilha ou _hashtag_ `#` antes do valor da cor.

```css
body {
    background-color: black;
    color: #F6F6F6;
}
```

**Rafaella:** Salvando e atualizando a página no navegador, conseguiremos deixar o texto em branco sobre o fundo preto.

**Guilherme:** Então teremos um problema, pois conseguimos representar cores no HTML e estilizando no CSS de maneiras diferentes.

Na barra de busca no navegador, pesquisaremos por "cores no CSS" e, logo no topo da lista de resultados do buscador, aparecerá a **Especificação CSS Level 1**.

Especificação

Palavra-chave

valores hex RGB

gray

#808080

**CSS** Level 1

white

#ffffff

marron

#800000

red

#ff0000

Portanto, existem formas diferentes de gerar nossas cores.

Acessando a [documentação oficial do Mozilla neste link](https://developer.mozilla.org/pt-BR/docs/Web/CSS/color_value), encontraremos uma tabela mais completa de cores, nomes e códigos.

Repararemos que podemos usar **palavras-chave** para as cores como o `black` e `white` que fizemos antes. Mas também poderemos representá-las com **Notação Hexadecimal RGB** que sempre começam com a cerquilha `#` seguido de seis números ou letras.

**Rafaella:** O Hexadecimal usa números de zero até nove e da letra "A" até "F". Por exemplo, o preto que é a ausência de cor é "000000", e o branco que é a junção de todas as cores é "ffff".

Todas as outras cores estão neste intervalo e sua numeração representa a proporção de vermelho, verde e azul que possuem, ou seja, _red_, _green_ e _blue_ que compõe o padrão RGB.

**Guilherme:** Vamos fazer um teste então. Eu vou escolher a cor "purple" por palavra-chave.

**Rafaella:** E eu vou outra com valor "00ffff" pelo RGB.

**Guilherme:** De volta ao código `style.css`, vamos usar a cor `purple` em `background-color:` e `#00ffff` em `color:`

```css
body {
    background-color: purple;
    color: #00ffff;
}
```

**Guilherme:** Vamos salvar e ver como ficaram essas cores aleatórias na página do navegador.

![Página do projeto no navegador, em que o nome da aba é "Portfolio" e a url é "127.0.0.1:5500/index.html". No corpo da página, aparece somente o texto "Eleve seu negócio digital a outro nível com um Front-end de qualidade!" em uma linha única, escrito em azul claro com fonte serifada e em um fundo roxo. Abaixo, está o texto do parágrafo também em azul claro e com tamanho menor. Abaixo deles, está a fotografia em preto e branco representando Joana Santos, uma mulher desenvolvedora, sentada em frente a um notebook aberto. A imagem também conta com um desenho em ciano de uma linha circulando Joana e seu notebook três vezes e terminando em uma estrela.](https://cdn1.gnarususercontent.com.br/1/308174/3b763c63-ef52-4860-a0b3-1456cd1ad93a.png)

**Guilherme:** Não ficou tão ruim, mas a versão que a pessoa _designer_ elaborou para nosso projeto é muito melhor. De volta ao nosso código no VSCode, voltaremos com as cores `black` e `#F6F6F6` do nosso projeto.

Isso acontece porque a junção das cores de **forma harmônica** é baseada em estudos, boas práticas e conceitos da área.

> Deixaremos um **desafio** para pesquisar e escolher as cores que poderiam ficar interessantes, e há várias ferramentas para isso.

Pesquisando no navegador, digitaremos "roda de cores adobe" na barra de busca e clicaremos no [link do **Adobe Colors**](https://color.adobe.com/pt/create/color-wheel).

Esta Roda de Cores produz paletas com boa interação entre si que ajudam na escolha dos estilos, e há várias regras de harmonia de cores como "Análogo", "Monocromático", "Tríade", "Complementar"< entre outras. Vale a pena explorar, mas há outros também.

**Rafaella:** Continuando, poderemos deixar a cor `black` como padrão substituindo-a pelo Hexadecimal `#00000` em `background-color`.

```css
body {
    background-color: #000000;
    color: #F6F6F6;
}
```

**Rafaella:** Salvaremos e rodaremos a aplicação sem problemas.

---

# Para saber mais: escolhendo as cores do projeto


Chegou a hora de colocar as mãos na massa. Desafiamos você a escolher cores para o seu projeto, pois uma paleta é essencial para providenciar uma boa experiência de usuário e enriquecer a identidade de sua página. E para te ajudar com esse desafio, separamos alguns sites.

## Coolors

O [Coolors](https://coolors.co/) possui uma interface bem clara. Com a barra de espaço do seu teclado, você consegue criar várias combinações, e uma das funções mais legais é a opção travar, que você pode usar se gostar de apenas uma cor, e assim que você clica nela, consegue continuar elaborando outras combinações levando em conta a cor que você escolheu.

![Tela do seletor de paleta de cores do site Coolors](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula5-img1.gif)

## Adobe Color

O [Adobe color](https://color.adobe.com/pt/create/color-wheel) apresenta um Color Wheel (roda de cores) que pode ser ajustado de maneiras variadas para obter uma harmonia de cores, e você pode aplicar diversas regras de harmonia de cores, como o modo análogo, monocromático, tríade, complementar, quadrado, composto, entre outros.

![Tela da roda de cores do site Adobe Color, onde as paletas de cores se modificam ao selecionar opções como “monocromático” e “complementar”](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula5-img2.gif)

## Color Hunt

O [Color Hunt](https://colorhunt.co/) dispõe de diversas paletas elaboradas. Você consegue encontrar a combinação que mais te agrada e consegue buscar por palavras-chave como pastel, vintage, neon e assim por diante. E caso não encontre nenhuma que te agrade, você consegue criar a sua própria paleta clicando nos três pontinhos do canto superior direito da página.

![Rolagem da tela com várias opções de paletas de cores do site Color Hunt](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula5-img3.gif)

## Color Tool - Material Design

O [Color Tool](https://m2.material.io/resources/color/#!/?view.left=0&view.right=0&primary.color=6002ee) é ótimo para criar, compartilhar e aplicar paletas de cores à interface do usuário, bem como é possível medir o nível de acessibilidade de qualquer combinação de cores na aba _accessibility_.

![Tela do seletor de paleta de cores do site Color Tool - Material Design, no qual é possível simular a interface de um aplicativo e modificar a paleta de cores](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula5-img4.gif)

São opções incríveis, não é? Se você conhece algum outro site nesse estilo pode indicar no fórum ou no [Discord da Alura](https://discord.gg/QeBdgAjXnn) para que outras pessoas estudantes também conheçam.

Agora é com você! Encontre a paleta de cores que mais te agrada e aplique no projeto para deixá-lo com a sua carinha :D

---

**Rafaella:** Olhando para o nosso _design_, já aplicamos os estilos de plano de fundo e decidimos a cor principal das nossas fontes.

Porém, o trecho "com um Front-End de qualidade!" em destaque no título está na cor azul.

Por isso definimos a _tag_ `<strong>` em `index.html` para destacarmos essa parte. Como utilizaremos o CSS para estilizar com essa outra cor?

**Guilherme:** No arquivo `style.css`, pegamos a `body` que queríamos, abrimos chaves e dentro colocamos as duas propriedades.

Já que `strong` também é uma _tag_, poderemos pegá-la e indicar qual a cor iremos usar nesse trecho do texto com `color:`.

Pegaremos o valor hexadecimal dela no projeto do Figma, que é `#22D4FD` e colaremos na propriedade.

```css
body {
    background-color: #000000;
    color: #F6F6F6;
}

strong {
    color: #22D4FD;
}
```

**Rafaella:** Vamos salvar e voltar à página atualizada no navegador para vermos o resultado.

![Página do projeto no navegador, em que o nome da aba é "Portfolio" e a url é "127.0.0.1:5500/index.html". No corpo da página, aparece o título "Eleve seu negócio digital a outro nível" em cor branca, seguido de "com um Front-end de qualidade!" em cor azul claro em uma linha única, com fonte serifada e em um fundo preto. Abaixo, está o texto do parágrafo também em branco e com tamanho menor. Abaixo deles, está a fotografia em preto e branco representando Joana Santos, uma mulher desenvolvedora, sentada em frente a um notebook aberto. A imagem também conta com um desenho em ciano de uma linha circulando Joana e seu notebook três vezes e terminando em uma estrela.](https://cdn1.gnarususercontent.com.br/1/308174/9b511153-76a7-480e-8234-b49598056d4d.png)

**Guilherme:** Funcionou, mas se voltarmos ao Figma, notaremos que, durante todo o projeto, a maioria dos textos que aparecem possuem a cor branca `#F6F6F6`.

Já o trecho "com um Front-end de qualidade!" foi definido com `<strong>`. Mas se a colocarmos em outra parte do projeto, também irá alterar a cor?

**Rafaella:** Vamos testar para saber. No `index.html`, copiaremos a _tag_ de destaque do trecho e a colaremos para destacar o trecho com as três tecnologias citadas no texto do parágrafo em `<p>`, "React, HTML e CSS". O restante ficará em branco mesmo.

```xml
<!DOCTYPE html>
<html lang="pt-br">

//código omitido

<body>
    <header</header>
    <main>
       <h1>Eleve seu negócio digital a outro nível <strong>com um Front-end de qualidade!</strong></h1>
        <p>Olá! Sou Joana Santos, desenvolvedora Front-end com especialidade em <strong>React, HTML e CSS</strong>. Ajudo pequenos negócios e designers a colocarem em prática boas ideias. Vamos conversar? 
        </p>

//código omitido

    </main>
    <footer></footer>
</body>
</html>
```

**Rafaella:** Vamos salvar e analisar o resultado no navegador.

![Página do projeto no navegador igual à anterior, porém o trecho "React, HTML e CSS" do texto do parágrafo abaixo do título está em destaque na cor azul claro.](https://cdn1.gnarususercontent.com.br/1/308174/364f4d67-2b19-4c64-8322-46e38a13b587.png)

**Rafaella:** Veremos que a `<strong>` deixou na mesma cor azul claro que havíamos definido no CSS, portanto toda vez que ela for aplicada, terá a mesma cor.

**Guilherme:** Certo, mas não é o que queremos, pois teoricamente, se nosso projeto continuar evoluindo e o código aumentando, todas as partes de texto que tiverem essa _tag_ terão a cor que definimos.

**Rafaella:** Caso queiramos depois criar um subtítulo com outro trecho em destaque em uma cor diferente, não poderemos usar a `<strong>`.

**Guilherme:** Exatamente, então precisaremos de uma forma para dizer que somente uma dessas _tags_ usará o azul claro. Mas faremos isso mais adiante.