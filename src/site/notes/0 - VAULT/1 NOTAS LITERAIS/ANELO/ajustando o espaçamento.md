---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/ajustando-o-espacamento/","tags":["css","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# ajustando o espaçamento

## criado em: 
-  30-03-2023 - 17:34

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/HTML e CSS 2\|HTML e CSS 2]]
- tags: #css #ANELO
- Fontes & Links: https://cursos.alura.com.br/course/html-css-classes-posicionamento-flexbox/task/121097

---

## Nessa aula, você aprendeu como:

-   Definir espaçamento vertical e horizontal;
-   Posicionar os elementos em coluna com Flexbox;
-   Utilizar o recurso Gap para espaçar cada elemento filho.

---

**Guilherme:** Todos os detalhes do nosso trabalho estão bem bacanas até agora! Mas ainda está diferente do projeto no Figma. Alguns espaçamentos estão diferentes.

**Rafaella:** Exatamente! Havíamos definido uma margem de 10% em `.apresentacao` de `style.css` para o nosso conteúdo inteiro `"apresentacao"`, que na verdade é um `<main>` com tudo o que estamos usando.

Essa `margin:` está fazendo com que dez por cento da página fique para dentro, deixando a disposição dos elementos diferente do projeto no Figma.

Também temos a opção de fixarmos um valor apertando a tecla "Alt" no Figma para obter os valores das margens em pixels, mas isso não é muito recomendável, afinal pode mudar em outras telas.

Como vimos antes, trabalhamos com o `padding:` do botão em que colocamos o valor de `21.5px` apenas para o lado vertical e um valor `0` para o horizontal, então podemos simplesmente inserir um valor maior para as laterais em `margin:`, que são o segundo valor após o `10%`.

Adicionaremos `15%` ao `margin:` de `.apresentacao` em `style.css` para salvarmos e testarmos o resultado no navegador.

Com isso, notaremos que os blocos de textos e a imagem da página já se posicionaram mais ao centro da tela.

Outra questão interessante para trabalharmos é o posicionamento dos elementos textuais que estão bem juntos.

**Guilherme:** Deve existir um certo espaçamento, e conseguimos até ver este valor.

**Rafaella:** Sim! Este valor é facilmente obtido no projeto do Figma para deixarmos fixo, que no caso é `40px`.

Poderemos fazer isso usando o FlexBox que já conhecemos, o qual sempre será colocado na _tag_ `<container>`. Temos os três elementos textuais de título `<h1>`, o parágrafo `<p>` e a `<div>` com os dois botões do nosso arquivo `index.html`, então colocaremos o FlexBox em `"apresentacao__conteudo"`.

Abrindo o `style.css`, iremos até `.apresentacao__conteudo` e adicionaremos `display: flex` abaixo de `width:`.

```css
//código omitido

.apresentacao__conteudo {
    width: 615px;
    display: flex;
}

//código omitido
```

**Rafaella:** Com isso, usaremos uma nova propriedade do FlexBox chamada `flex-direction`, descrita na documentação de _guide_.

Por padrão, ela é feita em _row_, fazendo com que nossos itens fiquem organizados por linhas.

![Projeto do nosso portfólio no navegador. Temos quatro blocos de conteúdo em sentido vertical, lado a lado, e centralizados sobre fundo preto. O bloco mais à esquerda possui um título em negrito dividido em duas cores: "Eleve seu negócio digital a outro nível" em branco, seguido de "com um Front-end de qualidade!" em ciano. O subtítulo ao lado direito está na cor branca, e exibe o texto de apresentação da Joana Santos. Ao lado do subtítulo, temos dois botões na cor ciano, lado a lado: no botão esquerdo temos o texto "Instagram" e no direito o texto "Github". Já o bloco mais à direita se constitui de uma fotografia em preto e branco representando Joana Santos, uma mulher desenvolvedora, sentada em frente a um notebook aberto. A fotografia também conta com um desenho em ciano de uma linha circulando Joana e seu notebook três vezes e terminando em uma estrela.](https://cdn1.gnarususercontent.com.br/1/308174/b215b13e-0b99-43a4-9dba-787881129765.png)

**Rafaella:** Como queremos que se posicionem na vertical, utilizaremos o `flex-direction: column` abaixo do `display: flex` para que fiquem "em pé" nas colunas.

```css
//código omitido

.apresentacao__conteudo {
    width: 615px;
    display: flex;
    flex-direction: column;
}

//código omitido
```

**Rafaella:** Feito isso, o posicionamento dos elementos voltará ao normal.

Agora precisaremos criar os espaços corretos, e existe outra propriedade descrita no guia do FlexBox chamada `gap`, a qual possuirá o espaçamento dos elementos filhos, que neste caso será `40px` segundo o Figma.

```css
//código omitido

.apresentacao__conteudo {
    width: 615px;
    display: flex;
    flex-direction: column;
    gap: 40px;
}

//código omitido
```

**Rafaella:** Salvaremos e retornaremos ao navegador para analisarmos o resultado.

![Projeto final no navegador. Temos dois blocos de conteúdo, lado a lado, centralizados sobre fundo preto. O bloco esquerdo possui um texto que se divide em duas partes: título e subtítulo. O título apresenta um texto em negrito dividido em duas cores: "Eleve seu negócio digital a outro nível" em branco, seguido de "com um Front-end de qualidade!" em ciano. O subtítulo está na cor branca, e exibe o texto de apresentação da Joana Santos. Abaixo do subtítulo temos dois botões na cor ciano, lado a lado: no botão esquerdo temos o texto "Instagram" e no direito o texto "Github". Já o bloco direito se constitui de uma fotografia em preto e branco representando Joana Santos, uma mulher desenvolvedora, sentada em frente a um notebook aberto. A fotografia também conta com um desenho em ciano de uma linha circulando Joana e seu notebook três vezes e terminando em uma estrela.](https://cdn1.gnarususercontent.com.br/1/935581/49e15161-1a46-4440-9cb5-6a66625f046d.png)

**Rafaella:** Agora já estará bem próximo da realidade que queremos!

---

### Gap

A propriedade `gap` não é exclusiva do Flexbox, porém é utilizada quase sempre em conjunto com ele. Ela especifica no CSS o tamanho dos espaços entre linhas e colunas em layouts de `grid`, `flex` e `multi-column`. Sua sintaxe é bem simples e ela aceita um ou dois valores.

Para entender mais dessa propriedade em específico, recomendamos a leitura do artigo [gap](https://css-tricks.com/almanac/properties/g/gap/), presente no [CSS-Tricks](https://css-tricks.com/).

##### Outras propriedades importantes

Se você deseja aprender sobre outras propriedades importantes para o Flexbox, leia o nosso artigo [Flexbox CSS: Guia Completo, Elementos e Exemplos](https://www.alura.com.br/artigos/css-guia-do-flexbox).

---

## Transcrição

**Guilherme:** Se você chegou até esta etapa, **parabéns!** Está finalizando mais um treinamento aqui da Plataforma Alura.

E o que aprendemos neste curso, Rafa?

**Rafaella:** Conseguimos estilizar tudo em nossa página através da criação de **classes** que definem o que queremos fazer, estilizamos nossos **links** e o **posicionamento dos elementos**, aprendemos sobre o **FlexBox** e soubemos como **importar fontes** no projeto.

**Guilherme:** Ou seja, amadurecemos em relação a como fazer a **estilização de textos** e disposição de itens, mas ainda há muito mais para aprendermos!

Nosso desafio de "mergulhar" em HTML e CSS será ainda mais "profundo" nos próximos cursos.

Porém, se houver qualquer dúvida em relação ao conteúdo deste treinamento, nosso fórum está sempre aberto para nossa comunidade da Alura esclarecer e compartilhar conhecimentos.

**Até o próximo curso!**