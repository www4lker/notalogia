---
{"dg-publish":true,"permalink":"/0-vault/2-notas-permanentes/cheatsheet-do-vim-e-sua-aplicabilidade-no-obsidian/","tags":["permanente","vim","TIPS","massacritica","meta","zettelkasten","escrivão","produtividades","markdown","edicaodetexto","productivity","gerenciamentodeanotações","notasintercon"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Cheatsheet do Vim e sua aplicabilidade no Obsidian

## criado em: 
- 05-09-2023
- 01:45
## relacionados:
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/VIM vi e venci\|VIM vi e venci]]
- [[0 - VAULT/2 NOTAS PERMANENTES/obsidian\|obsidian]]
- tags: #vim #TIPS #massacritica #meta #zettelkasten #escrivão #produtividades #markdown #edicaodetexto #productivity #gerenciamentodeanotações #notasintercon

---

>O Vim é um editor de texto baseado em linha de comando que oferece um conjunto único de comandos e atalhos, enquanto o Obsidian é uma ferramenta para criação e gerenciamento de anotações interconectadas em Markdown. Há uma sinergia entre os dois, já que as habilidades do Vim podem ser aplicadas no Obsidian para otimizar a edição. O Vim apresenta quatro modos principais (Normal, Insert, Visual e Command-Line) que permitem navegação, inserção de texto, seleção de blocos de texto e execução de comandos respectivamente. No modo Normal, por exemplo, você pode mover o cursor, ir para o início ou fim da palavra ou linha, entrar no modo de inserção antes ou depois do cursor, excluir caracteres ou linhas inteiras, copiar linhas e colar antes ou depois do cursor. 

## Cheatsheet do Vim e sua aplicabilidade no Obsidian

O Vim é um poderoso editor de texto baseado em linha de comando que possui um conjunto único de comandos e atalhos. Ele pode ser altamente eficiente uma vez que você domina seus conceitos. O Obsidian é um editor de anotações baseado em Markdown que permite criar e gerenciar anotações interconectadas. Embora sejam ferramentas diferentes, algumas habilidades do Vim podem ser aplicadas no Obsidian para melhorar a eficiência de edição.

## Modos do Vim:
- **Normal Mode**: O modo padrão que permite navegar e executar comandos.
- **Insert Mode**: Modo de inserção de texto.
- **Visual Mode**: Selecionar blocos de texto.
- **Command-Line Mode**: Executar comandos do Vim.

## Navegação e Edição Básica (Normal Mode):
- **h/j/k/l**: Mover o cursor para a esquerda/baixo/cima/direita.
- **w**: Ir para o início da próxima palavra.
- **e**: Ir para o final da próxima palavra.
- **b**: Voltar para o início da palavra anterior.
- **0**: Ir para o início da linha.
- **$**: Ir para o final da linha.
- **A**: Ir para o final da linha e entrar no modo de inserção.
- **i**: Entrar no modo de inserção antes do cursor.
- **o**: Inserir uma nova linha abaixo e entrar no modo de inserção.
- **O**: Inserir uma nova linha acima e entrar no modo de inserção.
- **x**: Excluir caractere sob o cursor.
- **dd**: Excluir linha inteira.
- **yy**: Copiar linha.
- **p**: Colar após o cursor.
- **P**: Colar antes do cursor.
- **u**: Desfazer ação.
- **Ctrl + r**: Refazer ação.

## Edição Avançada (Normal Mode):
- **c**: Mudar (alterar) o texto.
  - Exemplo: `cw` muda a palavra atual.
- **d**: Excluir texto.
  - Exemplo: `dw` exclui a palavra atual.
- **y**: Copiar texto.
  - Exemplo: `yw` copia a palavra atual.
- **v**: Entrar no modo Visual para selecionar texto.

## Busca e Substituição (Normal Mode):
- **/texto**: Pesquisar por "texto".
- **n**: Ir para a próxima ocorrência da busca.
- **N**: Ir para a ocorrência anterior da busca.
- **:%s/antigo/novo/g**: Substituir "antigo" por "novo" em todo o documento.
- **:%s/antigo/novo/gc**: Substituir com confirmação.

## Aplicabilidade no Obsidian:
- Use os modos de navegação para percorrer rapidamente as anotações no modo de pré-visualização.
- Aplique os comandos de edição para formatar o texto em Markdown de maneira eficiente.
- Use a busca para encontrar rapidamente palavras-chave em suas anotações extensas.
- Aplique os comandos de cópia/colagem para reorganizar e duplicar blocos de texto.
- Aplique os conceitos de mudança (alteração), exclusão e cópia para refinar o conteúdo das anotações.

Lembrando que o Obsidian tem sua própria interface e recursos, mas a familiaridade com os conceitos do Vim pode melhorar sua produtividade ao trabalhar com anotações no editor.