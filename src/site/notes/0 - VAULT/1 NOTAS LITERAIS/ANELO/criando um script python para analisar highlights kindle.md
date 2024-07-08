---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/criando-um-script-python-para-analisar-highlights-kindle/","tags":["meta","promptGPT","ANELO","python"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# prompt analises

## criado em: 
- 13-06-2024
- 16:32
## relacionados:
- notas:
1. [[0 - VAULT/2 NOTAS PERMANENTES/zettelkasten\|zettelkasten]]
2. [[0 - VAULT/2 NOTAS PERMANENTES/identificando fontes mais comuns\|identificando fontes mais comuns]]
3. [[0 - VAULT/1 NOTAS LITERAIS/meta notas/meta-prompt Article to notes\|meta-prompt Article to notes]]
- tags: #meta #promptGPT #ANELO #python 
---
## iteração 1

**Vamos criar um script python para criar um csv.**
Ele se baseará em um arquivo txt feito quando leio no kindle.
Tenha em mente que um destque feito no kindle, quando renderizado como txt possui algumas caracteristicas:

1. **Barra Separadora**:
   - **Campo**: `separator`
   - **Tipo**: String
   - **Descrição**: Uma sequência de caracteres usada para separar cada destaque ou nota.

2. **Título do Livro**:
   - **Campo**: `book_title`
   - **Tipo**: String
   - **Descrição**: O título do livro do qual o destaque ou nota foi feito.

3. **Autor do Livro**:
   - **Campo**: `author_name`
   - **Tipo**: String
   - **Descrição**: O nome do autor do livro.

4. **Tipo de Anotação**:
   - **Campo**: `annotation_type`
   - **Tipo**: String (com valores possíveis como `highlight`, `note`, `bookmark`)
   - **Descrição**: O tipo da anotação feita (destaque, nota pessoal ou marcador).

5. **Localização**:
   - **Campo**: `location`
   - **Tipo**: String ou Struct (contendo `page_number` e `position_number`)
   - **Descrição**: A localização exata do destaque ou nota no livro, podendo ser detalhada em número da página e/ou posição.

6. **Conteúdo**:
   - **Campo**: `content`
   - **Tipo**: String
   - **Descrição**: O texto real que foi destacado ou a nota pessoal que foi escrita.

7. **Data e Hora de Adição**:
   - **Campo**: `timestamp`
   - **Tipo**: DateTime
   - **Descrição**: A data e a hora em que o destaque ou a nota foram adicionados, seguindo o formato `dddd, dd de MMMM de yyyy HH:mm:ss`.

---
## iteração 2

**Vamos criar um script python para criar um csv.**
Ele se baseará em um arquivo txt feito quando leio no kindle.
Tenha em mente que um destque feito no kindle, quando renderizado como txt possui algumas caracteristicas:

1. **Barra Separadora**:
   - **Campo**: `separator`
   - **Tipo**: String
   - **Descrição**: Uma sequência de caracteres usada para separar cada destaque ou nota.

2. **Título do Livro**:
   - **Campo**: `book_title`
   - **Tipo**: String
   - **Descrição**: O título do livro do qual o destaque ou nota foi feito.

3. **Autor do Livro**:
   - **Campo**: `author_name`
   - **Tipo**: String
   - **Descrição**: O nome do autor do livro.

4. **Tipo de Anotação**:
   - **Campo**: `annotation_type`
   - **Tipo**: String (com valores possíveis como `highlight`, `note`, `bookmark`)
   - **Descrição**: O tipo da anotação feita (destaque, nota pessoal ou marcador).

5. **Localização**:
   - **Campo**: `location`
   - **Tipo**: String ou Struct (contendo `page_number` e `position_number`)
   - **Descrição**: A localização exata do destaque ou nota no livro, podendo ser detalhada em número da página e/ou posição.

6. **Conteúdo**:
   - **Campo**: `content`
   - **Tipo**: String
   - **Descrição**: O texto real que foi destacado ou a nota pessoal que foi escrita.

7. **Data e Hora de Adição**:
   - **Campo**: `timestamp`
   - **Tipo**: DateTime
   - **Descrição**: A data e a hora em que o destaque ou a nota foram adicionados, seguindo o formato `dddd, dd de MMMM de yyyy HH:mm:ss`.

Vou colocar uns exemplos:
```
"Seu destaque"

==========
zettelkasten guide (walker de barros dantas)
- Seu destaque ou posição 283-284 | Adicionado: terça-feira, 5 de julho de 2022 11:43:46

As a rule of thumb, you should always make something from the information you process. You should always translate information to knowledge by adding context and relevance
==========

"Sua nota"

==========
Diário Estoico: 366 Lições Sobre Sabedoria, Perseverança e a Arte de Viver (Holiday, Ryan)
- Sua nota na página 333 | posição 2640 | Adicionado: segunda-feira, 11 de julho de 2022 15:36:04

O mesmo vale para o consumismo - nao deveria me preocupar em adquirir uma versao melhor de mikm mesmo?
==========

"Seu marcador"

==========
How to Take Smart Notes: One Simple Technique to Boost Writing, Learning and Thinking (Ahrens, Sönke)
- Seu marcador na página 70 | posição 890 | Adicionado: domingo, 24 de julho de 2022 11:04:35


==========
```


AGORA: desejo que voce crie esse script que pegue esses dados em txt e crie uma série de arquivos csv - uma para cada ano - onde as principais caracteristicas das otas sejam organizadas em colunas - titulo do livro, autor, conteúdo, data e hora e tipo de anotação. Dados como localização e tipo de anotação "Seu marcador" podem ser desprezados, e o tipo de anotação "Sua Nota" tem um peso maior, seguido da nota tipo "Seu Destaque".

