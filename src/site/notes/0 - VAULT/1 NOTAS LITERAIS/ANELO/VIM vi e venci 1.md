---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/vim-vi-e-venci-1/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# VIM vi e venci 1

## criado em: 
- 04-06-2024
- 19:53
## relacionados:
- notas:
1. [[0 - VAULT/1 NOTAS LITERAIS/ANELO/VIM, vi e venci\|VIM, vi e venci]]
2. [[0 - VAULT/1 NOTAS LITERAIS/ANELO/VIM CheatSheet\|VIM CheatSheet]]
3. [[0 - VAULT/2 NOTAS PERMANENTES/Cheatsheet do Vim e sua aplicabilidade no Obsidian\|Cheatsheet do Vim e sua aplicabilidade no Obsidian]]
- tags: #ANELO 
- Fontes & Links: 
---
O VIM (Vi IMproved) é uma versão melhorada do VI, mantendo a funcionalidade original, mas adicionando uma série de recursos e melhorias. É um dos editores de texto mais populares no mundo Linux e Unix, amplamente usado por desenvolvedores, administradores de sistemas e entusiastas de tecnologia. A principal diferença entre o VI e o VIM é que este último oferece uma experiência mais amigável e produtiva, além de suportar uma ampla gama de extensões e plugins.

Principais atrativos do VIM:

1. **Modo Visual**: O VIM adiciona um modo visual, que permite selecionar texto com mais facilidade, seja por caracteres, palavras ou linhas inteiras.

2. **Realce de Sintaxe**: O VIM possui suporte a realce de sintaxe para uma ampla variedade de linguagens de programação, facilitando a leitura e edição de código.

3. **Configurável**: É altamente configurável, permitindo que os usuários personalizem suas preferências e mapeiem teclas para atalhos personalizados.

4. **Divisão de Tela**: O VIM suporta a divisão de tela, permitindo a visualização de vários arquivos simultaneamente.

5. **Extensões (Plugins)**: A comunidade do VIM criou inúmeros plugins que estendem ainda mais suas funcionalidades, adicionando recursos como autocompletar, integração com sistemas de controle de versão, etc.

6. **Portabilidade**: O VIM está disponível em várias plataformas e sistemas operacionais, garantindo que a experiência seja consistente, independentemente do ambiente.

Cheat Sheet do VIM para Iniciantes:

1. **Abrir o VIM**:
   ```
   vim nome_do_arquivo
   ```

2. **Modos do VIM**:
   - **Modo Normal**: Pressione 'Esc' para entrar no Modo Normal.
   - **Modo de Inserção (Insert)**: Pressione 'i' para entrar no modo de inserção, onde você pode digitar e editar o texto.
   - **Modo Visual**: Pressione 'v' para entrar no modo visual, onde você pode selecionar texto com as setas.
   - **Modo de Comando (Command)**: Pressione ':' no Modo Normal para entrar no Modo de Comando e executar comandos.

3. **Navegação no Modo Normal**:
   - Movimentar para cima: 'k'
   - Movimentar para baixo: 'j'
   - Movimentar para a esquerda: 'h'
   - Movimentar para a direita: 'l'
   - Ir para o início da linha: '0' (zero)
   - Ir para o final da linha: '$'
   - Ir para uma linha específica: ':n', onde 'n' é o número da linha.

4. **Comandos de Edição**:
   - Apagar caractere: 'x'
   - Apagar palavra: 'dw'
   - Apagar até o final da linha: 'd$'
   - Apagar a linha inteira: 'dd'
   - Copiar linha: 'yy'
   - Colar após o cursor: 'p'
   - Substituir caractere sob o cursor: 'r' seguido do novo caractere

5. **Desfazer e Refazer**:
   - Desfazer: 'u'
   - Refazer: 'Ctrl + r'

6. **Buscar e Substituir**:
   - Buscar: '/' seguido da palavra a ser encontrada. Use 'n' para encontrar a próxima ocorrência.
   - Substituir: ':s/palavra_antiga/nova_palavra/g' para substituir todas as ocorrências na linha atual. Use ':%s/...' para substituir em todo o arquivo.

7. **Salvar e Sair**:
   - Salvar: ':w'
   - Salvar e Sair: ':wq' ou ':x'
   - Sair sem salvar: ':q!' ou ':q' se não houver alterações.

8. **Divisão de Tela**:
   - Dividir verticalmente: ':vsplit'
   - Dividir horizontalmente: ':split'
   - Alternar entre painéis: 'Ctrl + w' seguido de setas direcionais.

9. **Configurações Básicas**:
   - Habilitar realce de sintaxe: ':syntax on'
   - Habilitar número de linhas: ':set number'

O VIM é um editor poderoso, mas requer um pouco de prática para se acostumar com seus comandos e aproveitar ao máximo seus recursos. Conforme você ganha experiência, pode explorar sua ampla gama de extensões e personalizações para tornar sua experiência de edição ainda mais produtiva.