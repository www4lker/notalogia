---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/convencao-de-codigo/","tags":["TIPS"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# CONVENÇÃO DE CÓDIGO

## criado em: 
-  21-03-2023 - 11:21

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/concatenação\|concatenação]]
- tags: #TIPS
- Fontes & Links: 

---

Começando deste ponto? Você pode fazer o [DOWNLOAD](https://github.com/alura-cursos/logica-de-programacao-I/archive/aula-2.zip) do projeto do capítulo anterior e continuar seus estudos a partir deste capítulo.

---

Antes de avançarmos, veremos o conceito de **convenção de código**.

Em um prédio ou condomínio, todos os moradores devem seguir a respectiva convenção de condomínio. Por exemplo, digamos que é proibido entrar molhado no elevador - alguém lhe impede de fazer isso? Não, mas isso não será bem visto, podendo inclusive ser penalizado com multa.

Na programação temos algo parecido, que é a convenção do código com o qual estamos trabalhando. Por exemplo, há uma convenção de que as tags HTML devem ser escritas com letras minúsculas. Porém, se utilizarmos `<H1>` ela funcionará perfeitamente.

Salvaremos e retornaremos ao navegador, recarregaremos a página e veremos que não há erro, o código continua funcionando. Entretanto, a **convenção** é utilizar letras minúsculas para as tags.

Outro ponto: da mesma forma, se na tag `<script>` escrevermos em letras maiúsculas, o resultado não será alterado, mas a convenção aconselha a mantermos as letras minúsculas. No entanto, tenha **atenção**, o mundo JavaScript é mais rígido.

Por exemplo, se escrevermos `ALERT` em maiúsculo, assim:

```xml
<script>

    ALERT("Isso sim é um programa");

</script>
```

E recarregarmos a página, não teremos o pop up. Ao abrirmos o console, veremos a seguinte mensagem:

```csharp
Uncaught ReferenceError: ALERT is not defined
```

Ou seja, `ALERT` não foi definido. O mundo JavaScript só está preparado para entender a sintaxe `alert`, em letras minúsculas. Devemos ser mais cuidadosos no mundo JavaScript. Ao escrevermos em letras maiúsculas, estamos incorrendo em um erro de **sintaxe**. É como o português, ao escrevermos uma palavra errada, estamos cometendo um erro de sintaxe.

Relembrando nosso código, criaremos um novo programa. Abriremos um novo arquivo, utilizando o atalho "Ctrl + N", e "Ctrl + S" para salvá-lo. Seu destino será a pasta `logica`, e o nome do arquivo é `programa.html`.

Para abri-lo no navegador, acessaremos o menu "Arquivo" na barra superior, e selecionaremos "Arquivo > programa.html". Caso você não possua um menu no seu Google Chrome basta utilizar o atalho `CTRL + O` e navegar até o arquivo criado. Nada acontece. Isso porque ainda não programamos nada.

Retornaremos ao editor de texto. Até o final do treinamento, todo o código que escrevermos seguirá sempre a mesma estrutura mínima. Nosso objetivo é aprender a lógica de programação, portanto abordaremos o mínimo de conteúdo HTML e JavaScript.

O **mínimo** de que precisamos em nosso programa, para que ele funcione, é a tag `<meta>` com atributo `charset="UTF-8"`, sem o qual o programa pode até funcionar, mas haverá problemas de acentuação. Se queremos escrever um código em JavaScript ele deve estar inserido na tag `<script>`:

```xml
1 <meta charset="UTF-8">
2 
3 <script>
4 </script>
```

Por enquanto, este é o mínimo necessário para começarmos a programar e criar novos programas. Se salvarmos o arquivo, e o abrirmos no navegador, nada acontecerá porque ainda não há nada dentro da tag `<script>`.

Para esta tag, aprendemos o comando `alert`. Precisamos informá-lo sobre que informações serão exibidas. Às instruções que o JavaScript recebe é dado o nome de **parâmetro**, que o `alert` precisa receber. Isto faz parte da lógica de programação.

Para o parâmetro, aprendemos que, se quisermos escrever um texto no mundo JavaScript utilizaremos aspas. Como exemplo, utilizaremos a frase "A idade do Flávio é":

```xml
1 <meta charset="UTF-8">
2 
3 <script>
4     alert "A idade do Flávio é"
5
6 </script>
```

Isso é suficiente?

Salvaremos e retornaremos ao navegador. Se recarregarmos a página, veremos que nada aconteceu. Na barra de menu superior, selecionaremos as opções "Visualizar > Desenvolvedor > Console JavaScript ou se preferir a tecla `F12`". Veremos a seguinte mensagem de erro:

```typescript
Uncaught SyntaxError: Unexpected string
```

Indicando que o problema está na linha 4 do código. Retornaremos ao editor de texto. Não funcionou porque o `alert` recebe um texto, mas possui uma peculiaridade: ele deve ser passado entre parênteses, que neste caso funcionam como se fossem uma cesta, onde jogamos a informação. Portanto, "jogaremos" a _string_ dentro dela:

```xml
3 <script>
4     alert("A idade do Flávio é")
5
6 </script>
```

Salvaremos, retornaremos ao navegador, e recarregaremos a página.

Surge um alerta com a mensagem "A idade do Flávio é". Percebemos que mesmo não tendo colocado o ponto e vírgula após fecharmos os parênteses, ele funcionou. Para o curso de lógica, o **`;`** não é de grande relevância, entretanto, ao evoluirmos na linguagem JavaScript, sua ausência pode causar problemas. Por isso, criaremos desde já o hábito de utilizá-lo ao final de cada instrução. Isso deixará claro que é o final da respectiva instrução.

Ao salvarmos e recarregarmos a página, o alerta será exibido normalmente