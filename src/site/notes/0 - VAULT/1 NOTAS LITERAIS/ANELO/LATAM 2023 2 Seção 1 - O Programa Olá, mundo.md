---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/latam-2023-2-secao-1-o-programa-ola-mundo/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# LATAM 2023 2 Seção 1 - O Programa Olá, mundo

## criado em: 
-  02-05-2023 - 18:48

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM Bem-vindo ao Fundamentos do Python\|LATAM Bem-vindo ao Fundamentos do Python]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023-11 Seção 1 - Introdução à programação\|LATAM 2023-11 Seção 1 - Introdução à programação]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023 2 S 2 - Operadores - ferramentas de manipulação de dados\|LATAM 2023 2 S 2 - Operadores - ferramentas de manipulação de dados]]- 
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/COMO CALCULAR NUMEROS BINARIOS\|COMO CALCULAR NUMEROS BINARIOS]]
- tags: #python #ANELO 
- Fontes & Links: 

---

# 2.1 Seção 1 - O Programa "Olá, mundo!

Bem-vindo ao módulo dois! Na primeira seção, vamos aprender sobre os elementos mais essenciais de sintaxe e semântica da linguagem Python, e usá-los para criar seu primeiro programa Python - "Olá, mundo!".

## 2.1.1 Seu primeiro programa

É hora de começar a escrever algum código Python real e funcional. Vai ser muito simples por enquanto.

Como mostraremos alguns conceitos e termos fundamentais, esses trechos de código não serão tão sérios ou complexos.

Execute o código na janela do editor. Se tudo correr bem aqui, você verá a linha de texto na janela do console.

Como alternativa, inicie o IDLE, crie um novo arquivo de origem Python, preencha-o com este código, nomeie o arquivo e salve-o. Agora execute-o. Se tudo correr bem, você verá o texto entre aspas na janela do console IDLE. O código que você executou deve parecer familiar. Vocês viram algo muito semelhante quando orientamos vocês pela configuração do ambiente IDLE.

Console

Agora vamos passar algum tempo mostrando e explicando o que você realmente está vendo e por que isso se parece com isso.

Como você pode ver, este primeiro programa consiste nas seguintes partes:

    a palavra print;
    um parênteses de abertura;
    aspas (")
    uma linha de texto: Olá, Mundo!;
    outra aspa;
    outro parênteses.

Cada uma das opções acima desempenha um papel muito importante no código.
Concluído 2.1.2 A função print()
## 2.1.2 A função print()

Veja a linha de código abaixo:

print("Olá, Mundo!")
 

A palavra print que você pode ver aqui é um nome de função. Isso não significa que, sempre que a palavra aparece, sempre há um nome de função. O significado da palavra vem do contexto em que a palavra foi usada.

Você provavelmente já encontrou o termo função muitas vezes, durante as aulas de matemática. Você provavelmente também pode listar vários nomes de funções matemáticas, como senoidal ou log.

As funções do Python, no entanto, são mais flexíveis e podem conter mais conteúdo do que seus irmãos matemáticos.

Uma função (nesse contexto) é uma parte separada do código do computador capaz de:

    causar algum efeito (por exemplo, envie texto para o terminal, crie um arquivo, desenhe uma imagem, toque um som etc.); isso é algo totalmente inédito no mundo da matemática;
    avaliar um valor (por exemplo, a raiz quadrada de um valor ou o comprimento de um determinado texto) e retorná-lo como resultado da função; é isso que torna as funções do Python parentes de conceitos matemáticos.

Além disso, muitas funções Python podem fazer as duas coisas acima juntas.
Lista de seções expansíveis. Selecione cada botão para expandir o conteúdo.
De onde vêm as funções?

O nome da função deve ser significativo (o nome da função de impressão é evidente).

Claro, se você vai usar qualquer função já existente, você não tem influência sobre seu nome, mas quando você começa a escrever suas próprias funções, você deve considerar cuidadosamente sua escolha de nomes.
Concluído 2.1.3 Argumentos de função
## 2.1.3 Argumentos de função

Como dissemos antes, uma função pode ter:

    um efeito;
    um resultado.

Há também um terceiro componente de função muito importante ‒ o(s) argumento(s).

As funções matemáticas geralmente levam um argumento. Por exemplo, sin(x) leva um x, que é a medida de um ângulo.

As funções Python, por outro lado, são mais versáteis. Dependendo das necessidades individuais, eles podem aceitar qualquer número de argumentos ‒ quantos forem necessários para realizar suas tarefas. Nota: quando dizemos qualquer número, que inclui zero ‒ algumas funções do Python não necessitam de argumento.
print("Olá Mundo!")

Apesar do número de argumentos necessários/fornecidos, as funções do Python exigem fortemente a presença de um par de parênteses ‒ abrindo e fechando, respectivamente.

Se você deseja entregar um ou mais argumentos para uma função, coloque-os dentro dos parênteses. Se você for usar uma função que não aceita nenhum argumento, ainda precisará dos parênteses.

Nota: para distinguir palavras comuns de nomes de funções, coloque um par de parênteses vazios após seus nomes, mesmo que a função correspondente precise de um ou mais argumentos. Essa é uma convenção padrão.

A função da qual estamos falando aqui é print().

A função print() em nosso exemplo tem algum argumento?

Claro que sim, mas o que são?
Cadeia de caracteres como o argumento da função print()

O único argumento entregue à função print() neste exemplo é uma string:
print("Olá Mundo!")

Como você pode ver, a string é delimitada por aspas - na verdade, as aspas formam a string - elas cortam uma parte do código e atribuem um significado diferente a ele.

Você pode imaginar que as citações dizem algo como: o texto entre nós não é código. Não se destina a ser executado e você deve tomá-lo como está.

Quase tudo o que você coloca dentro das aspas será levado literalmente, não como código, mas como dados. Tente brincar com essa string específica - modifique-a, insira algum novo conteúdo, exclua parte do conteúdo existente.

Há mais de uma maneira de especificar uma string dentro do código do Python, mas por enquanto, porém, essa é suficiente.

Até agora, você aprendeu sobre duas partes importantes do código: a função e a string. Conversamos sobre eles em termos de sintaxe, mas agora é hora de discuti-los em termos de semântica.
Concluído 2.1.4 Chamada de função
## 2.1.4 Chamada de função

O nome da função (print neste caso), juntamente com os parênteses e os argumento(s), formam a invocação da função.

print("Olá Mundo!")
 

Vamos discutir isso em mais detalhes em breve, mas vamos esclarecer isso agora.

O que acontece quando o Python encontra uma invocação como esta abaixo?
function_name(argument)

Vamos ver:

    Primeiro, o Python verifica se o nome especificado é legal (ele navega em seus dados internos para encontrar uma função atual do nome; se essa pesquisa falhar, o Python anula o código)
    segundo, o Python verifica se os requisitos da função para o número de argumentos permitem que você chame a função dessa maneira (por exemplo, se uma função específica exigir exatamente dois argumentos, qualquer invocação que forneça apenas um argumento será considerada errônea e abortará os execução)
    terceiro, o Python deixa seu código por um momento e salta para a função que você deseja chamar; é claro, ele também usa seus argumentos e os passa para a função;
    quarto, a função executa seu código, causa o efeito desejado (se houver), avalia o (s) resultado (s) desejado (s) (se houver) e termina sua tarefa;
    por fim, o Python retorna ao seu código (para o local imediatamente após a invocação) e retoma a execução.


Concluído 2.1.5   LAB   Trabalhando com a função print()
## 2.1.5   LAB   Trabalhando com a função print()
Cenário

O comando print(), que é uma das diretrizes mais fáceis em Python, simplesmente imprime uma linha na tela.

Em seu primeiro laboratório:

    Use a função de print() para imprimir a linha Olá, Python! na tela. Use aspas duplas ao redor da string.
    Depois de fazer isso, use a função print() novamente, mas desta vez imprima seu primeiro nome.
    Remova as aspas duplas e execute o código. Assista à reação do Python. Que tipo de erro é gerado?
    Em seguida, remova os parênteses, coloque aspas duplas e execute o código novamente. Que tipo de erro é gerado desta vez?
    Experimente o máximo que puder. Altere aspas duplas para aspas simples, use várias funções print() na mesma linha e, em seguida, em linhas diferentes. Veja o que acontece.


Console

Concluído 2.1.6 A função print() e seus efeitos, argumentos e valores retornados
## 2.1.6 A função print() e seus efeitos, argumentos e valores retornados

Três perguntas importantes devem ser respondidas o mais rápido possível:

1. Que efeito a função print() causa?

O efeito é muito útil e muito espetacular. A função:

    aceita seus argumentos (pode aceitar mais de um argumento e também pode aceitar menos de um argumento)
    Converte-os em forma legível pelo homem, se necessário (como você pode suspeitar, as strings não exigem essa ação, pois a string já é legível)
    e envia os dados resultantes para o dispositivo de saída (geralmente o console); Em outras palavras, tudo o que você coloca na função print() aparecerá na tela.

Não é de admirar que, a partir de agora, você utilizará a print() muito intensamente para ver os resultados de suas operações e avaliações.

2. Quais argumentos o print() espera?

Qualquer. Mostraremos em breve que o print() é capaz de operar com praticamente todos os tipos de dados oferecidos pelo Python. Strings, números, caracteres, valores lógicos, objetos - qualquer um desses itens pode ser passado com sucesso para print().

3. Qual valor a função print() retorna?

Nenhum. Seu efeito é suficiente.
Concluído 2.1.7 Instruções
## 2.1.7 Instruções

Você já viu um programa de computador que contém uma chamada de função. Uma invocação de função é um dos muitos tipos possíveis de instrução Python.

Obviamente, qualquer programa complexo geralmente contém muito mais instruções do que uma. A questão é: como você acopla mais de uma instrução no código Python?

A sintaxe do Python é bastante específica nessa área. Ao contrário da maioria das linguagens de programação, o Python exige que não haja mais de uma instrução em uma linha.

Uma linha pode estar vazia (ou seja, pode não conter nenhuma instrução), mas não deve conter duas, três ou mais instruções. Isso é estritamente proibido.

Nota: Python faz uma exceção a esta regra ‒ permite que uma instrução se espalhe por mais de uma linha (o que pode ser útil quando seu código contém construções complexas).

Vamos expandir um pouco o código. Você pode vê-lo no editor abaixo. Execute-o e observe o que você vê no console.

Console

Seu console Python agora deve estar assim:

A pequenina aranha escalou a tromba d'água.
Caiu a chuva e lavou a aranha.
Output

Esta é uma boa oportunidade para fazer algumas observações:

    o programa chama a função print() duas vezes, e você pode ver duas linhas separadas no console ‒ isso significa que print() começa sua saída a partir de uma nova linha cada vez que inicia sua execução; você pode mudar esse comportamento, mas também pode usá-lo a seu favor;
    cada invocação print() contém uma string diferente, como seu argumento, e o conteúdo do console a reflete ‒ isso significa que as instruções no código são executadas na mesma ordem em que foram colocadas no arquivo fonte; nenhuma instrução subseqüente é executada até que a anterior seja concluída (existem algumas exceções a esta regra, mas você pode ignorá-las por enquanto.)

Mudamos um pouco o exemplo - adicionamos uma Invocação de função vazia print(). Chamamos de vazio porque não entregamos nenhum argumento para a função.

Você pode vê-lo na janela do editor. Execute o código.

O que acontece?

Console

Se tudo der certo, você deverá ver algo assim:

A pequenina aranha escalou a tromba d'água.
 
Caiu a chuva e lavou a aranha.
Output

Como você pode ver, a invocação de print() vazia não é tão vazia quanto você esperava – ela produz uma linha vazia ou (esta interpretação também está correta) gera uma nova linha.

Esta não é a única maneira de produzir uma nova linha no console de saída. Agora vamos mostrar-lhe outra maneira.
Concluído 2.1.8 Escape do Python e caracteres de novas linhas
## 2.1.8 Escape do Python e caracteres de novas linhas

Modificamos o código novamente. Olhe com atenção.

Há duas mudanças muito sutis – inserimos um estranho par de caracteres dentro da rima. Eles se parecem com isso: \n.

Console

Curiosamente, enquantovocê pode ver dois caracteres, o Python vê um.

A barra invertida (\) tem um significado muito especial quando usada dentro de strings – isso é chamadode caractere de escape.

A palavra escape deve ser entendida especificamente - significa que a série de caracteres na string escapa por um momento (um momento muito curto) para introduzir uma inclusão especial.

Em outras palavras, a barra invertida não significa nada em si, mas é apenas um tipo de anúncio de que o próximo caractere após a barra invertida também tem um significado diferente.

A letra n colocada após a barra invertida vem da palavra newline (nova linha).
Tanto a barra invertida quanto o n formam um símbolo especial chamado caractere de nova linha, que incita o console a iniciar uma nova linha de saída.

Execute o código. Seu console agora deve ficar assim:

A aranha pequenininha
subiu a tromba d'água.
 
abaixo veio a chuva
e lavou a aranha.
Output

Como você pode ver, duas novas linhas aparecem na rima do berçário, nos lugares onde foram usados os \n.

Esta convenção tem duas consequências importantes:

1. Se você quiser colocar apenas uma barra invertida dentro de uma string, não se esqueça de sua natureza de escape - você precisa dobrá-la. Por exemplo, uma invocação como esta causará um erro:
print("\")

enquanto este não vai:
print("\\")

2. Nem todos os pares de escape (a barra invertida juntamente com outro caractere) significam algo.

Experimente seu código no editor, execute-o e veja o que acontece.

Console
Concluído 2.1.9 Usando vários argumentos
## 2.1.9 Usando vários argumentos

Até agora, testamos o comportamento da função print() sem argumentos e com um argumento. Também vale a pena tentar alimentar a função print() com mais de um argumento.

Olhe para a janela do editor. Isso é o que vamos testar agora:

Console

Há uma chamada de função print(), mas ela contém três argumentos. Todos eles são cadeias de caracteres.

Os argumentos são separados por vírgulas. Nós os cercamos de espaços para torná-los mais visíveis, mas não é realmente necessário, e não faremos mais isso.

Nesse caso, as vírgulas que separam os argumentos desempenham uma função completamente diferente da vírgula dentro da sequência. O primeiro faz parte da sintaxe do Python, enquanto o último deve ser exibido no console.

Se você olhar novamente o código, verá que não há espaços dentro das cadeias.

Execute o código e veja o que acontece.

O console agora deve estar mostrando o seguinte texto:

A pequenina aranha escalou a tromba d'água.
Output

Os espaços, removidos das cadeias, apareceram novamente. Você pode explicar por quê?

Duas conclusões emergem desse exemplo:

    uma função print() chamada com mais de um argumento gera todos eles em uma linha;
    a função print() coloca um espaço entre os argumentos gerados por sua própria iniciativa.

Incompleta 2.1.10 Argumentos posicionais
2.1.10 Argumentos posicionais

Agora que você sabe um pouco sobre os costumes da função print(), vamos mostrar-lhe como alterá-los.

Você deve ser capaz de prever a saída sem executar o código no editor.

Console

A forma como estamos passando os argumentos para a função print() é a mais comum em Python e é chamada de forma posicional. Esse nome vem do fato de que o significado do argumento é determinado pela sua posição (por exemplo, o segundo argumento será gerado após o primeiro, e não o contrário).

Execute o código e verifique se a saída corresponde às suas previsões.
Incompleta 2.1.11 Argumentos de palavra-chave
## 2.1.11 Argumentos de palavra-chave

O Python oferece outro mecanismo para a transmissão de argumentos, que pode ser útil quando você quiser convencer a função print() a mudar um pouco o comportamento.

Não vamos explicar isso em detalhes agora. Planejamos fazer isso quando falarmos sobre funções. Por enquanto, queremos apenas mostrar como ele funciona. Fique à vontade para usá-lo em seus próprios programas.

O mecanismo é chamado de argumentos de palavra-chave. O nome decorre do fato de que o significado desses argumentos é obtido não de sua localização (posição), mas da palavra especial (palavra-chave) usada para identificá-los.

A função print() tem dois argumentos de palavra-chave que você pode usar para seus propósitos. O primeiro é chamado de end.

Na janela do editor, você pode ver um exemplo muito simples de como usar um argumento de palavra-chave.

Console

Para usá-lo, é necessário conhecer algumas regras:

    um argumento de palavra-chave consiste em três elementos: uma palavra-chave que identifica o argumento (end aqui); um sinal de igual (=); e um valor atribuído a esse argumento;
    qualquer argumento de palavra-chave deve ser colocado após o último argumento posicional (isso é muito importante)

Em nosso exemplo, utilizamos o argumento chave end e o definimos como uma sequência contendo um espaço.

Execute o código para ver como ele funciona.

O console agora deve estar mostrando o seguinte texto:

Meu nome é Python. Monty Python.
Output

Como você pode ver, o argumento de palavra-chave end determina os caracteres que a função print() envia para a saída, uma vez que ela atinge o fim de seus argumentos de posição.

O comportamento padrão reflete a situação em que o argumento de palavra-chave end é usado implicitamente da seguinte maneira: end="\n".

E agora é hora de tentar algo mais difícil.

Se você olhar com atenção, verá que usamos o argumento end, mas a string atribuída a ele está vazia (não contém nenhum caractere).

O que vai acontecer agora? Execute o programa no editor para descobrir.

Console

Como o argumento end foi definido como nada, a função print() também não gera nada, uma vez que seus argumentos posicionais se esgotam.

O console agora deve mostrar o seguinte texto:

Meu nome é Monty Python.
Output

Nota: nenhum caracter de nova linha foi enviado para a saída.

A string atribuída ao argumento da palavra-chave end pode ter qualquer comprimento. Experimente se quiser.

Dissemos anteriormente que a função print() separa seus argumentos em saída com espaços. Esse comportamento também pode ser alterado.

O argumento da palavra -chave que pode fazer isso é nomeado sep (como no separador).

Veja o código no editor e execute-o.

Console

O argumento sep fornece os seguintes resultados:

Meu-nome-é-Monty-Python.
Output

A função print() agora usa um traço, em vez de um espaço, para separar os argumentos de saída.

Nota: o valor do argumento sep também pode ser uma string vazia. Experimente.

Ambos os argumentos de palavra-chave podem ser misturados em uma chamada, como aqui na janela do editor.

Console

O exemplo não faz muito sentido, mas apresenta visivelmente as interações entre end e sep.

Você consegue prever a saída?

Execute o código e veja se ele corresponde às suas previsões.

Agora que você entende a função print(), está pronto para pensar em como armazenar e processar dados em Python.

Sem a print(), você não seria capaz de ver nenhum resultado.

Incompleta 2.1.12   LAB   A função print() e seus argumentos
## 2.1.12   LAB   A função print() e seus argumentos
Cenário

Modifique a primeira linha de código no editor, usando as palavras-chave sep e end, para corresponder à saída esperada. Use as duas funções print() no editor.

Não altere nada na segunda invocação de print().
Saída esperada

Programação***Essenciais***em...Python
 
Output

Console

Incompleta 2.1.13   LAB   Formatação de saída
2.1.13   LAB   Formatação de saída
Cenário

Recomendamos que você brinque com o código que escrevemos para você e faça algumas alterações (talvez até destrutivas). Sinta-se livre para modificar qualquer parte do código, mas há uma condição: aprender com seus erros e tirar suas próprias conclusões.

Tente:

    minimizar o número de invocações de função print() inserindo a sequência \n nas strings;
    aumentar a flecha duas vezes (mas manter as proporções)
    duplique a seta, colocando as duas setas lado a lado; observação: uma string pode ser multiplicada usando o seguinte truque: "string" * 2 produzirá "stringstring" (falaremos sobre isso em breve)
    remova qualquer uma das aspas e analise com cuidado a resposta do Python; preste atenção onde Python vê um erro - este é o lugar onde o erro realmente existe?
    faça o mesmo com alguns parênteses;
    altere qualquer uma das palavras Print em algo diferente, diferindo apenas no caso (por exemplo, Print) - o que acontece agora?
    substitua algumas aspas por apóstrofos; veja o que acontece com cuidado.


Console



## 2.1.14 RESUMO DA SEÇÃO


1. A função print() é uma função interna. Ele imprime/envia uma mensagem especificada para a tela/janela do console.

2. As funções incorporadas, ao contrário das funções definidas pelo usuário, estão sempre disponíveis e não precisam ser importadas. O Python 3.8 vem com 69 funções integradas. Você pode encontrar a lista completa fornecida em ordem alfabética na Python Standard Library.

3. Para chamar uma função (este processo é conhecido como chamada de função ou invocação de função), você precisa usar o nome da função seguido de parênteses. Você pode passar argumentos para uma função colocando-os dentro dos parênteses. Você deve separar os argumentos com uma vírgula, por exemplo, print("Olá,", "world!"). Um print() vazio imprime uma linha vazia na tela.

4. Strings no Python são delimitadas por aspas, por exemplo, "eu sou um barbante" (aspas duplas), ou 'eu sou um barbante, demasiado' (aspas simples).

5. Programas de computador são uma coleção de instruções. Uma instrução é um comando para executar uma tarefa específica quando executado, por exemplo, para imprimir uma determinada mensagem na tela.

6. Em Strings do Python a barra invertida (\) é um caracter especial que anuncia que o próximo caracter terá um significado diferente, por exemplo, \n (o caracter de nova linha) inicia uma nova linha de saída.

7. Argumentos posicionais são aqueles cujo significado é ditado por sua posição, por exemplo, o segundo argumento é gerado após o primeiro, o terceiro é gerado após o segundo, etc.

8. Argumentos de palavras-chave são aqueles cujo significado não é ditado por sua localização, mas por uma palavra especial (palavra-chave) usada para identificá-los.

9. Os parâmetros end e sep podem ser utilizadas para formatar a saída do print(). O parâmetro sep especifica o separador entre os argumentos de saída, por exemplo, print("H", "E", "L", "L", "O", sep="-"), enquanto o parâmetro end especifica o que imprimir no final da impressão.

---

## Testes da seção


https://skillsforall.com/launch?id=c889bca7-0c31-4ee6-9424-bc709fe7be92&tab=curriculum&view=596f3118-37b2-5fd3-b582-fd2af3ce9884

---


# 2.2 Seção 2 - Literais Python

Bem-vindo à seção dois, onde falaremos sobre literais em Python.

### 2.2.1 Literais - os dados em si

Agora que você tem um pouco de conhecimento de alguns dos recursos poderosos oferecidos pela função print(), é hora de aprender sobre alguns novos problemas e um novo termo importante - o literal.

Um literal são dados cujos valores são determinados pelo próprio literal.

Como esse é um conceito difícil de entender, um bom exemplo pode ser útil.

Veja o seguinte conjunto de dígitos:

123

Você consegue adivinhar qual valor representa? Claro que você pode - são cento e vinte e três.

Mas e quanto a isso:

c

Isso representa algum valor? Talvez. Pode ser o símbolo da velocidade da luz, por exemplo. Também pode ser a constante de integração. Ou até mesmo o comprimento de uma hipotenusa no sentido de um teorema de Pitágoras. Há muitas possibilidades.

Você não pode escolher o caminho certo sem algum conhecimento adicional.

E esta é a pista: 123 é um literal e c não é.

Você usa literais para codificar dados e colocá-los em seu código. Vamos agora mostrar algumas convenções que você deve seguir ao usar o Python.

Vamos começar com uma experiência simples: dê uma olhada no snippet no editor.

Console

A primeira linha parece familiar. A segunda parece estar errada devido à visível falta de aspas.

Tente executá-lo.

Se tudo correr bem, agora você verá duas linhas idênticas.

O que aconteceu? O que isso significa?

Neste exemplo, você encontrará dois tipos diferentes de literais:

    uma string, que você já conhece,
    e um número inteiro, algo completamente novo.

A função print() os apresenta exatamente da mesma maneira ‒ este exemplo é óbvio, pois sua representação legível por humanos também é a mesma. Internamente, na memória do computador, esses dois valores são armazenados de formas completamente diferentes ‒ a string existe apenas como uma string ‒ uma série de letras.

O número é convertido em representação de máquina (um conjunto de bits). A função print() é capaz de mostrar ambos em um formato legível para humanos.

Agora vamos passar algum tempo discutindo literais numéricos e sua vida interna.
Concluído 2.2.2 Inteiros
2.2.2 Inteiros

Você já deve saber um pouco sobre como os computadores realizam cálculos em números. Talvez você já tenha ouvido falar do sistema binário e saiba que é o sistema que os computadores usam para armazenar números e que esses computadores podem realizar qualquer operação neles.

Não exploraremos as complexidades dos sistemas numéricos de posição aqui, mas vamos dizer que os números manipulados por computadores modernos são de dois tipos:

    inteiros, ou seja, aqueles que são desprovidos da parte fracionária;
    e números de ponto flutuante (ou simplesmente float), que contêm (ou são capazes de conter) a parte fracionária.

Essa definição não é totalmente precisa, mas é suficiente por enquanto. A distinção é muito importante, e a fronteira entre esses dois tipos de números é muito rigorosa. Esses dois tipos de números diferem significativamente na forma como são armazenados na memória do computador e na faixa de valores aceitáveis.

A característica do valor numérico que determina seu tipo, intervalo e aplicação é chamada de tipo.

Se você codificar um literal e o colocar dentro do código Python, a forma do literal determinará a representação (tipo) que o Python usará para armazená-lo na memória.

Por enquanto, vamos deixar os números de ponto flutuante de lado (vamos voltar para eles em breve) e considerar a questão de como o Python reconhece números inteiros.

O processo é quase como se você os escrevesse com um lápis no papel - é simplesmente uma sequência de dígitos que compõe o número. Mas há uma reserva - você não deve inserir caracteres que não sejam dígitos dentro do número.

Tomemos, por exemplo, o número onze milhões cento e onze mil cento e onze. Se você pegasse um lápis na mão agora, escreveria o número assim: 11,111,111, ou assim: 11.111.111, ou até mesmo assim: 11 111 111.

É claro que essa disposição facilita a leitura, especialmente quando o número consiste em muitos dígitos. No entanto, o Python não aceita coisas como essas. É proibido. O que o Python permite, porém, é o uso de sublinhados em literais numéricos.*

Portanto, você pode escrever este número da seguinte forma: 11111111 ou desta forma: 11_111_111.

  Observação     *O Python 3.6 introduziu sublinhados em literais numéricos, permitindo a colocação de sublinhamentos únicos entre dígitos e especificadores de base para melhorar a legibilidade. Esse recurso não está disponível em versões mais antigas do Python.

E como codificamos números negativos em Python? Como de costume - adicionando um sinal de menos. Você pode escrever: -11111111 ou -11_111_111.

Os números positivos não precisam ser precedidos pelo sinal de mais, mas é permitido, se você quiser fazer isso. As seguintes linhas descrevem o mesmo número: +11111111 e 11111111.
Números octais e hexadecimais

Há duas convenções adicionais em Python que são desconhecidas para o mundo da matemática. A primeira nos permite usar números em uma representação octal.

Se um número inteiro for precedido por um prefixo 0O ou 0o (zero-o), ele será tratado como um valor octal. Isso significa que o número deve conter dígitos retirados apenas do intervalo [0..7].

0o123 é um número octal com um valor (decimal) igual a 83.

A função print() faz a conversão automaticamente. Tente isto:

print(0o123)
 

A segunda convenção nos permite usar números hexadecimais. Esses números devem ser precedidos pelo prefixo 0x ou 0X (zero-x).

0x123 é um número hexadecimal com um valor (decimal) igual a 291. A função print() também pode gerenciar esses valores. Tente isto:

Console

Concluído 2.2.3 Floats
2.2.3 Floats

Agora é hora de falar sobre outro tipo, que é projetado para representar e armazenar os números que (como diria um matemático) têm uma fração decimal não vazia.

Eles são os números que têm (ou podem ter) uma parte fracionária após o ponto decimal e, embora essa definição seja muito ruim, certamente é suficiente para o que queremos discutir.

Sempre que usamos um termo como dois e meio ou menos o ponto zero quatro, pensamos em números que o computador considera números de ponto flutuante:

2.5
-0.4

Nota: dois e meio parecem normais quando você o escreve em um programa, embora se o seu idioma nativo preferir usar vírgula em vez de um ponto no número, você deve garantir que seu número não contenha nenhuma vírgula.

O Python não aceitará isso, ou (em casos muito raros, mas possíveis) pode interpretar mal suas intenções, pois a própria vírgula tem seu próprio significado reservado em Python.

Se você quiser usar apenas um valor de dois e meio, escreva-o como mostrado acima. Observe mais uma vez: há um ponto entre 2 e 5, não uma vírgula.

Como você provavelmente pode imaginar, o valor de zero ponto quatro poderia ser escrito em Python como:
0.4

Mas não se esqueça desta regra simples - você pode omitir zero quando for o único dígito antes ou depois da vírgula.

Em essência, você pode escrever o valor 0.4 como:
.4

Por exemplo: o valor de 4.0 pode ser escrito como:
4.

Isso não mudará seu tipo nem seu valor.
Int e. flutua

O ponto decimal é essencial para reconhecer números de ponto flutuante no Python.

Veja estes dois números:

4
4.0

Você pode pensar que eles são exatamente iguais, mas Python os vê de uma maneira completamente diferente.

4 é um número inteiro, enquanto 4.0 é um número de ponto flutuante.

O ponto é o que faz um ponto flutuante.

Por outro lado, não são apenas os pontos que fazem um float. Você também pode usar a letra e.

Quando você quiser usar números muito grandes ou muito pequenos, use notação científica.

Veja, por exemplo, a velocidade da luz, expressa em metros por segundo. Escrito diretamente, ficaria assim: 300000000.

Para evitar escrever tantos zeros, os livros de física usam uma forma abreviada, que você provavelmente já viu: 3 x 108.

Diz: Três vezes dez à potência de oito.

Em Python, o mesmo efeito é obtido de uma maneira ligeiramente diferente - veja:
3E8

A letra E (você também pode usar a letra minúscula e - vem da palavra expoente) é um registro conciso da frase vezes dez à potência de.

Nota:

    o expoente (o valor após o E) tem que ser um número inteiro;
    a base (o valor na frente do E) pode ser um número inteiro ou um valor flutuante.

Codificação de flutuantes

Vamos ver como essa convenção é usada para registrar números muito pequenos (no sentido de seu valor absoluto, que é próximo de zero).

Uma constante física chamada constante de Planck (e indicada como h), de acordo com os livros didáticos, tem o valor de: 6,62607 x 10-34.

Se você gostaria de usá-lo em um programa, escreva desta forma:
6.62607E-34

Nota: o fato de você ter escolhido uma das formas possíveis de codificação de valores flutuantes não significa que o Python a apresentará da mesma forma.

Às vezes, o Python pode escolher uma notação diferente da sua.

Por exemplo, digamos que você decidiu usar o seguinte literal de flutuação:
0.0000000000000000000001

Quando você executa esse literal pelo Python:

print(0.0000000000000000000001)
 
Output

esse é o resultado:

1e-22
Output

O Python sempre escolhe a forma mais econômica de apresentação do número, e você deve levar isso em consideração ao criar literais.
Incompleta 2.2.4 Strings
2.2.4 Strings

Strings são usadas quando você precisa processar texto (como nomes de todos os tipos, endereços, romances, etc.), não números.

Você já sabe um pouco sobre eles, por exemplo, que strings precisam de aspas assim como floats precisam de pontos.

Esta é uma string muito típica: "Eu sou uma string."

No entanto, há um porém. O problema é como codificar uma citação dentro de uma string que já está delimitada por aspas.

Vamos supor que queremos imprimir uma mensagem bem simples dizendo:
Eu gosto de "Monty Python"

Como fazemos isso sem gerar um erro? Há duas soluções possíveis.

A primeira é baseada no conceito que já conhecemos do caractere de escape, que você deve lembrar que é representado pela barra invertida. A barra invertida também pode escapar das aspas. Uma citação precedida por uma barra invertida muda seu significado ‒ não é um delimitador, mas apenas uma citação. Isso funcionará como pretendido:

print("Eu gosto \"Monty Python\"")
 

Nota: há duas aspas com escape dentro da string - você consegue ver as duas?

A segunda solução pode ser um pouco surpreendente. O Python pode usar um apóstrofo em vez de uma aspas. Qualquer um desses caracteres pode delimitar cadeias de caracteres, mas você deve ser coerente.

Se você abrir uma sequência com aspas, será necessário fechá-la com aspas.

Se você iniciar uma sequência de caracteres com um apóstrofo, precisará terminá-la com um apóstrofo.

Este exemplo também funcionará:

print('Eu gosto "Monty Python"')
 

Nota: você não precisa de usar escape aqui.
Codificando strings

Agora, a próxima pergunta é: como você incorpora um apóstrofo em uma string colocada entre apóstrofos?

Você já deve saber a resposta ou, para ser mais preciso, duas respostas possíveis.

Tente imprimir uma string contendo a seguinte mensagem:
Eu sou Monty Python.

Console

Você sabe como fazê-lo? Clique na Check abaixo para ver se você estava certo:

Como você pode ver, a barra invertida é uma ferramenta muito poderosa - ela pode escapar não apenas de aspas, mas também de apóstrofes.

Já mostramos isso, mas queremos enfatizar mais uma vez esse fenômeno: uma string pode estar vazia - pode não conter caracteres.

Uma string vazia ainda permanece uma string:

''
""

Incompleta 2.2.5 Valores booleanos
2.2.5 Valores booleanos

Para concluir com os literais do Python, há dois adicionais.

Elas não são tão óbvias quanto as anteriores, pois são usadas para representar um valor muito abstrato - a veracidade.

Cada vez que você pergunta ao Python se um número é maior que outro, a pergunta resulta na criação de alguns dados específicos - um valor booleano.

O nome vem de George Boole (1815-1864), autor da obra fundamental, The Laws of Thought, que contém a definição de álgebra booleana ‒ uma parte da álgebra que faz uso de apenas dois valores distintos: True e False, denotados como 1 e 0.

Um programador cria um programa, e o programa faz perguntas. Python executa o programa e fornece as respostas. O programa deve ser capaz de reagir de acordo com as respostas recebidas.

Felizmente, os computadores sabem apenas dois tipos de respostas:

    Sim, isso é verdade;
    Não, isso é falso.

Você nunca receberá uma resposta como: Não sei ou Provavelmente sim, mas não tenho certeza.

Python, então, é um réptil binário.

Esses dois valores booleanos têm denotações estritas em Python:
True
False

Você não pode mudar nada. É necessário aceitar esses símbolos como eles são, inclusive distinção entre maiúsculas e minúsculas.

Desafio: Qual será a saída do trecho de código a seguir?

print(True > False)
print(True < False)
 

Execute o código no editor para verificar. Você pode explicar o resultado?

Console


Incompleta 2.2.6   LAB   Literais Python - strings
2.2.6   LAB   Literais Python - strings
Cenário

Escreva um código de uma linha usando a função de print(), bem como os caracteres de nova linha e de escape, para corresponder ao resultado esperado gerado em três linhas.
Saída esperada

"Eu sou"
""aprendizado""
"""Python"""
Output

Console

Incompleta
2.2.7 RESUMO DA SEÇÃO
## 2.2.7 RESUMO DA SEÇÃO

1. Literais são notações para representar alguns valores fixos no código. Python tem vários tipos de literais - por exemplo, um literal pode ser um número (literais numéricos, por exemplo, 123) ou uma string (literais de string, por exemplo, "Eu sou um literal".).

2. O sistema binário é um sistema de números que emprega 2 como base. Portanto, um número binário é composto de 0s e 1s apenas, por exemplo, 1010 é 10 em decimal.
Os sistemas de numeração octal e hexadecimal, da mesma forma, empregam 8 e 16 como suas bases respectivamente. O sistema hexadecimal usa os números decimais e seis letras extras.

3. Inteiros (ou simplesmente ints) são um dos tipos numéricos compatíveis com o Python. São números escritos sem um componente fracionário, por exemplo, 256 ou -1 (números inteiros negativos).

4. Ponto flutuante (ou simplesmente float) são outro dos tipos numéricos compatíveis com o Python. São números que contêm (ou são capazes de conter) um componente fracionário, por exemplo, 1.27.

5. Para codificar um apóstrofo ou uma aspas dentro de uma string, você pode usar o caracter de escape, por exemplo, 'I\'m happy.' ou abrir e fechar a string usando um conjunto oposto de símbolos aos que você deseja codificar, por exemplo, "I'm happy." para codificar um apóstrofo e 'Ele disse "Python", não "typhoon"' para codificar uma aspas (dupla).

6. Valores booleanos são os dois objetos constantes True e False usados para representar valores de verdade (em contextos numéricos, 1 é True, enquanto 0 é False.

  Extra  

Há mais um literal especial usado em Python: o literal None. Esse literal é um objeto NoneType e é usado para representar a ausência de um valor. Vamos contar mais sobre isso em breve.

