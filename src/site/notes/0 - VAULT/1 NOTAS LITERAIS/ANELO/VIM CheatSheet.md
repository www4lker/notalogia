---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/vim-cheat-sheet/","tags":["vim","tips","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# VIM CheatSheet

## criado em: 
-  07-04-2023 - 15:49

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/VIM, vi e venci\|VIM, vi e venci]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/curso de VIM na Alura\|curso de VIM na Alura]]
- tags: #vim #tips #ANELO 
- Fontes & Links: 

---

Editor VIM - Cheatsheet para Iniciantes

1.  Modos do VIM:

-   Normal: navegação e manipulação do texto
-   Insert: inserção de texto
-   Visual: seleção de texto
-   Command-line: execução de comandos e configurações

2.  Como entrar nos modos:

-   Normal: sempre que você abrir o VIM, estará neste modo
-   Insert: pressione 'i' (inserir antes do cursor), 'a' (inserir após o cursor) ou 'o' (inserir nova linha abaixo)
-   Visual: pressione 'v' (visual), 'V' (visual linha) ou 'ctrl+v' (visual bloco)
-   Command-line: pressione ':' (comandos), '/' (pesquisa) ou '?' (pesquisa reversa)

3.  Navegação básica (modo Normal):

-   h: mover para a esquerda
-   j: mover para baixo
-   k: mover para cima
-   l: mover para a direita
-   w: mover para o início da próxima palavra
-   b: mover para o início da palavra anterior
-   0: mover para o início da linha
-   $: mover para o final da linha
-   gg: mover para o início do arquivo
-   G: mover para o final do arquivo

4.  Copiar, colar e recortar (modo Normal):

-   y: copiar (yank) a seleção
-   p: colar (paste) após o cursor
-   P: colar (paste) antes do cursor
-   d: recortar (delete) a seleção
-   dd: recortar (delete) a linha inteira
-   D: recortar (delete) do cursor até o final da linha

5.  Desfazer e refazer (modo Normal):

-   u: desfazer (undo) a última ação
-   ctrl+r: refazer (redo) a última ação desfeita

6.  Pesquisa (modo Command-line):

-   /<termo>: pesquisar pelo termo
-   n: próximo resultado
-   N: resultado anterior

7.  Salvar e sair (modo Command-line):

-   :w: salvar (write) o arquivo
-   :q: sair (quit) do VIM
-   :wq ou :x: salvar e sair
-   :q!: sair sem salvar (force quit)

8.  Configurações básicas (modo Command-line):

-   :set number: mostrar número das linhas
-   :syntax on: ativar realce de sintaxe
-   :set tabstop=4: definir tamanho do tab para 4 espaços
-   :set shiftwidth=4: definir tamanho do recuo para 4 espaços
-   :set expandtab: converter tabs em espaços

9.  Outros comandos úteis (modo Command-line):

-   :help <comando>: obter ajuda sobre um comando específico
-   :split <arquivo>: abrir arquivo em uma janela dividida horizontalmente
-   :vsplit <arquivo>: abrir arquivo em uma janela dividida verticalmente
-   :buffers: listar todos os arquivos abertos
-   :b <n>: alternar para o arquivo de número 'n' na lista de buffers
-   :e <caminho/arquivo>: abrir arquivo para edição

Lembre-se de que o VIM é altamente personalizável e possui muitos outros recursos. Essas são apenas algumas das funcionalidades básicas para ajudá-lo a começar

---


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/0-vault/1-notas-literais/anelo/vim-vi-e-venci/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




# VIM, vi e venci
## Por que usar o vim para programar?

## criado em: 
-  07-04-2023 - 15:30

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/curso de VIM na Alura\|curso de VIM na Alura]]
- tags: #vim #ide #teoria #TIPS #ANELO 
- Fontes & Links: https://www.alura.com.br/artigos/comandos-basicos-ao-utilizar-o-vim
- https://cursos.alura.com.br/course/vim

---

Há várias razões pelas quais programadores preferem usar o Vim como editor de texto para programação. Algumas delas incluem:

1.  Eficiência: O Vim é projetado para maximizar a eficiência do usuário, permitindo que o programador realize muitas tarefas rapidamente sem precisar usar o mouse ou teclas de atalho complexas.
    
2.  Personalização: O Vim é altamente personalizável, permitindo que os programadores ajustem as configurações para atender às suas necessidades específicas de programação.
    
3.  Disponibilidade: O Vim está disponível em muitas plataformas, incluindo sistemas operacionais Unix, Linux e Windows, o que o torna uma escolha popular para programadores que trabalham em diferentes ambientes de computação.
    
4.  Poder: O Vim é um editor poderoso que oferece recursos avançados, como navegação rápida, busca e substituição avançadas, edição de colunas, macros e muitos outros.
    
5.  Comunidade: O Vim tem uma grande comunidade de usuários e desenvolvedores que contribuem com plugins e extensões para estender suas capacidades e resolver problemas específicos de programação.
    

No entanto, é importante lembrar que o Vim tem uma curva de aprendizado íngreme e pode levar algum tempo para se familiarizar com seus comandos e recursos avançados.

---

Aprender Vim pode ser um processo desafiador, mas com dedicação e prática é possível dominar o editor e aproveitar seus recursos avançados. Algumas dicas para atenuar a curva de aprendizado do Vim incluem:

1.  Comece pelo básico: O Vim possui muitos recursos avançados, mas é importante começar pelo básico, como navegação no arquivo, edição de texto e gravação de macros.
    
2.  Use tutoriais e cursos: Há muitos tutoriais e cursos on-line que podem ajudar a aprender Vim. Alguns exemplos são o Vimtutor, que é um tutorial interativo integrado ao editor, e o Vim Adventures, um jogo que ensina os comandos do Vim.
    
3.  Personalize o Vim: Personalizar o Vim pode ajudar a tornar o editor mais amigável e adequado às suas necessidades. É possível personalizar a aparência, atalhos e até mesmo adicionar plugins para aumentar as funcionalidades.
    
4.  Pratique: A prática é essencial para aprender Vim. Comece com pequenos projetos e tente usar o editor sempre que possível. Com o tempo, o uso do Vim se tornará mais natural e eficiente.
    
5.  Use cheatsheets: Existem muitos cheatsheets disponíveis on-line que listam os principais comandos do Vim. Imprima ou mantenha um em sua área de trabalho para ajudá-lo a lembrar dos comandos e suas funcionalidades.
    
6.  Use plugins: O Vim tem uma comunidade ativa que desenvolve plugins para adicionar novas funcionalidades ao editor. Use-os para facilitar o trabalho em tarefas específicas.
    
7.  Não desista: Aprender Vim pode ser frustrante às vezes, mas não desista. Com dedicação e prática, você pode dominar esse editor poderoso e aumentar sua produtividade no desenvolvimento de software.

</div></div>

