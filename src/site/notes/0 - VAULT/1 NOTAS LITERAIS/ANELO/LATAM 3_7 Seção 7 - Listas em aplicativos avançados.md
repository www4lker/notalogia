---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/latam-3-7-secao-7-listas-em-aplicativos-avancados/","tags":["python","ANELO","1:**","2:**","3:**"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# LATAM 3_7 Seção 7 - Listas em aplicativos avançados

## criado em: 
-  09-05-2023 - 16:46

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 3_5 Seção 5 - Classificação de listas simples\|LATAM 3_5 Seção 5 - Classificação de listas simples]] 
- tags: #python #ANELO 
- Fontes & Links: 

---

Nesta seção, você aprenderá sobre matrizes, listas aninhadas (matrizes) e compreensões da lista.

Concluída 3.7.1 Listas em listas

# 3.7.1 Listas em listas

As listas podem consistir em escalares (ou seja, números) e elementos de uma estrutura muito mais complexa (você já viu exemplos como strings, booleanos ou até mesmo outras listas nas lições anteriores do Resumo da seção). Vamos dar uma olhada no caso em que os elementos de uma **lista são apenas listas**.

Muitas vezes, encontramos essas **matrizes** em nossas vidas. Provavelmente, o melhor exemplo disso é um **tabuleiro de xadrez**.

Um tabuleiro de xadrez é composto de linhas e colunas. Há oito linhas e oito colunas. Cada coluna é marcada com as letras de A a H. Cada linha é marcada com um número de um a oito.

A localização de cada campo é identificada por pares de letras e dígitos. Assim, sabemos que o canto inferior esquerdo do quadro (com a torre branca) é A1, enquanto o canto oposto é H8.

Vamos supor que somos capazes de usar os números selecionados para representar qualquer peça de xadrez. Também podemos assumir que **cada linha no tabuleiro de tabuleiro é uma lista**.

Veja o código abaixo:

              `row = []                                                for i in range(8):                                    row.append(WHITE_PAWN)`
              
               
          
              

      

Ele cria uma lista contendo oito elementos que representam a segunda linha do tabuleiro de tabuleiro - o preenchido com peões (assuma que WHITE_PAWN é um **símbolo predefinido** que representa um peão branco).

# Lista de compreensão

O mesmo efeito pode ser alcançado por meio de uma **compreensão de lista**, a sintaxe especial usada pelo Python para preencher listas enormes.

Uma compreensão de lista é, na verdade, uma lista, mas **criada em andamento durante a execução do programa e não é descrita estaticamente**.

Confira o trecho:

              `row = [WHITE_PAWN for i in range(8)]`
              
               
          
              

      

A parte do código colocada entre parênteses especifica:

-   os dados a serem usados para preencher a lista (WHITE_PAWN)
-   a cláusula que especifica quantas vezes os dados ocorrem dentro da lista (for i in range(8))

Veja outros **exemplos de compreensão da lista**:

**Exemplo #1:**

              `squares = [x ** 2 for x in range(10)]`
              
               
          
              

      

O snippet produz uma lista de dez elementos preenchida com quadrados de dez números inteiros começando em zero (0, 1, 4, 9, 16, 25, 36, 49, 64, 81)

**Exemplo #2:**

              `twos = [2 ** i for i in range(8)]`
              
               
          
              

      

O fragmento cria uma matriz de oito elementos que contém as oito primeiras potências de dois (1, 2, 4, 8, 16, 32, 64, 128)

**Exemplo #3:**

              `odds = [x for x in squares if x % 2 != 0 ]`
              
               
          
              

      

O fragmento faz uma lista com apenas os elementos ímpares da lista de squares.

Concluída 3.7.2 Matrizes bidimensionais

3.7.2 Matrizes bidimensionais

Vamos supor também que um **símbolo predefinido** chamado EMPTY designa um campo vazio no tabuleiro.

Então, se queremos criar uma lista de listas representando todo o tabuleiro de tabuleiro, isso pode ser feito da seguinte maneira:

              `board = []                                                for i in range(8):                                    row = [EMPTY for i in range(8)]                                    board.append(row)`
              
               
          
              

      

Nota:

-   a parte interna do loop cria uma linha que consiste em oito elementos (cada um deles igual a EMPTY) e a anexa à lista ao board;
-   a parte externa a repete oito vezes;
-   no total, a lista board compõe-se de 64 elementos (todos iguais a EMPTY)

Este modelo imita perfeitamente o tabuleiro de tabuleiro real, que na verdade é uma lista de oito elementos, todos sendo linhas únicas. Vamos resumir nossas observações:

-   os elementos das linhas são campos, oito deles por linha;
-   os elementos do tabuleiro são peças, oito deles por tabuleiro.

A variável board é agora uma **matriz bidimensional**. É também chamada, por analogia aos termos algébricos, de **matriz**.

Como as compreensões da lista podem ser **aninhadas**, podemos reduzir a criação da placa da seguinte maneira:

              `board = [[EMPTY for i in range(8)] for j in range(8)]`
              
               
          
              

      

A parte interna cria uma linha e a parte externa cria uma lista de linhas.

O acesso ao campo selecionado do quadro requer dois índices: o primeiro seleciona a linha; o segundo - o número do campo dentro da linha, que é de fato um número de coluna.

Dê uma olhada no tabuleiro de xadrez. Cada campo contém um par de índices que devem ser dados para acessar o conteúdo do campo:

![](https://skillsforall.com/content/pe1/1.0/m3/course/pt-BR/assets/984e1fdcdf6349b159ceb8644ea36c6f2ea570a0.png)

  

Olhando de relance para a figura mostrada acima, vamos colocar algumas peças de xadrez no tabuleiro. Primeiro, vamos adicionar todas as gralhas:

              `board[0][0] = ROOK                                board[0][7] = ROOK                                board[7][0] = ROOK                                board[7][7] = ROOK`
              
               
          
              

      

Se você quiser adicionar um Cavaleiro a C4, faça o seguinte:

              `board[4][2] = KNIGHT`
              
               
          
              

      

E agora um peão para o E5:

              `board[3][4] = PAWN`
              
               
          
              

      

E agora - experimente o código no editor.

Console

  

Concluída 3.7.3 Natureza multidimensional das listas: aplicações avançadas

3.7.3 Natureza multidimensional das listas: aplicações avançadas

Vamos aprofundar a natureza multidimensional das listas. Para encontrar qualquer elemento de uma lista bidimensional, você precisa usar duas _coordenadas_:

-   a vertical (número da linha)
-   e horizontal (número da coluna).

Imagine que você está desenvolvendo um software para uma estação meteorológica automática. O dispositivo registra a temperatura do ar a cada hora e faz isso durante todo o mês. Isso gera um total de 24 × 31 = 744 valores. Vamos tentar criar uma lista capaz de armazenar todos esses resultados.

Primeiro, você precisa decidir que tipo de dados seria adequado para essa aplicação. Nesse caso, um float seria o melhor, já que este termômetro é capaz de medir a temperatura com uma precisão de 0,1 ° C.

Em seguida, você toma uma decisão arbitrária de que as linhas gravarão as leituras de hora em hora (para que a linha tenha 24 elementos) e cada uma das linhas será atribuída a um dia do mês (vamos supor que cada mês tenha 31 dias, então você precisa de 31 linhas). Aqui está o par apropriado de compreensões (h é para hora, d para dia):

              `temps = [[0.0 for h in range(24)] for d in range(31)]`
              
               
          
              

      

Toda a matriz está preenchida com zeros agora. Você pode supor que ela é atualizada automaticamente usando agentes de hardware especiais. O que você precisa fazer é esperar que a matriz seja preenchida com medidas.

---

Agora é hora de determinar a temperatura média mensal ao meio-dia. Adicione todas as 31 leituras gravadas ao meio-dia e divida a soma por 31. Você pode supor que a temperatura da meia-noite é armazenada primeiro. Aqui está o código relevante:

              `temps = [[0.0 for h in range(24)] for d in range(31)]                                #                                # A matriz é magicamente atualizada aqui.                                #                                                total = 0.0                                                for day in temps:                                    total += day[11]                                                average = total / 31                                                print("Temperatura média ao meio-dia:", average)`
              
               
          
              

      

Observação: a variável day usada pelo loop for não é escalar; cada passagem pela matriz day itera por todas as linhas na temps a atribui às linhas subsequentes da matriz; portanto, é uma lista. Ele precisa ser indexado com 11 para acessar o valor de temperatura medido ao meio-dia.

---

Agora, encontre a temperatura mais alta durante todo o mês - veja o código:

              `temps = [[0.0 for h in range(24)] for d in range(31)]                                #                                # A matriz é magicamente atualizada aqui.                                #                                                highest = -100.0                                                for day in temps:                                    for temp in day:                                        if temp > highest:                                            highest = temp                                                print("A maior temperatura foi:", highest)`
              
               
          
              

      

Nota:

-   a variável day itera por todas as linhas na matriz temps;
-   a variável temp itera todas as medidas feitas em um dia.

---

Agora conte os dias em que a temperatura ao meio-dia era de pelo menos 20 ℃:

              `temps = [[0.0 for h in range(24)] for d in range(31)]                                #                                # A matriz é magicamente atualizada aqui.                                #                                                hot_days = 0                                                for day in temps:                                    if day[11] > 20.0:                                        hot_days += 1                                                print(hot_days, "dias estavam quentes.")`
              
               
          
              

      

O Python não limita a profundidade da inclusão na lista. Aqui você pode ver um exemplo de uma matriz tridimensional:

              `rooms = [[[False for r in range(20)] for f in range(15)] for t in range(3)]`
              
               
          
              

      

Imagine um hotel. É um grande hotel composto de três edifícios, de 15 andares cada. Há 20 salas em cada andar. Para isso, você precisa de uma matriz que possa coletar e processar informações sobre as salas ocupadas/livres.

Primeira etapa - o tipo dos elementos da matriz. Nesse caso, um valor booleano (True/False) seria adequado.

Etapa dois - Análise calma da situação. Resuma as informações disponíveis: três edifícios, 15 andares, 20 salas.

Agora você pode criar a matriz:

              `rooms = [[[False for r in range(20)] for f in range(15)] for t in range(3)]`
              
               
          
              

      

O primeiro índice (0 a 2) seleciona um dos edifícios; o segundo (0 a 14) seleciona o piso, o terceiro (0 a 19) seleciona o número do quarto. Todas as salas são gratuitas.

Agora você pode reservar um quarto para dois noivos: no segundo edifício, no décimo andar, quarto 14:

              `rooms[1][9][13] = True`
              
               
          
              

      

e liberar a segunda sala no quinto andar, localizada no primeiro edifício:

              `rooms[0][4][1] = False`
              
               
          
              

      

Verifique se há vagas no 15º andar do terceiro edifício:

              `vacancy = 0                                                for room_number in range(20):                                    if not rooms[2][14][room_number]:                                        vacancy += 1`
              
               
          
              

      

A variável vacancy contém 0 se todas as salas estiverem ocupadas ou o número de salas disponíveis em contrário.

Parabéns! Você chegou ao final do módulo. Continue assim!

Concluída 3.7.4 RESUMO DA SEÇÃO

---

**3.7.4 RESUMO DA SEÇÃO**

---

1. A **compreensão da lista** permite criar novas listas a partir das existentes de forma concisa e elegante. A sintaxe de uma compreensão de lista tem a seguinte aparência:

              `[expressão para elemento na lista se condicional]`
              
               
          
              

      

que é equivalente ao seguinte código:

              `for element in list:                                    if conditional:                                        expression`
              
               
          
              

      

Aqui está um exemplo de compreensão de lista - o código cria uma lista de cinco elementos preenchida com os cinco primeiros números naturais elevados à potência de 3:

              `cubed = [num ** 3 for num in range(5)]                                print(cubed)  # outputs: [0, 1, 8, 27, 64]`
              
               
          
              

      

  

2. Você pode usar **listas aninhadas** em Python para criar **matrizes** (ou seja, listas bidimensionais). Por exemplo:

![](https://skillsforall.com/content/pe1/1.0/m3/course/pt-BR/assets/a6f8b0aeb5d930c150505e4866501b82f1ba8750.png)

              `# Uma tabela de quatro colunas/quatro linhas ‒ uma matriz bidimensional (4x4)                                                table = [[":(", ":)", ":(", ":)"],                                         [":)", ":(", ":)", ":)"],                                         [":(", ":)", ":)", ":("],                                         [":)", ":)", ":)", ":("]]                                                print(table)                                print(table[0][0])  # outputs: ':('                                print(table[0][3])  # outputs: ':)'`
              
               
          
              

      

  

3. Você pode aninhar quantas listas desejar, criando assim listas n-dimensionais, por exemplo, matrizes de três, quatro ou até mesmo sessenta e quatro dimensões. Por exemplo:

![](https://skillsforall.com/content/pe1/1.0/m3/course/pt-BR/assets/ddf332e438f646e9bc66aac916282ca065c47292.png)

              `# Cubo - uma matriz tridimensional (3x3x3)                                                cube = [[[':(', 'x', 'x'],                                         [':)', 'x', 'x'],                                         [':(', 'x', 'x']],                                                        [[':)', 'x', 'x'],                                         [':(', 'x', 'x'],                                         [':)', 'x', 'x']],                                                        [[':(', 'x', 'x'],                                         [':)', 'x', 'x'],                                         [':)', 'x', 'x']]]                                                print(cube)                                print(cube[0][0][0])  # outputs: ':('                                print(cube[2][2][0])  # outputs: ':)'`