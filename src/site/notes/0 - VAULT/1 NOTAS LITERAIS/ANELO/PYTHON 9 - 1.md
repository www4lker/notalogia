---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-9-1/","tags":["python","linguagem-c","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON 9 - 1

## criado em: 
-  30-04-2023 - 17:32

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 9 - final\|PYTHON 9 - final]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/neofito da linguagem C\|neofito da linguagem C]]
- tags: #python #linguagem-c #ANELO 
- Fontes & Links: 

---

No curso [**C I: Introdução à Linguagem das Linguagens**](https://cursos.alura.com.br/course/introducao-a-programacao-com-c-parte-1) também é implementado um jogo de adivinhação, você pode baixá-lo [aqui](https://s3.amazonaws.com/caelum-online-public/python3/files/adivinhacao.c) e deixe-o na mesma pasta que os arquivos Python, ou seja, na pasta **jogos**. O que faremos nesse vídeo é comparar o Python com C, mas sem explicá-lo, a ideia é só enfatizar algumas diferenças entre eles.

A primeira diferença que vemos é que no C precisamos importar mais bibliotecas, isso porque algumas funções no C não são _built-in_, como a de imprimir (**`printf`**) e a de capturar entrada do usuário (**`scanf`**), por isso para utilizá-las é necessário importar algumas bibliotecas.

Outra diferença é que no C somos obrigados a definir a função **`main`**, que é considerada o início de qualquer programa, sem ela nada vai funcionar. Ao contrário do Python, já que nós só criamos a função **`jogar()`** quando precisamos importar o arquivo em outro, mas antes nós conseguíamos executar diretamente o jogo sem problemas.

No capítulo 1 falamos sobre tipagem de variáveis, e o C é uma linguagem que possui a **tipagem estática**, ou seja, quando declaramos uma variável, precisamos dizer qual será o tipo dela e esse tipo nunca mudará. O Python, como já sabemos, é uma linguagem que possui a **tipagem dinâmica**, já que o tipo da variável varia de acordo com o valor que ela recebe, por isso que em Python não podemos declarar variáveis vazias, só definindo o seu nome, porque se não atribuirmos um valor a uma variável, o Python não saberá o seu tipo.

O resto do código é bem parecido, com algumas diferenças de sintaxe e nomenclatura, como por exemplo a sintaxe dos blocos, para definir um bloco no C devemos colocá-lo entre chaves e a indentação não é obrigatório, apesar de todos os desenvolvedores utilizarem por conta da formatação do código, já no Python só precisamos colocar os dois pontos e indentar o código do bloco; o C também te obriga a colocar ponto e vírgula ao final das instruções.

Essas foram algumas das diferenças que podemos citar comparando os dois códigos. Agora veremos na hora da execução, mas no próximo vídeo :)