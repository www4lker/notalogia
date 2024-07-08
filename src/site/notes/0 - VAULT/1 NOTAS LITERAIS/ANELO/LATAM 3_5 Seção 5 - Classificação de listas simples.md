---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/latam-3-5-secao-5-classificacao-de-listas-simples/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# 3.5 Seção 5 - Classificação de listas simples: o algoritmo de classificação bubblesort

## criado em: 
-  09-05-2023 - 14:54

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM Bem-vindo ao Fundamentos do Python\|LATAM Bem-vindo ao Fundamentos do Python]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023-11 Seção 1 - Introdução à programação\|LATAM 2023-11 Seção 1 - Introdução à programação]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023 2 Seção 1 - O Programa Olá, mundo\|LATAM 2023 2 Seção 1 - O Programa Olá, mundo]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023 2 S 2 - Operadores - ferramentas de manipulação de dados\|LATAM 2023 2 S 2 - Operadores - ferramentas de manipulação de dados]]
- tags: #python #ANELO 
- Fontes & Links: https://skillsforall.com/launch?id=c889bca7-0c31-4ee6-9424-bc709fe7be92&tab=curriculum&view=b3beab38-edc1-56d1-ba14-73690f12a5f1

---

# 3.5 Seção 5 - Classificação de listas simples: o [[0 - VAULT/1 NOTAS LITERAIS/ANELO/algoritmo de classificação bubblesort\|algoritmo de classificação bubblesort]]

Role para comecar  

Bem-vindo à seção 5, onde você aprenderá a classificar listas simples usando o algoritmo de classificação de Bubblesort.

Concluída 3.5.1 A ordenção em bolhas

3.5.1 A ordenção em bolhas

Agora que você pode efetivamente manipular os elementos das listas, é hora de aprender a **classificá**-las. Muitos algoritmos de classificação foram inventados até agora, que diferem muito na velocidade e na complexidade. Vamos mostrar um algoritmo muito simples, fácil de entender, mas infelizmente não muito eficiente. É usado muito raramente, e certamente não para listas grandes e extensas.

Digamos que uma lista pode ser classificada de duas maneiras:

-   crescente (ou mais precisamente - não decrescente) - se, em cada par de elementos adjacentes, o primeiro elemento não for maior que o último;
-   diminuindo (ou mais precisamente - não aumentando) - se em cada par de elementos adjacentes o primeiro elemento não for menor que o último.

Nas seções a seguir, classificaremos a lista em ordem crescente, para que os números sejam ordenados do menor para o maior.

Aqui está a lista:

8

10

6

2

4

Vamos tentar usar a seguinte abordagem: vamos pegar o primeiro e o segundo elementos e compará-los; se determinarmos que eles estão na ordem errada (ou seja, o primeiro é maior que o segundo), vamos trocá-los; se o pedido for válido, não faremos nada. Uma rápida olhada em nossa lista confirma a última; os elementos 01 e 02 estão na ordem correta, como em 8<10.

Agora, observe o segundo e o terceiro elementos. Eles estão nas posições erradas. Temos que trocá-los:

8

**6**

**10**

2

4

Vamos mais além e olhamos para o terceiro e o quarto elementos. Novamente, isso não é o que deveria ser. Temos que trocá-los:

8

6

**2**

**10**

4

Agora vamos verificar o quarto e o quinto elementos. Sim, eles também estão nas posições erradas. Outra troca ocorre:

8

6

2

**4**

**10**

A primeira passagem pela lista já está concluída. Ainda estamos longe de terminar nosso trabalho, mas algo curioso aconteceu enquanto isso. O maior elemento, 10, já foi ao fim da lista. Observe que este é **o local desejado**. Todos os elementos restantes formam uma confusão pitoresca, mas este já está em vigor.

Agora, por um momento, tente imaginar a lista de uma maneira um pouco diferente, ou seja, assim:

10

4

2

6

8

Veja - 10 está no topo. Poderíamos dizer que ela flutuava do fundo para a superfície, como a **bolha em uma taça de champanha**. O método de classificação deriva seu nome da mesma observação - é chamado de **classificação de bolha**.

Agora vamos começar com a segunda passagem pela lista. Analisamos o primeiro e o segundo elementos - uma troca é necessária:

**6**

**8**

2

4

10

Tempo para o segundo e terceiro elementos: temos que trocá-los também:

6

**2**

**8**

4

10

Agora, o terceiro e o quarto elementos e a segunda passagem estão concluídos, pois 8 já está em vigor:

6

2

**4**

**8**

10

Começamos o próximo passe imediatamente. Observe o primeiro e o segundo elementos com cuidado; outra troca é necessária:

**2**

**6**

4

8

10

Agora 6 precisa ser implementado. Trocamos o segundo e o terceiro elementos:

2

**4**

**6**

8

10

A lista já está classificada. Não temos mais nada a fazer. Isso é exatamente o que queremos.

Como você pode ver, a essência desse algoritmo é simples: **comparamos os elementos adjacentes e, ao trocar alguns deles, atingimos nosso objetivo**.

Vamos codificar em Python todas as ações executadas durante uma única passagem pela lista e, em seguida, vamos considerar quantas passagens realmente precisamos para realizá-la. Não explicamos isso até agora, e faremos isso um pouco mais tarde.

Incompleta 3.5.2 Ordenando uma lista

3.5.2 Ordenando uma lista

Quantos passos precisamos para classificar a lista inteira?

Resolvemos esse problema da seguinte maneira: **introduzimos outra variável** ; sua tarefa é observar se alguma troca foi feita durante a passagem ou não; se não houver troca, a lista já está classificada e nada mais precisa ser feito. Criamos uma variável chamada swapped e atribuímos um valor de False a ela para indicar que não há swaps. Caso contrário, ele será atribuído como True.

              `my_list = [8, 10, 6, 2, 4]  # Lista para ordenar                                                for i in range(len(my_list) - 1):  # precisamos de (5 - 1) comparações                                    if my_list[i] > my_list[i + 1]:  # comparar elementos adjacentes                                        my_list[i], my_list[i + 1] = my_list[i + 1], my_list[i]  # Se acabarmos aqui, nós temos que trocar os elementos.`
              
               
          
              

      

Você deve conseguir ler e entender este programa sem problemas:

              `my_list = [8, 10, 6, 2, 4]  # Lista para ordenar                                swapped = True  # É um pouco falso, precisamos dele para entrar no loop while.                                                while swapped:                                    swapped = False  # nenhuma troca até agora                                    for i in range(len(my_list) - 1):                                        if my_list[i] > my_list[i + 1]:                                            swapped = True  # uma troca ocorreu!                                            my_list[i], my_list[i + 1] = my_list[i + 1], my_list[i]                                                print(my_list)`
              
               
          
              

      

Execute o programa e teste-o.

Console

Incompleta 3.5.3 A ordenação por bolhas - versão interativa

3.5.3 A ordenação por bolhas - versão interativa

No editor, você pode ver um programa completo, enriquecido por uma conversa com o usuário, e permitindo que ele insira e imprima elementos da lista: **A classificação de bolha - versão interativa final**.

Console

Python, no entanto, tem seus próprios mecanismos de classificação. Ninguém precisa escrever seus próprios tipos, pois há um número suficiente de **ferramentas prontas para o uso**.

Explicamos esse sistema de classificação porque é importante aprender a processar o conteúdo de uma lista e mostrar como a classificação real pode funcionar.

Se você quiser que o Python classifique sua lista, é possível fazer o seguinte:

              `my_list = [8, 10, 6, 2, 4]                                my_list.sort()                                print(my_list)`
              
               
          
              

      

É simples assim.

A saída do fragmento é a seguinte:

              `[2, 4, 6, 8, 10]`
          
              

              Output
      

Como você pode ver, todas as listas têm um método chamado sort(), que as classifica o mais rápido possível. Você já aprendeu sobre alguns dos métodos de lista antes e em breve aprenderá mais sobre outros.

Concluída

---

**3.5.4 RESUMO DA SEÇÃO**

---

---

**3.5.4 RESUMO DA SEÇÃO**

---

1. Você pode usar o método sort() para classificar elementos de uma lista, por exemplo:

              `lst = [5, 3, 1, 2, 4]                                print(lst)                                                lst.sort()                                print(lst)  # outputs: [1, 2, 3, 4, 5]`
              
               
          
              

      

2. Há também um método de lista chamado revers(), que você pode usar para reverter a lista, por exemplo:

              `lst = [5, 3, 1, 2, 4]                                print(lst)                                                lst.reverse()                                print(lst)  # outputs: [4, 2, 1, 3, 5]`