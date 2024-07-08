---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/java-script-e-html-pratique-logica-com-desenhos-animacoes-e-um-jogo/","tags":["javascript","HTML","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# JavaScript e HTML - pratique lógica com desenhos, animações e um jogo

## criado em: 
-  28-03-2023 - 13:27

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/JS e HTML - LOGICA DE PROGRAMAÇÃO\|JS e HTML - LOGICA DE PROGRAMAÇÃO]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/nossa primeira obra de arte\|nossa primeira obra de arte]]
- tags: #javascript #HTML #ANELO 
- Fontes & Links: https://cursos.alura.com.br/course/logica-programacao-pratica-com-desenho-animacoes-em-jogo/task/21876
---

Nosso primeiro passo nesta aula será criarmos nosso `programa.html`.

Abriremos nosso editor de texto e salvaremos o arquivo em nossa área de trabalho, com o nome `programa.html`.

> Aqui estamos utilizando o Sublime 2, mas você pode utilizar qualquer editor de sua preferência.

Lembrando que, no curso anterior de Lógica de Programação, vimos que quando queremos escrever um código em JavaScript utilizamos as tags `<meta charset=UTF-8">` e a `<script>` para podermos escrever nosso código.

Conforme vimos, tudo que está dentro da tag `<script>` pertence ao mundo JavaScript, e tudo que está fora - seja antes ou depois -, pertence ao mundo HTML.

Aprendemos no mundo JavaScript, a utilizar funções do mundo HTML por meio do `document`, por exemplo o `document.write()` que nos permite imprimir algo:

```xml
<meta charset="UTF-8">

<script>

document.write("");

</script>
```

Podemos, por exemplo, escrever a mensagem "Oi":

```xml
<meta charset="UTF-8">

<script>

document.write("<h1>Oi</h1>");

</script>
```

Salvaremos o programa e retornaremos ao navegador. Nele, escolheremos a opção de abrir arquivo, e selecionaremos o `programa.html`, assim, temos a seguinte exibição:

```undefined
Oi
```

Entretanto, nosso objetivo não é escrever HTML no mundo HTML, em vez disso, queremos desenhar. Sendo assim, não utilizaremos o `document.write()`.

Para desenhar precisamos: de uma tela e de um pincel.

Vamos acessar a página do [Google](http://www.google.com.br) e digitar "_empty canvas_". A palavra "_empty_" significa "vazio", em Português.

Observando os resultados, vemos que são exibidas imagens de telas em branco. Os mundos HTML e JavaScript utilizam o Inglês, por isso, as tags estão neste idioma, "_canvas_" também é uma tag do mundo HTML.

Se inserirmos em nosso código a tag `<canvas>`, ela é válida do mundo HTML e tem a mesma finalidade de uma tela em branco, ou seja, uma área em que podemos desenhar.

Como vamos trabalhar com desenhos, não iremos utilizar textos, não será necessária a inclusão da tag `<meta charset="UTF-8">`, que serve para resolvermos problemas de acentuação.

Assim, temos o mínimo para podermos começar a programar:

```xml
<canvas></canvas>

<script>

</script>
```

> Recapitulando: O _canvas_ é uma área da tela onde podemos desenhar, escrever com um pincel.

Precisamos informar, em nosso programa, quanto o `<canvas>` ocupa de espaço. Para isso, utilizaremos dois atributos, o `width`, que em português é "largura", diremos que é 600, e o `height`, ou "altura", que será de 400.

```xml
<canvas width="600" height="400"> </canvas>
```

Se salvarmos e recarregarmos a página, nada acontece para nós, visualmente. Isso porque o `<canvas>` é branco, por padrão. Como o fundo do navegador também é, não conseguimos ver o que acabamos de criar.

Para que possamos visualizar, faremos com que ele ganhe cor. É o que veremos adiante.