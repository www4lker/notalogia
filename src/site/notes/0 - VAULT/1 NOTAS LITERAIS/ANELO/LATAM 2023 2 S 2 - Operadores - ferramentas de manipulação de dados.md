---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/latam-2023-2-s-2-operadores-ferramentas-de-manipulacao-de-dados/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# LATAM 2023 2 S 2 - Operadores - ferramentas de manipulação de dados

## criado em: 
-  03-05-2023 - 11:28

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM Bem-vindo ao Fundamentos do Python\|LATAM Bem-vindo ao Fundamentos do Python]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023-11 Seção 1 - Introdução à programação\|LATAM 2023-11 Seção 1 - Introdução à programação]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023 2 Seção 1 - O Programa Olá, mundo\|LATAM 2023 2 Seção 1 - O Programa Olá, mundo]]
- tags: #python #ANELO 
- Fontes & Links: 

---

## 2.3.1 Python como uma calculadora

Agora, vamos mostrar a você um lado completamente novo da função print(). Você já sabe que a função é capaz de mostrar os valores dos literais passados a ela por argumentos.

Na verdade, ele pode fazer algo mais. Confira o trecho:

print(2+2)

Redigite o código no editor e execute-o. Você consegue adivinhar o resultado?

Console

Você deve ver o número quatro. Sinta-se à vontade para experimentar outros operadores.

Sem levar isso a sério, você acabou de descobrir que o Python pode ser usado como uma calculadora. Não é muito prático, e definitivamente não é de bolso, mas mesmo assim uma calculadora.

Levando isso mais a sério, agora estamos entrando na província de operadores e expressões.
Incompleta 2.3.2 Operadores básicos
## 2.3.2 Operadores básicos

Um operador é um símbolo da linguagem de programação, capaz de operar com os valores.

Por exemplo, assim como na aritmética, o sinal de + (mais) é o operador que é capaz de adicionar dois números, dando o resultado da adição.

Nem todos os operadores Python são tão óbvios quanto o sinal de mais, então vamos ver alguns dos operadores disponíveis no Python, e vamos explicar quais regras regem o uso e como interpretar as operações que realizam.

Vamos começar com os operadores que estão associados às operações aritméticas mais amplamente reconhecidas:

+ - * / // % **

A ordem de aparência não é acidental. Falaremos mais sobre isso depois de passar por todos eles.

>Lembre-se: os dados e os operadores, quando conectados, formam expressões. A expressão mais simples é um literal em si.
Exponenciação

Veja o exemplo a seguir no editor:

Console

Nota: Recebemos os asteriscos duplos com espaços em nossos exemplos. Não é obrigatório, mas melhora a legibilidade do código.

Os exemplos mostram uma característica muito importante de praticamente todos os operadores numéricos do Python.

Execute o código e observe cuidadosamente os resultados que produz. Você pode ver alguma regularidade aqui?

Lembre-se: É possível formular as seguintes regras com base neste resultado:

    quando os dois ** argumentos são inteiros, o resultado também é um número inteiro;
    Quando pelo menos um argumento ** é um float, o resultado também é um float.

Esta é uma distinção importante para se lembrar.
Multiplicação

Um sinal de * (asterisco) é um operador de multiplicação.

Execute o código abaixo e verifique se nossa regra de número inteiro vs. flutuante ainda está funcionando.

Console
Divisão

Um sinal / (barra) é um operador de divisão.

O valor na frente da barra é um dividendo, o valor atrás da barra, um divisor.

Execute o código abaixo e analise os resultados.

Console

Você verá que há uma exceção à regra.

O resultado produzido pelo operador de divisão é sempre um float, independentemente de parecer ou não ser um flutuante à primeira vista: 1 / 2, ou se parece com um inteiro puro: 2 / 1.

Isso é um problema? Sim, o limite continua igual. Às vezes acontece que você realmente precisa de uma divisão que forneça um valor inteiro, não um valor flutuante.

Felizmente, o Python pode ajudá-lo com isso.
Divisão de número inteiro (divisão arredondada)

Um sinal // (barra dupla) é um operador de divisão inteira. Difere do padrão / operador em dois detalhes:

    seu resultado não possui a parte fracionária ‒ está ausente (para inteiros), ou é sempre igual a zero (para flutuantes); isso significa que os resultados são sempre arredondados;
    ele está de acordo com a regra integer vs. float.

Execute o exemplo abaixo e veja os resultados:

Console

Como você pode ver, a divisão de inteiro por inteiro dá um resultado inteiro. Todos os outros casos produzem floats.

Vamos fazer alguns testes mais avançados.

Observe o trecho a seguir:

Console

Imagine que usamos / em vez de // - você poderia prever os resultados?

Sim, seria 1.5 em ambos os casos. Isso é claro.

Mas que resultados devemos esperar com a // divisão?

Execute o código e veja por si mesmo.

O que obtemos são dois uns - um inteiro e um flutuador.

O resultado da divisão do número inteiro é sempre arredondado para o valor inteiro mais próximo que é menor que o resultado real (não arredondado).

Isso é muito importante: o arredondamento sempre vai para o número inteiro menor.

Observe o código abaixo e tente prever os resultados mais uma vez:

Console

Nota: alguns valores são negativos. Obviamente, isso afetará o resultado. Mas como?

O resultado é dois pares negativos. O resultado real (não arredondado) é -1.5 em ambos os casos. No entanto, os resultados são sujeitos a arredondamento. O arredondamento vai em direção ao valor inteiro menor, e o valor inteiro menor é -2, portanto: -2 e -2.0.
  Observação  

A divisão inteira também pode ser chamada de divisão de piso. Você definitivamente vai encontrar esse termo no futuro.
Restante (módulo)

O próximo operador é bastante peculiar, porque não tem equivalente entre os operadores aritméticos tradicionais.

Sua representação gráfica em Python é o sinal de % (percentual), que pode parecer um pouco confuso.

Tente pensar nisso como uma barra (operador de divisão) acompanhada de dois pequenos círculos engraçados.

O resultado do operador é o restante após a divisão do número inteiro.

Em outras palavras, é o valor que falta depois de dividir um valor por outro para produzir um quociente inteiro.

Nota: o operador às vezes é chamado de módulo em outras linguagens de programação.

Dê uma olhada no snippet - tente prever o resultado e execute-o:

Console

Como você pode ver, o resultado é dois. É por isso que:

    14 // 4 dá 3 → este é o quociente inteiro;
    3 * 4 dá 12 → como resultado da multiplicação de quociente e divisor;
    14 - 12 dá 2 → este é o restante.

Este exemplo é um pouco mais complicado:

print(12 % 4.5)

Qual é o resultado?
Como não dividir

Como você provavelmente sabe, a divisão por zero não funciona.

Não tente:

    realizar uma divisão por zero;
    realizar uma divisão inteira por zero;
    encontre o resto de uma divisão por zero.

Adição

O operador de adição é o sinal de + (mais), que está totalmente de acordo com os padrões matemáticos.

Novamente, dê uma olhada no snippet do programa abaixo:

Console

O resultado não deve ser surpreendente. Execute o código para verificá-lo.
O operador de subtração, os operadores unários e binários

O operador de subtração é obviamente o sinal - (menos), embora você deva notar que esse operador também tem outro significado -ele pode alterar o sinal de um número.

Esta é uma grande oportunidade para apresentar uma distinção muito importante entre operadores unários e binários.

Ao subtrair aplicações, o operador menos espera dois argumentos: o esquerdo (um minuendo em termos aritméticos) e o direito (um subtraendo).

Por esta razão, o operador de subtração é considerado um dos operadores binários, assim como os operadores de adição, multiplicação e divisão.

Mas o operador menos pode ser usado de uma forma diferente (unária) ‒ dê uma olhada na última linha do trecho abaixo:

Console

A propósito: também há um operador + unário. Você pode usá-lo assim:

print(+2)

O operador preserva o sinal de seu único argumento - o correto.

Embora essa construção seja sintaticamente correta, usá-la não faz muito sentido e seria difícil encontrar uma boa lógica para isso.

Dê uma olhada no snippet acima - você consegue adivinhar o resultado?
## Concluído 2.3.3 Operadores e suas prioridades
2.3.3 Operadores e suas prioridades

Até agora, tratamos cada operador como se não tivesse nenhuma conexão com os outros. Obviamente, uma situação tão simples e ideal é uma raridade na programação real.

Além disso, muitas vezes você encontrará mais de um operador em uma expressão e, em seguida, as coisas não serão mais tão simples.

Considere a seguinte expressão:

2 + 3 * 5

Você provavelmente se lembra da escola que as multiplicações precedem as adições.

Você certamente se lembra que primeiro deve multiplicar 3 por 5 e, mantendo o 15 na memória, adicione-o a 2, obtendo assim o resultado de 17.

O fenômeno que faz com que alguns operadores ajam antes de outros é conhecido como a hierarquia de prioridades.

O Python define com precisão as prioridades de todos os operadores e assume que os operadores de prioridade mais alta executam suas operações antes dos operadores de prioridade mais baixa.

Então, se você sabe que * tem uma prioridade mais alta que +, o cálculo do resultado final deve ser óbvio.
Operadores e suas ligações

A ligação do operador determina a ordem das computações executadas por alguns operadores com igual prioridade, colocados lado a lado em uma expressão.

A maioria dos operadores do Python tem ligação do lado esquerdo, o que significa que o cálculo da expressão é realizado da esquerda para a direita.

Este exemplo simples vai mostrar como ele funciona. Dê uma olhada:

print(9 % 6 % 2)

Há duas maneiras possíveis de avaliar essa expressão:

    da esquerda para a direita: primeiro 9 % 6 dá 3, e então 3 % 2 dá 1;
    da direita para a esquerda: primeiro 6 % 2 dá 0 e depois 9 % 0 causa um erro fatal.

Execute o exemplo e veja o que você obtém.

Console

O resultado deve ser 1. Este operador tem ligação do lado esquerdo. Mas há uma exceção interessante.

Repita o experimento, mas agora com exponenciação.

Use este trecho de código:

Console

Os dois resultados possíveis são:

    2 ** 2 → 4; 4 ** 3 → 64
    2 ** 3 → 8; 2 ** 8 → 256


Execute o código. O que você vê?

O resultado mostra claramente que o operador de exponenciação usa a associação do lado direito.

Isso tem um efeito interessante. Se o operador de exponenciação usar a associação pelo lado direito, você consegue adivinhar a saída do seguinte fragmento?

print(-3 ** 2) print(-2 ** 3) print(-(3 ** 2))

Lista de prioridades

Já que você é novo nos operadores Python, não queremos apresentar a lista completa de prioridades do operador agora.
[[0 - VAULT/1 NOTAS LITERAIS/ANELO/lista de operadores aritmeticos e suas prioridades\|lista de operadores aritmeticos e suas prioridades]]

Em vez disso, mostraremos um formulário truncado e o expandiremos de forma consistente ao apresentarmos novos operadores.

Veja a tabela abaixo:
Prioridade 	Operadora 	
1 	** 	
2 	+, - (observação: operadores unários localizados ao lado direito do operador de potência se vinculam mais fortemente)) 	unário
3 	*, /, //, % 	
4 	+, - 	⁪binário

Nota: enumeramos os operadores em ordem das prioridades mais altas (1) às mais baixas (4).

Tente trabalhar com a seguinte expressão:

print(2 * 3 % 5)
 


Ambos os operadores (* e %) têm a mesma prioridade, portanto, o resultado pode ser adivinhado apenas quando você sabe a direção da encadernação. O que você acha? Qual é o resultado?
Operadores e parênteses

Claro, você sempre pode usar parênteses, o que pode alterar a ordem natural de um cálculo.

De acordo com as regras aritméticas, subexpressões entre parênteses são sempre calculadas primeiro.

Você pode usar quantos parênteses precisar, e eles geralmente são usados para melhorar a legibilidade de uma expressão, mesmo que não alterem a ordem das operações.

Veja um exemplo de expressão com vários parênteses:

print((5 * ((25 % 13) + 100) / (2 * 13)) // 2)
 


Tente calcular o valor impresso no console. Qual é o resultado da função print()?

## 2.3.4 RESUMO DA SEÇÃO
Pontos principais

1. Uma expressão é uma combinação de valores (ou variáveis, operadores, chamadas para funções - você aprenderá sobre eles em breve) que resulta em um determinado valor, por exemplo, 1 + 2.

2. Operadores são símbolos especiais ou palavras-chave que são capazes de operar nos valores e realizar operações (matemáticas), por exemplo, o operador * multiplica dois valores: x * y.

3. Operadores aritméticos em Python: + (adição), - (subtração), * (multiplicação), / (divisão clássica ‒ sempre retorna um ponto flutuante), % (módulo ‒ divide o operando esquerdo pelo operando direito e retorna o restante da operação, por exemplo , 5 % 2 = 1), ** (exponenciação ‒ operando esquerdo elevado à potência do operando direito, por exemplo, 2 ** 3 = 2 * 2 * 2 = 8), // (floor/divisão inteira ‒ retorna um número resultante da divisão, mas arredondado para o número inteiro mais próximo, por exemplo, 3 // 2.0 = 1.0)
[[0 - VAULT/1 NOTAS LITERAIS/ANELO/Restinho em aritmética e programação\|Restinho em aritmética e programação]]

5. Um operador unário é um operador com apenas um operando, por exemplo, -1 ou +3.

6. Um operador binário é um operador com dois operandos, por exemplo, 4 + 5 ou 12 % 5.

7. Alguns operadores agem antes de outros - a hierarquia de prioridades:

    o operador ** (exponenciação) tem a prioridade mais alta;
    então o unário + e - (Nota: um operador unário à direita do operador de exponenciação se liga mais fortemente, por exemplo, 4 ** -1 é igual a 0.25)
    então: *, /, e %,
    e, por fim, a prioridade mais baixa: binário + e -.

7. Subexpressões entre parênteses são sempre calculadas primeiro, por exemplo, 15 - 1 * (5 * (1 + 2)) = 0.

8. O operador de exponenciação usa a associação do lado direito, por exemplo, 2 ** 2 ** 3 = 256.

---
![Pasted image 20230503172502.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230503172502.png)


# 2.4 Seção 4 - Variáveis

>Bem-vindo à seção quatro! Esta parte do curso se concentra nas variáveis - vamos aprender o que são, como usá-las e quais são as regras que as regem. Vamos lá?

 2.4.1 Variáveis - caixas em forma de dados

Parece bastante óbvio que o Python deva permitir que você codifique literais portando valores de número e texto.

Você já sabe que pode fazer algumas operações aritméticas com esses números: Adicionar, subtrair etc. Você fará isso muitas vezes.

Mas é uma pergunta normal perguntar como armazenar os resultados dessas operações, para usá-los em outras operações e assim por diante.

Como você salva os resultados intermediários e os usa novamente para produzir os subsequentes?

Python irá ajudá-lo com isso. Ele oferece "caixas" especiais (ou "contêineres", como podemos chamá-los) para essa finalidade, e essas caixas são chamadas de variáveis - o próprio nome sugere que o conteúdo desses contêineres pode ser variado (quase) de qualquer forma.
![Pasted image 20230503172944.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230503172944.png)
O que todas as variáveis Python têm?

    um nome;
    um valor (o conteúdo do contêiner)

Vamos começar com os problemas relacionados ao nome de uma variável.

As variáveis não aparecem em um programa automaticamente. Como desenvolvedor, você deve decidir quantas variáveis e quais usar em seus programas.

**Você também deve nomeá-los.** (o que nao parece, mas pode ser um desafio)
## 2.4.2 Nomes de variáveis
2.4.2 Nomes de variáveis

Se quiser dar um nome a uma variável, você deve seguir algumas regras estritas:

    o nome da variável deve ser composto de letras maiúsculas ou minúsculas, dígitos e o caractere _ (sublinhado)
    o nome da variável deve começar com uma letra;
    o caractere de sublinhado é uma letra;
    as letras maiúsculas e minúsculas são tratadas como diferentes (um pouco diferente do que no mundo real - Alice e ALICE são os mesmos nomes, mas em Python são dois nomes de variáveis diferentes e, consequentemente, duas variáveis diferentes);
    o nome da variável não deve ser nenhuma das palavras reservadas do Python (as palavras-chave - explicaremos mais sobre isso em breve).

**Observe que as mesmas restrições se aplicam a nomes de função.**

O Python não impõe restrições ao comprimento dos nomes de variáveis, mas isso não significa que um nome de variável longo seja sempre melhor do que um nome curto.

Aqui estão alguns nomes de variáveis corretos, mas nem sempre convenientes:

    MyVariable
    i
    l
    t34
    Exchange_Rate
    counter
    days_to_christmas
    TheNameIsTooLongAndHardlyReadable
    _

Esses nomes de variáveis também estão corretos:

    Adiós_Señora
    sûr_la_mer
    Einbahnstraße
    переменная.

O Python permite que você use não apenas letras latinas, mas também caracteres específicos de idiomas que usam outros alfabetos.

E agora, alguns nomes incorretos:

    10t (não começa com uma letra)
    !important (não começa com uma letra)
    exchange rate (contém um espaço).

  Observação  

O PEP 8 - Guia de Estilo para Código Python recomenda a seguinte convenção de nomenclatura para variáveis e funções em Python:
[[0 - VAULT/1 NOTAS LITERAIS/ANELO/Style guide Python\|Style guide Python]]

    os nomes de variáveis devem estar em letras minúsculas, com palavras separadas por sublinhados para melhorar a legibilidade (por exemplo, var, my_variable)
    nomes de funções seguem a mesma convenção que nomes de variáveis (por exemplo, fun, my_function)
    também é possível usar casos mistos (por exemplo, myVariable), mas apenas em contextos onde esse já é o estilo predominante, para manter a compatibilidade com a convenção adotada.

### Palavras-chave

Dê uma olhada na lista de palavras que desempenham um papel muito especial em todos os programas Python.

```
'False', 'None', 'True', 'and', 'as', 'assert', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield'
```

Eles são chamados de palavras-chave ou (mais precisamente) palavras-chave reservadas. Eles são reservados porque você não deve usá-los como nomes: nem para suas variáveis, nem funções, nem quaisquer outras entidades nomeadas que você deseja criar.

O significado da palavra reservada é predefinido e não deve ser alterado de forma alguma.

Felizmente, devido ao fato de que o Python faz distinção entre maiúsculas e minúsculas, você pode modificar qualquer uma dessas palavras alterando a letra de qualquer letra, criando assim uma nova palavra, que não é mais reservada.

Por exemplo - você não pode nomear sua variável assim:

import

Você não deve ter uma variável chamada dessa forma - ela é proibida. Mas você pode fazer isso:

Import (letra inicial maiúscula)

Essas palavras podem ser um mistério para você agora, mas você aprenderá em breve o significado delas.
## Concluído 2.4.3 Como criar variáveis
2.4.3 Como criar variáveis

O que você pode colocar dentro de uma variável?

Qualquer coisa.

Você pode usar uma variável para armazenar qualquer valor de qualquer um dos tipos já apresentados, e muitos outros que ainda não mostramos.

O valor de uma variável é o que você coloca nela. Pode variar com a frequência desejada ou desejada. Pode ser um inteiro um momento, e um momento depois, e, se tornar uma string.

Vamos falar agora de duas coisas importantes - como as variáveis são criadas e como colocar valores dentro delas (ou melhor, como dar ou passar valores para elas).

### Lembre-se  

Uma variável passa a existir como resultado da atribuição de um valor a ela. Ao contrário de outros idiomas, você não precisa declará-lo de nenhuma maneira especial.

Se você atribuir qualquer valor a uma variável inexistente, a variável será criada automaticamente. Você não precisa fazer mais nada.

A criação (ou seja, sua sintaxe) é extremamente simples: basta usar o nome da variável desejada, depois o sinal de igual (=) e o valor que deseja colocar na variável.

Dê uma olhada no snippet no editor:

Console

Consiste em duas instruções simples:

    O primeiro deles cria uma variável chamada var e atribui um literal com um valor inteiro igual a 1.
    O segundo imprime o valor da variável recém-criada no console.

Como você pode ver, print() tem outro lado – ele também pode manipular variáveis. Você sabe qual será a saída do snippet? Execute o código para verificar.
Concluído 2.4.4 Como usar uma variável
## 2.4.4 Como usar uma variável

Você tem permissão para usar quantas declarações de variáveis forem necessárias para atingir seu objetivo, assim:

Console

No entanto, você não pode usar uma variável que não existe (em outras palavras, uma variável que não recebeu um valor).

Este exemplo causará um erro:

Console

Você sabe por quê? Tentamos usar uma variável chamada Var, que não tem nenhum valor (nota: var e Var são entidades diferentes e não têm nada em comum no que diz respeito ao Python).
### Lembre-se  

Você pode usar a função print() e combinar texto e variáveis usando o operador + para gerar sequências e variáveis. Por exemplo:

var = "3.8.5"
print("Versão Python: " + var)
 

Você consegue adivinhar a saída do snippet acima?
Concluído 2.4.5 Como atribuir um novo valor a uma variável já existente
## 2.4.5 Como atribuir um novo valor a uma variável já existente

Como você atribui um novo valor a uma variável que já existe? Da mesma forma. Você só precisa usar o sinal de igual.

O sinal de igual é, na verdade, um operador de atribuição. Embora isso possa parecer estranho, o operador tem uma sintaxe simples e uma interpretação clara.

Ela atribui o valor do argumento da direita para a esquerda, enquanto o argumento da direita pode ser uma expressão arbitrariamente complexa envolvendo literais, operadores e variáveis já definidas.

Veja o código abaixo:

Console

O código envia duas linhas para o console:

1
2
Output

A primeira linha do trecho cria uma nova variável chamada var e atribui 1 a ela.

A instrução diz: atribua um valor de 1 a uma variável denominada var.

Podemos dizer mais curto: atribua 1 ao var.

Alguns preferem ler uma declaração como: var se torna 1.

A terceira linha atribui a mesma variável com o novo valor retirado da própria variável, somada com 1. Vendo um registro como esse, um matemático provavelmente protestaria - nenhum valor pode ser igual a si mesmo mais um. Isso é uma contradição. Mas Python trata o sinal = não como igual a, mas como atribuir um valor a.

Então, como você lê esse registro no programa?

Pegue o valor atual da variável var, adicione 1 e armazene o resultado na variável var.

Com efeito, o valor da variável var tem sido incrementado por um, o que não tem nada a ver com a comparação da variável com qualquer valor.

Você sabe qual será a saída do snippet a seguir?

var = 100
var = 200 + 300
print(var)
 

Concluído 2.4.6 Solução de problemas matemáticos simples
## 2.4.6 Solução de problemas matemáticos simples

Agora você deve ser capaz de construir um programa curto que resolva problemas matemáticos simples, como o teorema de Pitágoras:

O quadrado da hipotenusa é igual à soma dos quadrados dos outros dois lados.

O código a seguir avalia o comprimento da hipotenusa (ou seja, o lado mais longo de um triângulo retângular, o oposto do ângulo reto) usando o teorema de Pitágoras:

a = 3.0
b = 4.0
c = (a ** 2 + b ** 2) ** 0.5
print("c =", c)
 

Nota: precisamos fazer uso do operador ** para avaliar a raiz quadrada como:

√ (x)  = x(½)

e

c = √ a2 + b2 

Você consegue adivinhar a saída do código?

```
O código em Python que você forneceu implementa o teorema de Pitágoras, que estabelece que em um triângulo retângulo, o quadrado da hipotenusa é igual à soma dos quadrados dos outros dois lados.

Em termos matemáticos, se a e b são os comprimentos dos dois catetos e c é o comprimento da hipotenusa, então:

c^2 = a^2 + b^2

O código que você apresentou define os comprimentos dos catetos como "a = 3.0" e "b = 4.0", e em seguida, calcula o comprimento da hipotenusa usando a fórmula do teorema de Pitágoras.

O resultado é armazenado na variável "c" e, em seguida, é impresso na tela usando o comando "print".

Em resumo, o código Python apresentado é uma implementação da fórmula matemática do teorema de Pitágoras para calcular a hipotenusa de um triângulo retângulo a partir dos comprimentos dos catetos.
```

Concluído 2.4.7   LAB   Variáveis
## 2.4.7   LAB   Variáveis
Cenário

Aqui está uma breve história:

Era uma vez em Appleland, John tinha três maçãs, Maria cinco maçãs e Adam tinha seis maças. Todos ficaram muito felizes e viveram por muito tempo. Fim da história.

Sua tarefa:

    crie as variáveis: john, mary e adam;
    atribuir valores às variáveis. Os valores devem ser iguais aos números de fruto possuído por John, Mary e Adam, respectivamente;
    tendo armazenado os números nas variáveis, imprimindo as variáveis em uma linha e separando cada uma delas com uma vírgula;
    Agora, crie uma nova variável chamada total_apples igual à adição das três variáveis anteriores.
    imprima o valor armazenado em total_apples no console;
    experimente com seu código: crie novas variáveis, atribua valores diferentes a elas e execute várias operações aritméticas nelas (por exemplo, +, -, *, /, //, etc.). Tente imprimir uma sequência de caracteres e um número inteiro juntos em uma linha, por exemplo, "Número total de maças:" e total_apples.

```python
john = 3  
mary = 5  
adam = 6  
print(john, mary, adam)  
  
total_apples = john + mary + adam  
  
print(total_apples)  
  
print("Maçãs totais", total_apples, "\nJohn possui",john, "maçãs", "\nMary possui",mary,"maçãs","\nAdam possui",adam,"maçãs")
```

## 2.4.8 Operadores atalhos

É hora do próximo conjunto de operadores que facilita a vida do desenvolvedor. Frequentemente, queremos usar uma e a mesma variável nos lados direito e esquerdo do operador =.

Por exemplo, se precisamos calcular uma série de valores sucessivos de potências de 2, podemos usar uma parte como esta:

x = x * 2
 

Você pode usar uma expressão como essa se não conseguir adormecer e estiver tentando lidar com ela usando alguns métodos bons e antiquados:

sheep = sheep + 1
 

O Python oferece uma maneira reduzida de escrever operações como essas, que podem ser codificadas da seguinte forma:

x *= 2
sheep += 1
 

Vamos tentar apresentar uma descrição geral para essas operações. Se op for um operador de dois argumentos (esta é uma condição muito importante) e o operador for usado no seguinte contexto...:

variable = variable op expression

... então pode ser simplificado e exibido da seguinte forma:

variable op= expression

Veja os exemplos abaixo. Certifique-se de entender todos eles.
![Pasted image 20230503181239.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230503181239.png)
Expressão 	Operador de atalho

**A MELHOR FORMA DE LEMBRAR DISSO** é ver como se a variável duplicada do outro lado do sinal na verdade fosse um portal, e que no seu retorno ao lar (a variavel antes do sinal de designação "=" ) ela sempre traz o sinal de operção que estiver la com ela. 


## 2.4.9   LAB   Variáveis ‒ um simples conversor
Cenário

Milhas e quilômetros são unidades de comprimento ou distância.

Lembrando que 1 milha é igual a aproximadamente 1.61 quilômetros, complete o programa no editor para que converta:

    milhas em quilômetros;
    quilômetros em milhas.

Não altere nada no código atual. Escreva seu código nos locais indicados por ###. Teste seu programa com os dados que fornecemos no código-fonte.

Preste atenção especial ao que está acontecendo na função de print(). Analise como fornecemos multiplos argumentos para a função e como produzimos os dados esperados.

Observe que alguns dos argumentos dentro da função print() são strings (por exemplo, "milhas é", enquanto outros são variáveis (por exemplo, miles).
**Dica**  

Há mais uma coisa interessante acontecendo lá. Você pode ver outra função dentro da função print()? É a função round(). Seu trabalho é arredondar o resultado de saída para o número de casas decimais especificadas entre parênteses e retornar um float (dentro da função round() você pode encontrar o nome da variável, uma vírgula e o número de casas decimais que pretendemos por). Falaremos sobre funções muito em breve, então não se preocupe que tudo pode não estar totalmente claro ainda. Só queremos despertar a sua curiosidade.

Depois de concluir o laboratório, abra o Sandbox e experimente um pouco mais. Tente escrever conversores diferentes, por exemplo, um conversor de USD para EUR, um conversor de temperatura, etc. - deixe sua imaginação voar! Tente gerar os resultados combinando strings e variáveis. Tente usar e experimentar a função round() para arredondar seus resultados para uma, duas ou três casas decimais. Confira o que acontece se você não fornecer qualquer número de dígitos. Lembre-se de testar seus programas.

Experimente, tire conclusões e aprenda. Seja curioso.
Saída esperada

7.38 milhas é 11.88 quilômetros
12.25 quilômetros é 7.61 milhas
Output

Console

Concluído 2.4.10   LAB   Operadores e Expressões
## 2.4.10   LAB   Operadores e Expressões
Cenário

Dê uma olhada no código no editor: ele lê um valor float, coloca-o em uma variável chamada x e imprime o valor de uma variável chamada y. Sua tarefa é completar o código para avaliar a seguinte expressão:

3x3 - 2x2 + 3x - 1

O resultado deve ser atribuído a y.

Lembre-se de que a notação algébricas clássica gosta de omitir o operador de multiplicação - você precisa usá-la explicitamente. Observe como mudamos o tipo de dados para garantir que x seja do tipo float.

Mantenha seu código limpo e legível e teste-o usando os dados que fornecemos, atribuindo-o sempre à variável x (codificando-o). Não desanime por qualquer falha inicial. Seja persistente e inquisitivo.
Exemplo de entrada

x = 0
x = 1
x = -1

Exemplo de saída

y = -1.0
y = 3.0
y = -9.0
Output
```python
x = 15  
x = float(x)  
y = 3*x**3-2*x**2+3*x-1  
print("y =", y)  
  
x = 0  
x = float(x)  
y = 3*x**3-2*x**2+3*x-1  
print("y =", y)  
  
x = 1  
x = float(x)  
y = 3*x**3-2*x**2+3*x-1  
print("y =", y)  
  
x = -1  
x = float(x)  
y = 3*x**3-2*x**2+3*x-1  
print("y =", y)
```

Concluído
## 2.4.11 RESUMO DA SEÇÃO
2.4.11 RESUMO DA SEÇÃO

-  Uma variável é um local nomeado reservado para armazenar valores na memória. Uma variável é criada ou inicializada automaticamente quando você atribui um valor a ela pela primeira vez. (2.1.4.1)
- Cada variável deve ter um nome exclusivo ‒ um identificador. Um nome de identificador legal deve ser uma sequência não vazia de caracteres, deve começar com o sublinhado (_) ou uma letra e não pode ser uma palavra-chave do Python. O primeiro caractere pode ser seguido por sublinhados, letras e dígitos. Os identificadores em Python diferenciam maiúsculas de minúsculas.
- Python é uma **linguagem de tipagem dinâmica**, o que significa que você não precisa declarar variáveis nela. (2.1.4.3) Para atribuir valores a variáveis, você pode usar um operador de atribuição simples na forma do sinal de igual (=), ou seja, var = 1.
- Você também pode usar operadores de atribuição compostos (operadores de atalho) para modificar valores atribuídos a variáveis, por exemplo: var += 1 ou var /= 5 * 2.
- Você pode atribuir novos valores a variáveis já existentes usando o operador de atribuição ou um dos operadores compostos, por exemplo:

```python
var = 2
print(var)
 
var = 3
print(var)
 
var += 1
print(var)
 

```
    Você pode combinar texto e variáveis usando o operador + e usar a função print() para gerar sequências e variáveis, por exemplo: 

``` python
var = "007"
print("Agent " + var)
```

[[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023 - 2.5 Section 5 – Comments\|LATAM 2023 - 2.5 Section 5 – Comments]]