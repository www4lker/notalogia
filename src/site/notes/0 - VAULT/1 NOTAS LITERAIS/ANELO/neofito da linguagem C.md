---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/neofito-da-linguagem-c/","tags":["linguagem-c","ANELO","cover"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# neofito da linguagem C

## criado em: 
-  30-04-2023 - 17:38

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Linux - 101\|Linux - 101]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/notas de estudo/javascript 1/CONVENÇÃO DE CÓDIGO\|CONVENÇÃO DE CÓDIGO]]
- tags: #linguagem-c #ANELO 
- Fontes & Links: 

---

[alura.com.br](https://www.alura.com.br/artigos/comecando-a-programar-com-c)

# Começando a programar com C

Alura

7–9 minutos

---

![Imagem de destaque #cover](https://www.alura.com.br/artigos/assets/uploads/2018/06/abstract-access-close-up-1089438.jpg)

Quando vamos começar a estudar programação, nos deparamos com diversas linguagens de programação. Qual delas devemos aprender primeiro?

Independente da linguagem de programação, todas elas têm ao menos uma coisa em comum: **a lógica**. Não importa a linguagem que escolhemos para começar, a lógica executada será a mesma. Claro, talvez os passos para realizar essas tarefas sejam diferentes, pois cada linguagem tem uma sintaxe diferente.

Em meio tantas linguagens de programação, uma [muito popular](https://www.tiobe.com/tiobe-index/) é a [**linguagem C**](https://pt.wikipedia.org/wiki/C_(linguagem_de_programa%C3%A7%C3%A3o)).

A linguagem C é uma das linguagens mais utilizadas nos dias de hoje, e serviu como base para diversas outras linguagens, como [**C++**](https://www.alura.com.br/artigos/formacao-linguagem-c-plus-plus), C#, Java, PHP, Javascript, entre algumas outras. Mas como podemos escrever um programa em C?

## Olá, mundo! E algumas coisas a mais

Temos que começar a escrever nosso código que será o nosso programa em C. Para isso, podemos utilizar qualquer editor de textos. Precisamos falar para o computador que esse é um arquivo da linguagem C, para isso, colocamos a extensão `.c`:

![](https://www.alura.com.br/artigos/assets/uploads/2018/06/image_0-3.png)

Temos o arquivo criado, agora o que colocamos nele? Que comandos passamos para o computador começar a executar ações?

Vamos falar para o C imprimir (`printf`) uma mensagem para a gente no vídeo:

```

printf("Ola, Alura!");
```

Demos nossa instrução para o C. Falamos para ele imprimir um texto. O C pede que todo texto, também chamado de string, deve estar entre aspas duplas e toda instrução deve terminar com ponto e vírgula.

Esse código que escrevemos em C é um código legível por seres humanos. Isto é, uma pessoa consegue ler esse código sem muitos problemas. Contudo, o computador não entende essa linguagem.

Temos que transformar essa linguagem que nós escrevemos para uma linguagem que o computador consiga entender. Esse processo de transformação de um código de uma linguagem de programação em código de máquina é chamado de [**compilação**](https://www.alura.com.br/artigos/o-que-e-compilacao).

Quando compilamos um código, o compilador pega nosso código, neste caso escrito em C, e transforma para uma linguagem que a máquina entenda. Existem [**alguns compiladores disponíveis**](https://pt.wikipedia.org/wiki/Categoria:Compiladores_C), como estou utilizando um Linux, vou utilizar o [**GCC**](http://gcc.gnu.org/), que já vem por padrão na maioria das distribuições.

`gcc ola-mundo.c`

![](https://www.alura.com.br/artigos/assets/uploads/2018/06/image_1-3.png)

Não conseguimos compilar o código. O GCC retornou um erro quando tentamos. Por que isso aconteceu?

Nós pedimos para o C escrever um texto na tela, mas onde falamos para ele onde está essa instrução `printf`?

Nós queremos falar para o C usar uma instrução que realiza a saída dos dados. Isto é, mostrar uma mensagem na tela. Então precisamos mostrar pra ele de qual lugar essa função está vindo, isto é, de qual biblioteca ela vem.

No caso, a função `printf` vem da biblioteca padrão de entrada e saída de dados, a `stdio.h`. Para utilizar, basta pedir para o C incluí-la (`include`) no nosso arquivo:

```

#include <stdio.h>

printf("Ola, Alura!");
```

Bacana, se tentarmos compilar nosso programa veremos o mesmo erro:

![](https://www.alura.com.br/artigos/assets/uploads/2018/06/image_2-3.png)

Mas incluímos a biblioteca que tem a função `printf`, então por que esse erro continua?

Todo programa em C quando vai ser executado, precisa de uma função principal (`main`). Essa função indica qual o ponto de entrada no programa. Como queremos que o nosso `printf` apareça quando o programa rodar, precisamos declará-lo dentro da função `main`. Mas como declaramos essa função?

## A função principal

Como todo programa em C tem a função `main`, o C padronizou o estilo que declaramos essa função. Basta colocarmos `int main() { … }` e pronto! Temos a função principal. Tudo que estiver entre as chaves (`{ }`) será executado linha a linha quando o programa começar:

```

#include <stdio.h>

int main() {

    printf("Ola, Alura!");

}
```

Agora podemos pedir para o GCC compilar nosso arquivo sem receber um erro:

![](https://www.alura.com.br/artigos/assets/uploads/2018/06/image_3-3.png)

Legal, nosso arquivo está compilado! Agora, basta executá-lo. Mas como executar esse arquivo?

Como pedimos para o GCC apenas compilar esse arquivo, ele gera um nome automaticamente para o arquivo compilado. No meu caso esse nome é `a.out`:

![](https://www.alura.com.br/artigos/assets/uploads/2018/06/image_4-3.png)

Podemos falar para o computador executar esse código para a gente digitando `./` seguido do nome do arquivo:

![](https://www.alura.com.br/artigos/assets/uploads/2018/06/image_5-3.png)

Bacana! Conseguimos imprimir nossa mensagem na tela! Agora podemos ir aprendendo outras funcionalidades da linguagem. :)

## Para saber mais

O sinal de porcentagem que apareceu no final da frase, indica que naquele lugar acabou a string, isto é, acabou a frase que passamos para o `printf`. Como essa instrução não tinha uma quebra de linha, o meu **terminal inseriu **ela. Mas isso não é um comportamento padrão do programa.

O comum é que a linha não seja quebrada. Para colocar esse comportamento de quebra de linha como padrão, precisamos falar que no final da nossa frase, o `printf` imprima também uma linha nova (`\n`):

```

#include <stdio.h>

int main() {

    printf("Ola, Alura!\n");

}
```

Quando compilamos e rodamos o arquivo, veremos que o sinal de porcentagem sumiu, pois a quebra de linha está explícita agora:

![](https://www.alura.com.br/artigos/assets/uploads/2018/06/image_6-3.png)

Nestes casos, o compilador está nomeando nosso arquivo de saída. Mas se nós quisermos, podemos passar um nome para o arquivo que será compilado. Basta falarmos para o compilador gerar a saída (`-o`) para o arquivo `ola-mundo.out`, por exemplo:

`gcc ola-mundo.c -o ola-mundo.out`

![](https://www.alura.com.br/artigos/assets/uploads/2018/06/image_7.png)

Uma coisa que precisamos nos atentar é que quando declaramos a função `main`, colocamos a palavra `int` antes. Essa palavra indica o tipo de retorno de uma função. Ou seja, quando digitamos o `int main()`, falamos que a nossa função retorna um número inteiro. Contudo onde indicamos esse retorno?

Em alguns compiladores, quando nós compilássemos nosso código ele geraria um aviso (Warning) falando que a função `main` não tem valor de retorno. Isso não impediria o programa de rodar, mas não é considerada uma boa prática.

Ou seja, o legal é que a nossa função `main` retorne um número falando que sua execução ocorreu sem nenhum problema. Por convenção, este número é o `0`. Logo, podemos falar para a `main` retornar o número zero quando ela executar tudo que precisa:

```

#include <stdio.h>

int main() {

    printf("Ola, Alura!\n");

    return 0;
}
```

O C é uma linguagem muito utilizada até hoje. Ela tem uma capacidade de processamento muito alta.

Aqui na Alura, temos [**três cursos na linguagem**](https://www.alura.com.br/cursos-online-programacao/c). Em cada um deles você criará jogos que ajudarão a conhecer as funcionalidades da linguagem.

Também temos um [**curso sobre a linguagem C na Alura Start**](https://www.alurastart.com.br/curso-online-obic). Nele você também conhecerá as funcionalidades da linguagem. Além do curso de C, temos cursos que te mostrarão como utilizar os [**recursos da linguagem em desafíos da Olimpíada Brasileira de Informática**](https://www.alurastart.com.br/curso-online-obi2017-iniciacao1-fase1). Nele você verá como utilizar o C para criar algoritmos e se preparar para a olimpíada.