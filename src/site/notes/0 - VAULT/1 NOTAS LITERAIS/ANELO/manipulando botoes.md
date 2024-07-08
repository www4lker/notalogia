---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/manipulando-botoes/","tags":["css","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# manipulando botoes

## criado em: 
-  30-03-2023 - 16:48

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/ajustando o espaçamento\|ajustando o espaçamento]]
- tags: #css #ANELO 
- Fontes & Links: 

---

## Nessa aula, você aprendeu como:

-   Posicionar e estilizar botões;
-   Criar e utilizar divisões (divs) no projeto;
-   Identificar o espaçamento no Figma;
-   Retirar o sublinhado com o text-decoration;
-   Arredondar bordas com border-radius.

---

**Guilherme:** Rafa, com as fontes, o projeto está com outra cara. Porém, existe uma parte distante do resultado proposto no Figma.

**Rafaella:** Sim, os links do _Instagram_ e do _Github_.

**Guilherme:** Não dá pra ver. Eu estou de óculos e não consigo enxergar.

Em nenhum momento estilizamos nossos botões. Vamos fazer isso?

**Rafaella:** Vamos. Podemos estilizá-los e depois posicioná-los.

Voltando no nosso [Figma do projeto](https://www.figma.com/file/4EKKCbr5rS93RWP7kRjXIz/Portfolio---Curso-1?t=6dfeFknOinJA1UCL-0), veremos que os botões possuem espaçamentos.

**Guilherme:** Existe um grupo que os une. Ele nos diz que existem dois botões na mesma linha.

**Rafaella:** Exatamente. Temos também um espaço entre eles. É isso que traremos para nosso código.

Já que os botões parecem estar unidos num grupo, podemos criar de fato um grupo entre eles. Acessaremos o arquivo `index.html` e veremos os botões localizados na _tag_ âncora, ou `<a>`. Para agrupá-los, criaremos uma _tag_ chamada `<div>` que significa "divisão". Ela envolverá os dois `<a>` dos botões.

```javascript
    <main class="apresentacao">
        <section class="apresentacao__conteudo">
            <h1 class="apresentacao__conteudo__titulo">Eleve seu negócio digital a outro nível <strong class="titulo-destaque">com um Front-end de qualidade!</strong></h1>
            <p class="apresentacao__conteudo__texto">Olá! Sou Joana Santos, desenvolvedora Front-end com especialidade em React, HTML e CSS. Ajudo pequenos negócios e designers a colocarem em prática boas ideias. Vamos conversar?</p>
            <div>
                <a href="https://instagram.com/rafaballerini">Instagram</a>
                <a href="https://github.com/guilhermeonrails">Github</a>
            </div>
        </section>
        <img src="imagem.png" alt="Foto da Joana Santos programando">
```

Utilizamos esta _tag_ para agrupamentos bem específicos, como no caso dos nossos botões. Não utilizamos para esses fins as _tags_ `<main>` ou `<section>`.

**Guilherme:** Não é uma divisão de estrutura. Ela só aponta um agrupamento entre os elementos. E não precisam ser necessariamente botões. Podemos agrupar elementos de texto, desde que não se enquadrem em um contexto maior.

**Rafaella:** Em um contexto semântico, né. Por exemplo: o conteúdo principal precisa de um nome: é o `<main>`. Se estamos trabalhando com um agrupamento de elementos que querem dizer uma coisa só, digitamos `<section>`. Já a `<div>` é puramente visual e serve apenas para juntar os dois botões em um lugar só, não possui valor semântico.

Vamos estilizar os botões. Posicionaremos um botão à esquerda e outro à direita, na horizontal. Para isso, criaremos uma `class` para essa `div`.

**Guilherme:** Podemos criar uma `class` para qualquer elemento, né.

**Rafaella:** Qualquer elemento ou _tag_. Qual nome você quer dar a ela, Gui?

**Guilherme:** Já que estamos dentro da seção de `apresentacao`, vamos nomeá-la de `apresentacao__links`.

```javascript
    <main class="apresentacao">
        <section class="apresentacao__conteudo">
            <h1 class="apresentacao__conteudo__titulo">Eleve seu negócio digital a outro nível <strong class="titulo-destaque">com um Front-end de qualidade!</strong></h1>
            <p class="apresentacao__conteudo__texto">Olá! Sou Joana Santos, desenvolvedora Front-end com especialidade em React, HTML e CSS. Ajudo pequenos negócios e designers a colocarem em prática boas ideias. Vamos conversar?</p>
            <div class="apresentacao__links">
                <a href="https://instagram.com/rafaballerini">Instagram</a>
                <a href="https://github.com/guilhermeonrails">Github</a>
            </div>
        </section>
        <img src="imagem.png" alt="Foto da Joana Santos programando">
```

**Rafaella:** Salvaremos esse código e acessaremos o arquivo `style.css`. Abaixo de `.apresentacao__conteudo__texto{}` criaremos um `.apresentacao__links{}`.

```css
.apresentacao__conteudo__texto{
    font-size: 24px;
    font-family: 'Montserrat', sans-serif;
}

.apresentacao__links{

}
```

Dentro de suas chaves criaremos um Flexbox. Já fizemos algo parecido quando selecionamos o elemento pai e utilizamos o `space-between`. Sempre que utilizamos o Flexbox, precisamos fazer um procedimento no elemento pai. Lembrando que se trata do pai pois incluímos os dois botões em seu interior como elementos filhos, e são estes que posicionaremos.

O que devemos adicionar como propriedade no elemento pai?

**Guilherme:** Um `display: flex`.

**Rafaella:** Exatamente. Adicionaremos um `display: flex` dentro das chaves de `.apresentacao__links{}`. Abaixo desse comando acrescentaremos a propriedade `justify-content: space-between`.

```css
.apresentacao__links{
    display: flex;
    justify-content: space-between;
}
```

Salvaremos esse código e retornaremos à nossa aplicação exibida no navegador. Nela veremos que os botões estão separados, um de cada lado.

**Guilherme:** Deu certo, os botões estão separados. O nosso próximo desafio é deixá-los bonitos.

---

#### Quando utilizar div

A tag `<div>` define uma divisão em um documento HTML e costuma ser usada como um contêiner para outros elementos, o que ajuda na estilização do bloco. Por esse motivo, a `<div>` é frequentemente utilizada quando precisamos agrupar elementos sem usar as tags semânticas do HTML. Isso acontece porque a `<div>` não tem valor semântico. Portanto, não significa nada para os navegadores e mecanismos de pesquisa.

Além do mais, por ser muito utilizada para agrupar elementos, acaba facilitando na organização das informações nos layouts. Dessa forma, pode ser formatada e manipulada organicamente via CSS. Geralmente vem acompanhado de atributos de ID e classe para facilitar essa organização e formatação.

Se quiser aprofundar no assunto, recomendamos que leia a [documentação oficial](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/div).

---

**Rafaella:** Nesta aula, estilizaremos os **botões**.

**Guilherme:** Observando nosso código no VSCode, criamos o `.apresentacao__links` com `display: flex` para as duas _tags_ âncoras, mas agora o processo será diferente, pois queremos estilizar os dois botões. Porém, o estilo de um é igual ao do outro.

No projeto do Figma, tanto o botão "Instagram" quanto o de "GitHub", ou ainda se criarmos mais, possuem as mesmas características: retângulo com vértices arredondados, fundo azul e usam a mesma fonte sem serifa.

**Rafaella:** Só muda o texto que definimos no HTML.

**Guilherme:** Exatamente, então uma ideia seria criarmos uma classe que será utilizada para ambos os botões.

**Rafaella:** No arquivo `index.html`, iremos à `<div>` da `class` igual a `"apresentacao__links"` e, na _tag_ `<a>`, adicionaremos a nova classe chamada `"apresentacao__links__link"` antes de `href`.

Utilizaremos essa mesma `class` para a _tag_ âncora seguinte.

```xml
//código omitido

    <main class="apresentacao">
        <section class="apresentacao__conteudo">

//código omitido

            <div class="apresentacao__links">
                <a  class="apresentacao__links__link" href="https://instagram.com/rafaballerini">Instagram</a>
                <a class="apresentacao__links__link" href="https://github.com/guilhermeonrails">Github</a>
            </div>
        </section>
        <img src="imagem.png" alt="Foto da Joana Santos programando">
    </main>
    <footer></footer>
</body>
</html>
```

**Rafaella:** Em nosso arquivo `style.css`, adicionaremos essa nova classe ao final do código para estilizarmos dentro das chaves.

**Guilherme:** Vamos começar pela cor de fundo que geralmente é feita com `background-color:`. Funciona também para a _tag_ âncora?

**Rafaella:** Sim, funciona! Então podemos buscar no Figma qual é o valor hexadecimal ao clicarmos no botão, que no caso é `#22D4FD`. No arquivo CSS, adicionaremos o `background-color:` seguido deste valor que obtivemos.

Salvaremos e analisaremos o resultado no navegador.

```css
//código omitido

.apresentacao__links__link {
    background-color: #22D4FD;
}
```

**Rafaella:** Com isso, já teremos a cor azul no fundo dos botões, mas ainda estão muito pequenos e diferentes do Figma.

Vamos continuar estilizando o botão pegando sua largura de `280px`. Copiaremos este valor e inseriremos na propriedade `width:` do arquivo CSS também.

**Guilherme:** O texto ainda está alinhado à esquerda, e precisamos centralizá-lo.

**Rafaella:** Para isso, teremos a propriedade `text-align:` com o valor `center` em `.apresentacao__links__link` para que fique alinhado ao centro.

Analisando o resultado no navegador, os escritos dos botões já estarão centralizados em suas áreas azuis, as quais ainda estão com as pontas em noventa graus.

**Guilherme:** Sim, pois no projeto final, esses retângulos possuem os vértices arredondados.

**Rafaella**: Têm sim, e este raio de arredondamento é estabelecido pela propriedade `border-radius:`, e no Figma veremos que seu valor é de `16px`.

Com isso, o resultado no navegador ficará mais parecido com o projeto.

**Guilherme:** Já está melhorando! Mas a fonte dos textos dos botões deve ser maior também, contendo `24px`.

**Rafaella:** Pegaremos este valor e adicionamos à propriedade `font-size:` no arquivo CSS.

**Guilherme:** Já ficou bem melhor!

**Rafaella:** Um ponto interessante que ainda está diferente do Figma é o espaço que há entre os limites do retângulo do botão e o texto central.

Lembrando do Box Model, queremos uma margem entre o conteúdo e a borda. Abriremos nosso projeto no navegador, clicaremos com o botão direito do mouse e escolheremos a opção "Inspecionar" para abrirmos a aba lateral.

Se passarmos o cursor e selecionarmos qualquer elementos, exibiremos a seleção no BoxModel da aba "Estilos". Se quisermos aumentar o espaço entre os elementos, precisaremos colocar um valor no `padding:`.

Para essa propriedade, iremos ao Figma, selecionaremos o conteúdo, apertaremos a tecla "Alt" e visualizaremos o valor das distâncias passando o mouse sobre a área que queremos alterar, que este caso será de `21.5px` em relação à base e o topo no botão "Instagram".

**Guilherme:** Vamos ver o conteúdo do "GitHub" também?

**Rafaella:** Também é `21.5px`, então adicionaremos o `padding:` com este valor.

Porém, já temos uma distância boa do texto até as bordas laterais, então não precisaremos alterá-la, e sim apenas no `top` e `bottom` relativos ao topo e à base respectivamente.

Até agora, selecionávamos apenas um valor para o `padding:`, e se escrevermos o valor de `21.5px` e salvarmos, essa distância será colocada para todos os lados da área.

Quando queremos apenas selecionar um dos eixos, inserimos dois valores: o primeiro sempre será relativo ao eixo vertical, enquanto o segundo é do horizontal. Como não alteraremos este último, deixaremos como zero mesmo.

```css
//código omitido

.apresentacao__links__link {
    background-color: #22D4FD;
    width: 280px;
    text-align: center;
    border-radius: 16px;
    font-size: 24px;
    padding: 21.5px 0;
}
```

**Rafaella:** Feito isso, já veremos a diferença no projeto do navegador.

**Guilherme:** No Figma, os textos dos botões de "Instagram" e "GitHub" não estão sublinhados, diferente do que temos até agora. Vamos tirá-la também?

**Rafaella:** Esta linha abaixo dos conteúdos é um padrão quando estamos desenvolvendo, e teremos que tirar sua decoração.

**Guilherme:** Faltam duas coisas ainda: a cor do texto do botão e a fonte, pois se observarmos, a fonte está em um tom de azul um pouco mais escuro que a cor do fundo da área.

**Rafaella:** Ainda está como link clicável, então retiraremos o sublinhado da decoração com `text-decoration:` sendo `none` e daremos uma cor ao conteúdo com `color:` igual a `#000000`, cujo valor da cor preta também foi obtido do Figma.

Por fim, a fonte ainda está diferente, e descobrimos no Figma também que é a Montserrat que já importamos no projeto.

Portanto poderemos simplesmente fazer da mesma forma que aplicamos no parágrafo usando `font-family:` de `'Montserrat'` e retirando as serifas com `sans-serif`.

Como é a mesma do seletor de `.apresentacao__conteudo__texto`, apenas copiaremos a linha e colaremos na `.apresentacao__links__link`.

Com isso, nosso botão já estará bem parecido com o projeto final, muito mais bonito e interessante. Mas, se repararmos com atenção no texto dos links, notaremos que as letras deveriam ser mais grossas.

No Figma, as selecionaremos e veremos que, na aba lateral, mesmo a fonte sendo da família Montserrat na parte de "Text", perceberemos que a propriedade `font-weight:` relativa ao peso da fonte é de `600` no HTML da aba de "Inspect".

Ainda não importamos este tipo de fonte, que é um detalhe pequeno porém importante.

No navegador, buscaremos a página do Google Fonts e pesquisaremos a fonte "Montserrat" na barra de busca. Clicaremos nesta opção e, na lista mais adiante da página, procuraremos pelo peso de `600`.

Selecionaremos clicando no link de "Select SemiBold 600" ao lado da opção correta, e pegaremos o código HTML atualizado de `<style>` na parte de "Use on the web" ou "use na web" da aba lateral.

O copiaremos e o colaremos no `@import url()` do topo do arquivo CSS, colocaremos o `font-weight: 600` abaixo de `font-size` e salvaremos.

```css
@import url('https://fonts.googleapis.com/css2?family=Krona+One&family=Montserrat:wght@400;600&display=swap');

//código omitido

.apresentacao__links__link {
    background-color: #22D4FD;
    width: 280px;
    text-align: center;
    border-radius: 16px;
    font-size: 24px;
    font-weight: 600;
    padding: 21.5px 0;
    text-decoration: none;
    color: #000000;
    font-family: 'Montserrat', sans-serif;
}
```

**Rafaella:** Observando o projeto no navegador, veremos se irá funcionar.

![Projeto no navegador. Temos dois blocos de conteúdo, lado a lado, centralizados sobre fundo preto. O bloco esquerdo possui um texto que se divide em duas partes: título e subtítulo. O título apresenta um texto em negrito dividido em duas cores: "Eleve seu negócio digital a outro nível" em branco, seguido de "com um Front-end de qualidade!" em ciano. O subtítulo está na cor branca, e exibe o texto de apresentação da Joana Santos. Abaixo do subtítulo temos dois botões na cor ciano, lado a lado: no botão esquerdo temos o texto "Instagram" e no direito o texto "Github". O espaçamento entre esses primeiros elementos é quase inexistente. Já o bloco direito se constitui de uma fotografia em preto e branco representando Joana Santos, uma mulher desenvolvedora, sentada em frente a um notebook aberto. A fotografia também conta com um desenho em ciano de uma linha circulando Joana e seu notebook três vezes e terminando em uma estrela.](https://cdn1.gnarususercontent.com.br/1/1319058/4053e60c-95b2-441a-a952-2f9b03a0966f.png)

**Guilherme:** Ficou bem mais interessante, pois estava visualmente diferente.

**Rafaella:** Agora já estamos com nosso projeto bem mais parecido com o Figma.

---

# CSS Border

A propriedade `border` é responsável pelas bordas dos elementos HTML. Ao inserir um elemento em um documento HTML, há várias possibilidades de estilizar sua borda. Você pode utilizar estilos que a propriedade já possui, além de poder também alterar sua cor, espessura e até mesmo seu formato! Utilizando apenas o poder do CSS!

Se quiser mergulhar de vez nesse assunto, você pode explorar o nosso artigo [CSS Border: estilizando com bordas seus elementos CSS](https://www.alura.com.br/artigos/css-border-estilizando-bordas-elementos-css). Nele você vai encontrar um passo a passo explicado e detalhado de como utilizar essa propriedade.