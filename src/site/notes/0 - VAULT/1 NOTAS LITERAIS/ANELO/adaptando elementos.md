---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/adaptando-elementos/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# adaptando elementos

## criado em: 
-  03-04-2023 - 14:53

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/checklist do design responsivo\|checklist do design responsivo]]
- tags: #ANELO
- Fontes & Links: 

---

## Nessa aula, você aprendeu:

-   Adaptar elementos;
-   Utilizar a ferramenta do DevTools;
-   Visualizar nosso projeto na versão responsiva;
-   Alterar o tamanho da visualização na tela;
-   Adaptar elementos utilizando a unidades de medidas.

---

**Guilherme:** Conseguimos adaptar nossos textos utilizando outra unidade de medida, mas nossa aplicação não contém só textos. Temos imagens, links e outros elementos na nossa página.

**Rafaela:** E temos que perceber em que momento precisamos alterar o tamanho da imagem e dos outros elementos. Por exemplo, pode ser que vocês estejam assistindo à aula em uma tela completamente diferente da nossa.

Nossa tela tem um tamanho específico e estamos desenvolvendo nosso projeto pensando nessa tela. Caso a sua não seja completamente igual a nossa, pode ter ficado com espaços maiores e com a imagem diferente. São esses pontos que vamos resolver a partir desse momento.

E como conseguimos visualizar essas transição dos tamanhos de pixels da tela?

**Guilherme:** Como nosso projeto fica em uma tela diferente, de outro tamanho?

**Rafaela:** Para visualizar como fica em uma tela de notebook, que é menor, por exemplo, podemos clicar na página com o botão direito, selecionar a opção "Inspecionar". Com isso, a janela de Inspecionar abre na metade direita da tela.

No canto superior esquerdo da janela, o segundo botão, que é o "Alternar barra de ferramentas do dispositivo" tem o ícone de um celular sobrepondo o canto inferior direito de um retângulo. Ao clicar nele, aparece uma margem ao redor da nossa página para fazermos testes.

Nós conseguimos arrastar a margem lateral para direita ou para esquerda, aumentando ou diminuindo as dimensões da tela.

**Guilherme:** Rafa, um detalhe importante é que com o atalho "Ctrl + Shift + M" ativamos ele também. E eu tenho uma curiosidade. Vamos deixar a largura da tela menor, em 720px.

**Rafaela:** Vou escrever essa medida no primeiro campo que está na parte centro-superior da nossa página.

**Guilherme:** Feito isso, reparamos que a página abriu, mas a disposição dos elementos está estranha.

**Rafaela:** Muito. Percebemos que _footer_ está menor, a imagem está levando tudo para direita, os botões estão encostados na imagem, ou seja, está tudo bem caótico.

**Guilherme:** Então vamos corrigir isso em etapas. Antes de modificarmos onde cada coisa ficará, existe uma forma de informarmos que queremos que esse conteúdo, a imagem e os links se adaptem?

Portanto não queremos usar unidades absolutas para esses valores, e sim unidades relativas.

**Rafaela:** Tem sim.

**Guilherme:** E qual unidade usaremos?

**Rafaela:** Na verdade, já até utilizamos em algumas partes, mas para conseguirmos trabalhar no tamanho da imagem, podemos usar a **porcentagem(%)**. Inclusive nós vimos quando abrimos a [documentação do W3Schools, sobre as unidades do CSS](https://www.w3schools.com/cssref/css_units.php), que uma das unidades relativas é a porcentagem.

Vou abrir essa documentação novamente. Tento deixar em português para ficar um pouco mais claro, ele não muda, mas está informando que a porcentagem é relativa ao elemento pai.

Então ao mudarmos o tamanho da imagem para 50%, será 50% do espaço da tag pai da imagem. E quando abrimos o `index.html` para descobrirmos quem é a tag pai da imagem, observamos que ela é filha, assim como a `<section>`, da `<main>`.

Portanto seria o tamanho de 50% da tag _main_, e conseguimos usar essa unidade de medida.

**Guilherme:** Vamos então fazer isso. No lugar das unidades absolutas, usaremos as relativas.

**Rafaela:** Para a imagem, especificamente, ainda não tínhamos criado nenhuma classe, então faremos isso agora. No arquivo `index.html`, vamos até a linha 37 e vamos adicionar um `class` à tag `<img>` e vamos seguir o padrão de nome que estamos utilizando para classe, usando "apresentacao__imagem".

```cpp
<img class="apresentacao__imagem" src="./assets/imagem.png" alt="Foto da Joana Santos programando">
```

Também precisamos fazer isso no outro HTML que temos com o "Sobre mim", que é o `about.html`. Portanto também vamos colar essa classe na linha 25 desse arquivo, deixando o código de imagem idêntico nos dois arquivos.

Agora vamos copiar o nome dessa classe, abrir o `style.css` e vamos colar na linha acima à do `.rodape`, na linha 103. Em seguida abriremos chaves e vamos acrescentar a porcentagem para o tamanho.

**Guilherme:** Como estamos falando de tamanho, vamos configurar o `width`, certo?

**Rafaela:** Na verdade quando mudamos o `width` da imagem, que é a largura, automaticamente a altura também muda, porque ela acompanha a escala da imagem que processamos, seja ela quadrada ou redonda. Então podemos usar:

```css
.apresentacao__imagem {
    width: 50%;
}
```

**Guilherme:** Vamos testar com metade.

**Rafaela:** Até porque estamos realmente usando metade da página.

**Guilherme:** Quando voltamos para nossa página de portfólio, já observamos que mudou, mas a experiência de navegação no celular fica diferente.

Ao arrastarmos a margem lateral para esquerda, diminuindo o tamanho da tela, percebemos que tem um texto e ao lado uma imagem minúscula.

**Rafaela:** O tamanho das outras coisas que estão muito grandes, na verdade, e não a imagem que está pequena

**Guilherme:** Então vamos arrumar os outros elementos, porque, à medida que nossa tela muda de tamanho, o que está legal, mas a disposição do conteúdo está estranha, porque está fixa.

**Rafaela:** Exato, então temos que encontrar uma forma desse conteúdo diminuir também, à medida que diminuímos o tamanho da tela. Vamos descobrir onde alteramos isso.

**Guilherme:** Vamos procurar no `index.html` pelo elemento pai. Nele temos a `apresentacao__conteudo` que é filho do `apresentacao`. Em qual deles mudamos, Rafa?

**Rafaela:** Para mudar apenas o tamanho de onde estão os textos, seria na `<section>`. A imagem está fora da _section_, mas temos uma tag _section_ dentro que contém o título, o texto e os botões.

Portanto, no `style.css`, vamos procurar pela `.apresentacao__conteudo`. Nela reparamos que temos uma `width: 615px`, ou seja, uma largura fixa, por isso está ficando muito grande. Conseguimos transformá-la em porcentagem.

**Guilherme:** Vamos colocar também 50% para começar.

**Rafaela:** Perfeito, Gui. É exatamente o que acho que deveríamos fazer, porque ela ocupa metade do `<main>`, enquanto a imagem ocupa a outra metade.

```css
.apresentacao__conteudo {
    width: 50%;
    display: flex;
    flex-direction: column;
    gap: 40px;
}
```

**Guilherme:** Interessante! Vamos voltar para o nosso projeto e diminuir a tela para observarmos como fica. Assim reparamos que a disposição dela já vai mudando.

**Rafaela:** Antes nosso título e nosso parágrafo não quebravam para acompanhar a diminuição ou aumento da tela. Agora nós mudamos as medidas da tela e eles ocupam uma quantidade diferente de linhas para se espalharem melhor.

**Guilherme:** A única coisa que ainda está estranha, Rafa, são os links, que ainda estão bem esmagados. Eu queria também aproveitar para trocar o nome de "links" para algo melhor.

Eu fiquei pensando que esse nome de classe "apresentacao__links__link" nós podemos mudar.

**Rafaela:** Vamos sim. Qual nome você quer colocar?

**Guilherme:** Podemos mudar para "apresentacao__links__navegacao".

**Rafaela:** Como tem vários "links", eu não posso selecionar a parte do "link" para mudar de uma única vez.

**Guilherme:** Tem como pressionar o "Alt" e clicar após cada "link".

**Rafaela:** Vamos fazer isso, pressionar o botão de apagar quatro vezes para apagar o "link" e escrever "navegacao" no lugar. Então nossa classe virou `apresentacao__links__navegacao`.

Em seguida, precisamos trocar no CSS, então na linha 83 vamos mudar para `apresentacao__links__navegacao`.

**Guilherme:** Isso é comum, mudarmos para um nome melhor conforme evoluímos. É complexo escolher um bom nome de primeira.

E por enquanto não fizemos nenhuma alteração no projeto, certo?

**Rafaela:** Ainda não. Agora vamos mudar a `width` do nosso link, que ainda está fixa e por isso fica muito grande. Vamos testar com 50% também, lembrando que as porcentagens são sempre relativas ao link pai, não estamos deduzindo do nada.

```css
.apresentacao__links__navegacao {
    display: flex;
    justify-content: center;
    gap: 16px;
    border: 2px solid var(--cor-terciaria);
    width: 50%;
    text-align: center;
    border-radius: 8px;
    font-size: 1.5rem;
    font-weight: 600;
    padding: 21.5px 0;
    text-decoration: none;
    color: var(--cor-secundaria);
    font-family: var(--font-secundaria);
}
```

Quando voltamos para página do nosso portfólio, reparamos que os links também acompanham o aumento e a diminuição da tela conforme mudamos as medidas. Entretanto, tem um ponto que se diminuímos demais a tela, ele quebra, ou seja, o texto fica fora do contorno do botão.

**Guilherme:** Arrumamos uma coisa, mas ainda está estranho.

**Rafaela:** Sim, ainda teremos muitas coisas para fazer nesse projeto.

---

**Guilherme:** Agora temos um novo desafio.

Assim como no curso anterior que recebemos um Figma com uma nova página, porque nosso projeto está crescendo, temos um novo desafio, certo, Rafa, que é tornar nossa página...

**Rafaela:** **_Responsiva_**.

Responsividade significa termos no nosso projeto a capacidade da tela se adaptar dependendo do dispositivo que estivermos acessando. Então a página fica boa em um desktop, no notebook e até no celular.

**Guilherme:** A ideia no celular, na verdade, não é só deixar tudo esmagado.

**Rafaela:** Nós até estávamos fazendo isso e mesmo assim o design não estava bom.

**Guilherme:** A ideia no celular é que os elementos mudem de posição, deixando a imagem mais em cima, dispor os elementos em coluna e coisas do tipo. Pensando nisso, o que acontece no mundo real é que a pessoa que trabalha com o Figma e com design pensa nisso, e nós, devs do Front-end, implementamos o que foi pensado.

Então vamos mostrar para o pessoal, Rafa.

**Rafaela:** Usaremos o mesmo Figma que estávamos utilizando para fazer o _footer_ e a segunda página com o "Sobre mim". Na parte superior da coluna da esquerda, existem duas páginas: a **web**, que utilizamos para desenvolver o projeto até agora, e a página **mobile**. Na página mobile é onde temos o design para dispositivos móveis.

![Figma com o template da página para mobile. Na imagem há dois protótipos de tela, sendo a da esquerda o protótipo da tela inicial e à esquerda o da tela "Sobre mim". Na direita a barra de navegação está na parte centro-superior dos elementos já existentes dispostos em coluna na seguinte ordem: imagem, título, subtítulo, título dos links, botão do GitHub, botão do LinkedIn, botão da Twitch e barra de rodapé. Na tela da esquerda temos também o menu na parte centro-superior, seguido da foto, do título "Sobre mim", do texto e do rodapé.](https://cdn1.gnarususercontent.com.br/1/935581/293961b9-2160-4a92-a4cc-cd3da0964c1e.png)

**Guilherme:** Percebemos que o conteúdo é igual: os texto, os links e a imagem, mas a posição deles está diferente.

Eu falo tudo igual, mas a imagem talvez seja diferente, em outro tamanho, para a experiência da pessoa que vai navegar pelo celular fique melhor. Então temos um desafio, Rafa: implementar esse design de alguma forma.

Imagino que usaremos bastante o CSS, apesar de não saber ainda o código, mas imagino que teremos que informar que, ao estarmos em uma tela com determinado tamanho, a disposição dos elementos precisa mudar.

**Rafaela:** Será que para isso precisaremos criar outro HTML ou precisaremos criar vários arquivos CSS? O que precisaremos fazer nos nosso projeto?

**Guilherme:** Vamos descobrir.

[](https://cursos.alura.com.br/forum/curso-html-css-responsividade-publicacao-projetos/exercicio-figma-mobile/119279/novo)