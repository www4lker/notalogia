---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/vim-vi-e-venci/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Sem título

## criado em: 
-  03-08-2023 - 11:08

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Linux - 101\|Linux - 101]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/VIM vi e venci 1\|VIM vi e venci 1]]
- tags: #ANELO 
- Fontes & Links: 

---

Cheat Sheet do VI no Terminal Linux:

O VI é um editor de texto poderoso disponível em sistemas Linux e Unix. Embora possa ser um pouco intimidante no início, dominar seus comandos essenciais é uma habilidade útil para edição de arquivos no terminal. Aqui está um cheat sheet para ajudar você a começar:

1. Abrir o VI:
   ```
   vi nome_do_arquivo
   ```

2. Modos do VI:
   - **Modo Normal**: Modo padrão ao abrir o VI. Pressione a tecla 'Esc' para voltar a esse modo.
   - **Modo de Inserção (Insert)**: Pressione 'i' para entrar no modo de inserção, onde você pode digitar e editar o texto.
   - **Modo de Inserção no Fim da Linha (Append)**: Pressione 'a' para entrar no modo de inserção no final da linha.
   - **Modo de Inserção no Próximo Caractere (Insert After)**: Pressione 'A' para entrar no modo de inserção após o cursor.

3. Navegação no Modo Normal:
   - **Movimentar para cima**: 'k'
   - **Movimentar para baixo**: 'j'
   - **Movimentar para a esquerda**: 'h'
   - **Movimentar para a direita**: 'l'
   - **Ir para o início da linha**: '0' (zero)
   - **Ir para o final da linha**: '$'

4. Comandos de Edição:
   - **Apagar caractere**: 'x'
   - **Apagar palavra**: 'dw'
   - **Apagar até o final da linha**: 'd$'
   - **Apagar a linha inteira**: 'dd'
   - **Copiar linha**: 'yy'
   - **Colar após o cursor**: 'p'
   - **Substituir caractere sob o cursor**: 'r' seguido do novo caractere

5. Desfazer e Refazer:
   - **Desfazer**: Pressione 'u' para desfazer a última alteração.
   - **Refazer**: Pressione 'Ctrl + r' para refazer a última alteração desfeita.

6. Buscar e Substituir:
   - **Buscar**: Pressione '/' para iniciar a busca e digite a palavra a ser encontrada. Use 'n' para encontrar a próxima ocorrência.
   - **Substituir**: Para substituir todas as ocorrências de uma palavra, entre no Modo Normal e use o comando `:%s/palavra_antiga/nova_palavra/g`.

7. Salvar e Sair:
   - **Salvar**: No Modo Normal, pressione ':w' e tecle 'Enter'.
   - **Salvar e Sair**: No Modo Normal, pressione ':wq' e tecle 'Enter'.
   - **Sair sem salvar**: No Modo Normal, pressione ':q!' e tecle 'Enter'.

8. Dicas Adicionais:
   - **Números de Linha**: Pressione ':' e digite o número da linha para ir diretamente para ela.
   - **Alternar para o Modo Normal**: Pressione 'Esc' a qualquer momento.

Lembre-se de que o VI tem uma curva de aprendizado, e a prática é fundamental para se tornar mais confortável com esse editor de texto. Com o tempo, você descobrirá seu poder e eficiência para editar arquivos no terminal.