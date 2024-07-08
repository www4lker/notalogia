---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/figma-do-nosso-projeto-com-atualizacoes/","tags":["css","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# figma do nosso projeto com atualizações

## criado em: 
-  03-04-2023 - 09:36

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/HTML e CSS 3\|HTML e CSS 3]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/criando ícones links\|criando ícones links]]
- tags: #css #ANELO 
- Fontes & Links: 

---

**Guilherme:** Iniciaremos um novo desafio: atualizar a nossa aplicação. No mundo real, geralmente desenvolvemos uma tela, assim como fizemos, e de repente precisamos atualizá-la, incluindo novas funcionalidades.

Sistemas de software, páginas Web e aplicações geralmente passam por atualizações.

**Rafaella:** Principalmente em momentos de alta nas vendas, como na Black Friday. Nestas datas, empresas de _e-commerce_ enviam _landing pages_ para que modifiquemos, adicionando chamadas de desconto. É bem comum recebermos no dia-a-dia pedidos de atualização de projetos.

**Guilherme:** Traremos acontecimentos do mundo real para esse curso. Não somos um _e-commerce_, mas temos uma atualização a ser implementada. O nosso projeto evoluirá um pouco mais: **_ele terá uma nova tela_**.

Vamos acessar o [Figma do nosso projeto em sua nova etapa](https://www.figma.com/file/NrzJacC887svMVfF9oC2jM/Portfolio-Projeto-2?node-id=0%3A1&t=PMVfvZa872DqgZIK-0).

![Tela atualizada do projeto no Figma. O fundo é preto. Na parte superior, temos dois textos em negrito na cor ciano: "Home" e "Sobre mim", dispostos na horizontal, da esquerda para a direita. Abaixo deles, temos dois blocos de conteúdo, lado a lado, centralizados. O bloco esquerdo possui um texto que se divide em duas partes: título e parágrafo. O título apresenta um texto em negrito dividido em duas cores: "Eleve seu negócio digital a outro nível" em branco, seguido de "com um Front-end de qualidade!" em ciano. O parágrafo está na cor branca, e exibe o texto de apresentação de Joana Santos. Abaixo do parágrafo temos subtítulo com o texto "Acesse minhas redes:", em negrito. Abaixo dele temos três botões pretos que possuem um contorno na cor ciano, dispostos na vertical: no botão superior temos o texto "Github" e à esquerda um ícone que representa esta aplicação. No botão do meio temos o texto texto "LinkedIn" acompanhado do ícone que representa esta aplicação, à esquerda. No botão inferior temos o texto "Twitch" e à esquerda o ícone representando esta aplicação. Já o bloco direito se constitui de uma fotografia em preto e branco representando Joana Santos, uma mulher desenvolvedora, sentada em frente a um notebook aberto. A fotografia também conta com um desenho em ciano de uma linha circulando Joana e seu notebook três vezes e terminando em uma estrela. Na parte inferior da tela, temos uma barra na cor ciano que se estende do canto esquerdo ao canto direito. Em seu interior há o texto "Desenvolvido por Alura", na cor preta.](https://cdn1.gnarususercontent.com.br/1/1319057/7ee7d76b-91d7-46dd-96da-b3e97e0f9613.png)

Temos botões com ícones em seu interior. O que visualmente chama mais a atenção, Rafa?

**Rafaella:** Os botões, definitivamente. Também temos o novo subtítulo "Acesse minhas redes", que antes eram completamente ciano. Agora eles possuem apenas uma borda nesta cor. Temos também ícones nos botões.

**Guilherme:** Estes elementos estão nas cores que estamos utilizando.

**Rafaella:** Exato.

**Guilherme:** Agora temos também na parte superior os menus "Home" e "Sobre mim".

**Rafaella:** Nós já desenvolvemos o `<header>`, agora vamos adicionar em seu interior todas as nossas _tags_ para criar o cabeçalho de fato. Nós o adicionamos e o deixamos vazio somente para entender onde ele deveria ficar.

**Guilherme:** O mesmo vale para o `<footer>` (ou "rodapé"). Onde está escrito "Desenvolvido por Alura", você pode adicionar seu nome.

Além dessa, temos uma página nova, que será acessada quando clicarmos no menu "Sobre mim".

![Tela "Sobre mim" do projeto no Figma. O fundo é preto. Na parte superior, temos dois textos em negrito na cor ciano: "Home" e "Sobre mim", dispostos na horizontal, da esquerda para a direita. Abaixo deles, temos dois blocos de conteúdo, lado a lado, centralizados. O bloco esquerdo possui um texto que se divide em duas partes: título e parágrafo. O título apresenta o texto "Sobre mim" em negrito e na cor branca. Os dois parágrafos estão um abaixo do outro, na cor branca, e exibem um texto "Lorem ipsum". Já o bloco direito se constitui de uma fotografia em preto e branco representando Joana Santos, uma mulher desenvolvedora, sentada em frente a um notebook aberto. A fotografia também conta com um desenho em ciano de uma linha circulando Joana e seu notebook três vezes e terminando em uma estrela. Na parte inferior da tela, temos uma barra na cor ciano que se estende do canto esquerdo ao canto direito. Em seu interior há o texto "Desenvolvido por Alura", na cor preta.](https://cdn1.gnarususercontent.com.br/1/1319057/49008f5f-f397-4f16-acae-6a621d1f20d5.png)

Nela, o cabeçalho e o rodapé continuam iguais. O que muda é o conteúdo principal, do meio da tela. Teremos a chance de criar uma biografia, onde poderemos escrever um pouco sobre nós. Por isso, o texto que incluímos no Figma e no curso é **_ilustrativo_**.

**Rafaella:** É importante salientar que, quando recebemos um design para trabalhar, é comum que haja nele esse tipo de texto chamado **_Lorem ipsum_**. Ele serve para nos mostrar como o texto final fica disposto na página, sem precisarmos acessar o texto verdadeiro, o qual às vezes nem foi produzido ainda.

**Guilherme:** Vamos comparar as duas páginas?

**Rafaella:** Vamos sim.

**Guilherme:** Os estilos das duas páginas são parecidos, utilizam os mesmos estilos.

**Rafaella:** Exatamente, a mudança está nas disposições e nos tamanhos do texto. A foto também é a mesma.

**Guilherme:** Com base no que já aprendemos, é possível deduzir os estilos de cada trecho: o "Sobre mim" seria um `<h1>`, e os blocos de biografia seriam dois blocos de parágrafo. Nós nos pegamos pensando se vamos utilizar um Flexbox na horizontal ou na vertical. Isso é muito comum. Com a prática, aos poucos, desenvolvemos esse tipo de percepção e passamos a aplicá-la em todas as páginas que vemos.

A seguir, começaremos a criar esta nova etapa do nosso projeto.