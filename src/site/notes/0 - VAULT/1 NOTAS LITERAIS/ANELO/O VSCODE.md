---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/o-vscode/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# O VSCODE

## criado em: 
-  30-03-2023 - 11:46

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/HTML e CSS 1\|HTML e CSS 1]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/documentação HTML\|documentação HTML]]
- tags: #ANELO 
- Fontes & Links: 

---

**Guilherme:** Olá! Meu nome é Guilherme Lima.

**Rafaella:** E eu sou Rafaella Ballerini.

**Guilherme:** Estamos muito felizes em te acompanhar no curso **HTML e CSS: Desenvolvendo uma página**.

**Rafaella:** Afinal, o que é HTML? O que é CSS? São linguagens de programação? Como conseguimos transformar esses códigos em uma página web?

**Guilherme:** Aprenderemos do zero a:

-   utilizar páginas HTML;
-   onde escrever nossos arquivos HTML e CSS;
-   para que servem essas duas linguagens.

Este curso é indicado para pessoas que **_nunca utilizaram HTML e CSS_** na vida. Se você se encaixa nessa descrição, te convidamos para mergulhar juntos!

HTML e CSS com Gui Lima e Rafa Ballerini aqui na Alura!

---

**Rafaella:** Antes de começar a codar, criaremos um arquivo com outro tipo de extensão, a qual estamos mais acostumados, para entendermos como este arquivo é criado. A primeira etapa será abrir um editor de texto — pode ser o Docs do Google, o Word ou mesmo um bloco de notas. Vamos escrever neste documento.

**Guilherme:** A ideia é entender que a criação de um código HTML ou CSS é similar à criação de um documento de texto. A diferença é que, no arquivo do Docs, existem elementos que nos auxiliam nessa criação.

**Rafaella:** Exato, elementos visuais.

**Guilherme:** Até de interface. Todo texto que lemos — como por exemplo um livro — possui um título. Vamos criar um título?

**Rafaella:** Sim. Se abrirmos o Docs do Google, veremos no topo da página uma barra de menus. Abaixo do menu "Formatar" temos uma lista de submenus de estilo que nos permite modificar automaticamente a configuração da fonte, sem precisar realizar modificações manualmente. Vamos abrir esse submenu e selecionar a opção "Título". No corpo do documento escreveremos "Isso é um título".

**Guilherme:** Temos um título. Pressionaremos "Enter" no final dessa linha e veremos que o tamanho do nosso cursor diminuiu. Na nova linha, o documento espera o formato "parágrafo", que consiste em um texto menor.

**Rafaella:** Este formato "parágrafo" é o padrão do Docs do Google. Nessa linha escreveremos "isso é um parágrafo". Podemos ver como é diferente a formatação entre o título e o parágrafo.

**Guilherme:** Este exemplo parece muito simples, mas explicaremos a ideia posteriormente. Os livros, geralmente, possuem imagens. Vamos acrescentar uma imagem do HTML 5?

**Rafaella:** Vamos. Buscaremos no google por "html 5" e clicaremos na aba "Imagens", na qual salvaremos uma imagem da logo do HTML 5. O nome do arquivo será html 5. Retornaremos ao Docs do Google, abriremos a nossa imagem e a arrastaremos para o documento que estamos editando.

**Guilherme:** Foram criados um título, um parágrafo e uma imagem. Você não deve estar entendendo nada. Contudo, a ideia é a seguinte: definimos que o título é um título clicando nos estilos e aplicando-os ao texto. No HTML fazemos algo parecido, porém sem clicar em menus.

**Rafaella:** Exatamente. As nossas páginas web também utilizam títulos, assim como os livros. Por exemplo, quando entramos em páginas de notícias percebemos um título grande, vários parágrafos com notícias e imagens embutidas. Precisamos pensar como uma página web funciona. Ela também possui esses elementos. Entretanto, para desenvolvermos um HTML não temos menus de estilização prontos, em vez disso utilizaremos códigos.

No caso do HTML, utilizaremos as **_tags_**. Elas serão responsáveis por informar quais trechos serão títulos, por exemplo.

**Guilherme:** Boa. Precisamos aprender todas as _tags_ de uma só vez?

**Rafaella:** Não.

**Guilherme:** Não façam isso, por favor.

**Rafaella:** É uma questão de prática. Devemos analisar o que se encaixa melhor em cada contexto. Não adianta simplesmente decorar.

**Guilherme:** É isso aí. Vamos prestar atenção em um detalhe interessante, que é a **_extensão_**. Vamos dar um nome para esse documento?

**Rafaella:** Vamos. O nome será "Exemplo".

**Guilherme:** Baixaremos este arquivo. Quando clicamos no menu "Arquivo" localizado na barra de menus, uma lista de submenus é exibida. Selecionaremos o submenu "Fazer download" e nele veremos uma lista com vários tipos de extensão. Elas são formas com as quais esse arquivo será representado, ou seja, como ele vai funcionar. Pode ser um arquivo DOCX, um PDF, um TXT, e até mesmo um HTML compactado!

Podemos codar a partir de um editor de texto como o Docs Google ou o Word?

**Rafaella:** Não recomendamos.

**Guilherme:** Não conhecemos ninguém que faz isso.

**Rafaella:** Como pessoas desenvolvedoras, utilizamos na prática ferramentas específicas para essas tecnologias: os **_editores de código_**, algo como ambientes ou IDEs.

Neste curso utilizaremos um editor muito bom para códigos HTML e CSS: o **_Visual Studio Code_**, ou _VS Code_.

**Guilherme:** A seguir, aprenderemos como baixar e instalar o VS Code na nossa máquina para criarmos nosso arquivo HTML e desenvolver as nossas páginas.

---

## # Preparando o ambiente


No curso, usaremos uma ferramenta chamada [Visual Studio Code](https://code.visualstudio.com/), que é um editor de código desenvolvido pela Microsoft para Windows, Linux e macOS. Caso queira acompanhar os instrutores com as mesmas configurações, reserve um tempinho para a instalação do mesmo.

Para baixar o VSCODE, você pode procurar no Google por Visual Studio Code e clicar no primeiro link que aparece:

![Tela do Google com o resultado da busca sobre Visual Studio Code](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula1-img1.png)

Se o seu sistema operacional for Windows você pode clicar para baixar no botão **Download for Windows**:

![Tela da página de download do Visual Studio Code](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula1-img2.png)

Senão você pode clicar logo abaixo em [other platforms](https://code.visualstudio.com/#alt-downloads) que irá abrir uma página com opção de download para **Linux** e **macOS** também:

![Tela da página de download do Visual Studio Code com foco em other platforms](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula1-img3.png)

![Tela da página de download do Visual Studio Code para Linux e macOS](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula1-img4.png)

Se o seu sistema operacional for o Windows 8, 10 ou 11, siga os seguintes passos para instalação:

![Tela da página de download do Visual Studio Code mostrando a opção do Windows destacada](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula1-img9.png)

Após clicar na opção de baixar para Windows, o instalador do Visual Studio Code vai para a pasta de Downloads do seu computador. Acesse a pasta, localize o arquivo de instalação, clique com o botão direito sobre ele e “Execute como administrador”.

![Tela da pasta que contém o arquivo de instalação do Visual Studio Code, na qual mostra destacada a opção de Executar como administrador, que aparece após clicar com o botão direito do mouse sobre o arquivo, para iniciar a instalação](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula1-img10.png)

Após aceitar as permissões do Windows para a instalação, o instalador será iniciado e nessa etapa você deve aceitar o acordo de licença para poder prosseguir.

![Tela inicial do instalador que requer marcar a opção de Eu aceito o acordo antes de poder prosseguir com o botão Próximo destacado no canto inferior direito](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula1-img11.png)

A próxima tela é para você selecionar o local de destino, ou seja, onde o Visual Studio Code será instalado no seu computador. Caso prefira, pode deixar como está sem alterar nada e clique em “Próximo”. Antes de prosseguir com a instalação, é importante lembrar que para poder instalar o Visual Studio Code o seu computador tem que ter o espaço necessário livre.

![Tela do instalador para selecionar o local de destino onde o editor será instalado.](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula1-img12.png)

A tela seguinte serve apenas para você decidir se o Windows criará ou não uma pasta do Visual Studio Code no Menu Iniciar, ou seja, no menu que encontramos quando clicamos no símbolo do Windows na barra de tarefas do computador ou até mesmo no nosso teclado. Você pode renomear a pasta se quiser e prosseguir.

![Tela do instalador para selecionar se será criada ou não a pasta do menu iniciar do Windows, bem como o nome dessa pasta caso ela seja criada.](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula1-img13.png)

Essa próxima etapa é a seleção de tarefas adicionais que o Visual Studio Code será responsável ou capaz de fazer em seu computador. Recomendamos que marque todas as opções para poder desfrutar das diversas funcionalidades da ferramenta.

![Tela do instalador para selecionar as tarefas adicionais que o Visual Studio Code será capaz de realizar.](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula1-img14.png)

Pronto, chegamos no final da configuração de instalação e agora podemos clicar na opção “Instalar” para executar a última etapa do processo, a instalação de fato.

![Tela do instalador que exibe as configurações de instalação que selecionamos e dá a opção de Instalar de fato o editor.](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula1-img15.png)

Na próxima tela podemos ver o progresso da instalação, ou seja, da extração dos arquivos baixados para a pasta de destino que selecionamos. Após a barra de extração se completar, podemos prosseguir para a última tela.

![Tela do instalador que mostra visualmente o progresso da instalação.](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula1-img16.png)

Chegamos na última tela, essa é apenas para informar se o Visual Studio Code foi instalado com sucesso. Você pode marcar a opção “Iniciar o Visual Studio Code” para abri-lo após o fechamento do instalador. Finalmente, ao clicar em “Concluir” o instalador será fechado e todo o processo finalizado. A partir disso você pode usar o VSCode normalmente.

![Tela final do instalador que exibe o sucesso da instalação](https://caelum-online-public.s3.amazonaws.com/2808-html-css-ambiente-arquivos-tags/aula1-img17.png)

Caso seu ambiente não seja Windows e tenha dúvidas durante a instalação ou no decorrer do curso, pode contar conosco criando um tópico no fórum ou interagindo no nosso servidor do [servidor do Discord](https://discord.gg/QeBdgAjXnn). Também não deixe de ajudar outros colegas. Vamos construir juntos essa grande comunidade da Alura? :)