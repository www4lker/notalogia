---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/latam-2023-11-secao-1-introducao-a-programacao/","tags":["python","teoria","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# LATAM 2023-11 Seção 1 - Introdução à programação

## criado em: 
-  02-05-2023 - 17:47

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM Bem-vindo ao Fundamentos do Python\|LATAM Bem-vindo ao Fundamentos do Python]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Maratona LATAM 2023_PYTHON_SENAC\|Maratona LATAM 2023_PYTHON_SENAC]]
- tags: #python #teoria #ANELO 
- Fontes & Links: https://pythoninstitute.org/pcep
- [wiki python](https://wiki.python.org/moin/PythonImplementations)

---

Olá, bem-vindos à seção um! Começaremos aprendendo sobre alguns dos conceitos universais de programação, como lista de instruções, arquivo de origem, elementos de linguagem, compilação e interpretação. Vamos lá? Vamos começar!

## 1.1.1 Como funciona um programa de computador?

Um programa torna um computador utilizável. Sem um programa, um computador, mesmo o mais poderoso, não passa de um objeto. Da mesma forma, sem um jogador, um piano nada mais é do que uma caixa de madeira.

Os computadores são capazes de executar tarefas muito complexas, mas essa capacidade não é inata. A natureza de um computador é bem diferente.

Ele pode executar apenas operações extremamente simples. Por exemplo, um computador não consegue entender sozinho o valor de uma função matemática complicada, embora isso não esteja além dos limites das possibilidades no futuro próximo.

Os computadores contemporâneos só podem avaliar os resultados de operações muito fundamentais, como adicionar ou dividir, mas podem fazer isso com muita rapidez e podem repetir essas ações praticamente várias vezes.

Imagine que você quer saber a velocidade média que atingiu durante uma longa jornada. Você sabe a distância, você sabe o tempo, você precisa da velocidade.

Naturalmente, o computador poderá calcular isso, mas não está ciente de coisas como distância, velocidade ou tempo. Portanto, é necessário instruir o computador para:

    aceitar um número que represente a distância;
    aceitar um número que represente o tempo de viagem;
    divida o valor anterior pelo último e armazene o resultado na memória;
    exibem o resultado (representando a velocidade média) em um formato legível.

Essas quatro ações simples formam um programa. Obviamente, esses exemplos não são formalizados e estão muito longe do que o computador pode entender, mas são bons o suficiente para serem traduzidos para um idioma que o computador possa aceitar.

Linguagem é a palavra-chave.
### Concluída 1.1.2 Linguagens naturais vs. linguagens de programação
1.1.2 Linguagens Naturais vs Linguagens de Programação

Uma linguagem é um meio (e uma ferramenta) para expressar e registrar pensamentos. Há muitos idiomas ao nosso redor. Alguns deles não exigem fala nem escrita, como a linguagem corporal; é possível expressar seus sentimentos mais profundos sem dizer uma palavra.

Outra linguagem que você usa todos os dias é a sua língua nativa, que você usa para manifestar sua vontade e refletir sobre a realidade. Os computadores também têm sua própria linguagem, chamada de linguagem de máquina, o que é muito rudimentar.

Um computador, mesmo o mais tecnicamente sofisticado, não tem nem um traço de inteligência. Você pode dizer que é como um cão bem treinado - responde apenas a um conjunto predeterminado de comandos conhecidos.

Os comandos que ele reconhece são muito simples. Podemos imaginar que o computador responde a pedidos como "pegue esse número, divida por outro e salve o resultado".

Um conjunto completo de comandos conhecidos é chamado de lista de instruções, às vezes abreviada para IL (instrunction list). Diferentes tipos de computadores podem variar de acordo com o tamanho das ILs, e as instruções podem ser completamente diferentes em modelos diferentes.

Observação: linguagens de máquina são desenvolvidas por seres humanos.

Nenhum computador é capaz de criar um novo idioma no momento. No entanto, isso pode mudar em breve. Assim como as pessoas usam vários idiomas diferentes, as máquinas também têm muitos idiomas diferentes. A diferença, no entanto, é que as linguagens humanas se desenvolveram naturalmente.

Além disso, eles ainda estão evoluindo, e novas palavras são criadas todos os dias à medida que palavras antigas desaparecem. Esses idiomas são chamados de linguagens naturais.
Incompleta 1.1.3 O que torna uma linguagem?

## 1.1.3 O que faz uma linguagem?

![Pasted image 20230502175329.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230502175329.png)
![Pasted image 20230502175336.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230502175336.png)
![Pasted image 20230502175348.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230502175348.png)
![Pasted image 20230502175359.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230502175359.png)

Podemos dizer que cada linguagem (máquina ou natural, não importa) consiste nos seguintes elementos:
Concluída 1.1.4 Linguagem de máquina vs. linguagem de alto nível

## 1.1.4 Linguagem da máquina vs. linguagem de alto nível

A IL é, na verdade, o alfabeto de uma linguagem de máquina. Este é o conjunto de símbolos mais simples e primário que podemos usar para dar comandos a um computador. É a língua nativa do computador.

Infelizmente, essa língua nativa está muito longe de ser a língua nativa humana. Nós dois (computadores e seres humanos) precisamos de algo mais, uma linguagem comum para computadores e seres humanos, ou uma ponte entre os dois mundos diferentes.

Precisamos de uma linguagem na qual os humanos possam escrever seus programas e de uma linguagem que os computadores possam usar para executar os programas, uma linguagem que é muito mais complexa do que a linguagem de máquina e, no entanto, muito mais simples do que a linguagem natural.

Essas linguagens são frequentemente chamadas de linguagens de programação de alto nível. Eles são pelo menos um pouco semelhantes aos naturais, pois usam símbolos, palavras e convenções legíveis para os seres humanos. Essas linguagens permitem que seres humanos expressem comandos para computadores que são muito mais complexos do que aqueles oferecidos por ILs.

Um programa escrito em uma linguagem de programação de alto nível é chamado de código-fonte (em contraste com o código de máquina executado por computadores). Da mesma forma, o arquivo que contém o código-fonte é chamado de arquivo-fonte.


## 1.1.5 Compilação vs. interpretação

A programação de computadores é o ato de compor os elementos da linguagem de programação selecionada na ordem que causará o efeito desejado. O efeito pode ser diferente em cada caso específico - depende da imaginação, do conhecimento e da experiência do programador.

Obviamente, essa composição precisa ser correta em muitos sentidos:

    em ordem alfabética - um programa precisa ser escrito em um script reconhecível, como romano, cirílico etc.
    lexicamente - cada linguagem de programação tem seu dicionário e você precisa dominá-lo; felizmente, é muito mais simples e menor do que o dicionário de qualquer linguagem natural;
    sintaticamente - cada idioma tem suas regras e elas devem ser obedecidas;
    semanticamente - o programa tem que fazer sentido.

Infelizmente, um programador também pode cometer erros com cada um dos quatro sentidos acima. Cada um deles pode tornar o programa completamente inútil.

![Pasted image 20230502175921.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230502175921.png)
![Pasted image 20230502175929.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230502175929.png)
Due to some very fundamental reasons, a particular high-level programming language is designed to fall into one of these two categories.

There are very few languages that can be both compiled and interpreted. Usually, a programming language is projected with this factor in its constructors' minds – will it be compiled or interpreted?

## 1.1.6 What does the interpreter do?

Vamos supor que você tenha escrito um programa com sucesso. Como convencer o computador a executá-lo? Você precisa tornar o programa em linguagem de máquina. Felizmente, a tradução pode ser feita por um computador, tornando todo o processo rápido e eficiente.

Há duas maneiras diferentes de transformar um programa de uma linguagem de programação de alto nível em linguagem de máquina:
This component is a flipcard comprised of flippable cards containing display image. Select the front face image to flip to the back face of these card to display associated text.
Clique nas imagens para saber mais sobre as diferenças entre compilação e interpretação.

Compilação - o programa de origem é convertido uma vez (no entanto, esse ato deve ser repetido cada vez que você modifica o código-fonte) ao obter um arquivo (por exemplo, um arquivo an .exe se o código for executado no MS Windows) contendo a máquina código. Agora você pode distribuir o arquivo em todo o mundo; o programa que executa essa conversão é chamado de compilador ou traduzir.

Interpretação - você (ou qualquer usuário do código) pode traduzir o programa de origem toda vez que ele tiver que ser executado. O programa que executa esse tipo de transformação é chamado de interpretador, pois interpreta o código toda vez que se destina a ser executado. Isso também significa que você não pode apenas distribuir o código-fonte como está, porque o usuário final também precisa que o intérprete o execute.

Devido a algumas razões fundamentais, uma determinada linguagem de programação de alto nível foi projetada para se enquadrar em uma dessas duas categorias.

Existem muito poucas linguagens que podem ser compiladas e interpretadas. Normalmente, uma linguagem de programação é projetada com esse fator na mente de seus construtores - será compilada ou interpretada?

---

Vamos supor mais uma vez que você escreveu um programa. Agora, ele existe como um arquivo de computador: um programa de computador é na verdade um pedaço de texto, então o código-fonte geralmente é colocado em arquivos de texto.

Observação: ele precisa ser texto puro, sem nenhuma decoração, como fontes diferentes, cores, imagens incorporadas ou outras mídias. Agora você precisa chamar o intérprete e permitir que ele leia o arquivo de origem.

O intérprete lê o código-fonte de uma forma comum na cultura ocidental: da parte superior para a inferior e da esquerda para a direita. Há algumas exceções - elas serão abordadas mais adiante neste curso.

Primeiro de tudo, o intérprete verifica se todas as linhas subsequentes estão corretas (usando os quatro aspectos abordados anteriormente).

Se o compilador encontrar um erro, ele terminará o trabalho imediatamente. O único resultado nesse caso é uma mensagem de erro.

O intérprete informará onde o erro está localizado e o que o causou. No entanto, essas mensagens podem ser enganosas, pois o intérprete não é capaz de seguir suas intenções exatas e pode detectar erros a alguma distância de suas causas reais.

Por exemplo, se você tentar usar uma entidade de nome desconhecido, ela causará um erro, mas o erro será descoberto no local em que tenta usar a entidade, e não onde o nome da nova entidade foi introduzido.

Em outras palavras, o motivo real geralmente está localizado um pouco mais cedo no código, por exemplo, no lugar onde você tinha que informar o intérprete que você usaria a entidade do nome.

Se a linha parece boa, o intérprete tenta executá-la (observação: cada linha é geralmente executada separadamente, para que o "leitura-verificação-execute" do grupo possa ser repetido muitas vezes - mais vezes do que o número real de linhas no arquivo de origem ,, pois algumas partes do código podem ser executadas mais de uma vez).

Também é possível que uma parte significativa do código seja executada com sucesso antes que o intérprete encontre um erro. Esse é o comportamento normal neste modelo de execução.

Você pode perguntar agora: qual é o melhor? O modelo de "compilação" ou o modelo de "interpretação"? Não há uma resposta óbvia. Se houvesse, um desses modelos teria deixado de existir há muito tempo. Ambos têm suas vantagens e desvantagens.
## 1.1.7 Compilação vs. Interpretação - Vantagens e Desvantagens

![Pasted image 20230502180953.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230502180953.png)

	Compilação 	Interpretação
Vantagens
Compilação 

    ✓ a execução do código convertido é mais rápida;
    ✓ apenas o usuário precisa ter o compilador - o usuário final pode usar o código sem ele;
    ✓ o código traduzido é armazenado usando linguagem de máquina - como é muito difícil de entender, suas próprias invenções e truques de programação provavelmente permanecerão em segredo.

Interpretação

    ✓ você pode executar o código assim que tiver concluído - não há fases adicionais de conversão;
    ✓ o código é armazenado usando linguagem de programação, e não linguagem de máquina - isso significa que pode ser executado em computadores que usam linguagens de máquina diferentes; você não compila seu código separadamente para cada arquitetura.

Desvantagens
Compilação 

    ❌ a compilação em si pode ser um processo muito demorado - talvez você não consiga executar o código imediatamente após fazer uma alteração;
    ❌ você precisa ter tantos compiladores quanto plataformas de hardware nas quais deseja que seu código seja executado.

	
Interpretação

    ❌ não espere que a interpretação aumente seu código a alta velocidade - seu código vai compartilhar a capacidade do computador com o intérprete, então não pode ser muito rápido;
    ❌ Você e o usuário final precisam ter o intérprete para executar o código.


O que tudo isso significa para você?

- Python - como você deve ter certeza - é uma linguagem interpretada. Isso significa que ele herda todas as vantagens e desvantagens descritas. Obviamente, ele adiciona alguns de seus recursos exclusivos aos dois conjuntos.
- Se você quiser programar em Python, precisará do interpretador Python. Você não poderá executar seu código sem ele. Felizmente, o Python é gratuito. Essa é uma das vantagens mais importantes.

Devido a razões históricas, as linguagens projetadas para serem utilizadas na maneira de interpretação são frequentemente chamadas de linguagens de script (**scripting languages**), enquanto os programas de origem codificados usando-as são chamados de **scripts**. Ok, vamos conhecer Python.

---

# 1.2 Seção 2 - Introdução a Python

O que é Python?
![0b3914465393760842b337cfb38a22c53e356b06.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/0b3914465393760842b337cfb38a22c53e356b06.png)

Python é uma linguagem de programação amplamente usada, interpretada, orientada a objeto e de alto nível com semântica dinâmica, usada para programação de uso geral.

E embora você possa conhecer a píton como uma cobra grande, o nome da linguagem de programação Python vem de uma antiga série de comédia da BBC chamada Monty Python's Flying Circus.

No auge do sucesso, a equipe de Monty Python estava realizando seus esboços para viver audiências em todo o mundo, inclusive no Hollywood Bowl.

Como Monty Python é considerado um dos dois principais elementos essenciais para um programador (o outro é pizza), o criador do Python nomeou a linguagem em homenagem ao programa de TV.

Concluída 1.2.2 Quem criou o Python?

## 1.2.2 Quem criou Python?

Um dos recursos surpreendentes do Python é o fato de que ele é realmente o trabalho de uma pessoa. Normalmente, novas linguagens de programação são desenvolvidas e publicadas por grandes empresas que empregam muitos profissionais e, devido às regras de direitos autorais, é muito difícil nomear qualquer uma das pessoas envolvidas no projeto. Python é uma exceção.

Não há muitos idiomas cujos autores sejam conhecidos pelo nome. Python foi criada por Guido van Rossum, nascida em 1956 em Haarlem, na Holanda. Claro, Guido van Rossum não desenvolveu e evoluiu todos os componentes do Python...

A velocidade com que o Python se espalhou pelo mundo é resultado do trabalho contínuo de milhares (muitas vezes anônimos) programadores, testadores, usuários (muitos deles não são especialistas em TI) e entusiastas, mas é preciso dizer que os a primeira ideia (a semente da qual Python brotou) veio à tona - o de Guido.
Concluída 1.2.3 Um projeto de programação por hobby
## 1.2.3 Um projeto de programação de hobby

As circunstâncias em que o Python foi criado são um pouco intrigantes. De acordo com Guido van Rossum:

    Em dezembro de 1989, eu estava procurando por um projeto de programação "hobby" que me mantivesse ocupado durante a semana por volta do Natal. Meu escritório (...) ficava fechado, mas eu tinha um computador em casa e não muito mais. Decidi escrever um intérprete para a nova linguagem de script em que tenho pensado ultimamente: um descendente da ABC que agradaria a hackers Unix/C. Eu escolhi o Python como um título de trabalho para o projeto, por ser um pouco irreverente (e um grande fã de Circo Voador de Monty Python). Guido van Rossum

Objetivos do Python

Em 1999, Guido van Rossum definiu seus objetivos para o Python:

    uma linguagem fácil e intuitiva, tão eficiente quanto a dos grandes concorrentes;
    código aberto, para que qualquer pessoa possa contribuir com seu desenvolvimento;
    código tão compreensível quanto o simples inglês;
    adequado para tarefas diárias, permitindo tempos de desenvolvimento curtos.

Cerca de 20 anos depois, fica claro que todas essas intenções foram cumpridas. Algumas fontes dizem que Python é a linguagem de programação mais popular do mundo, enquanto outras afirmam que é a segunda ou a terceira.

De qualquer forma, ele ainda ocupa uma posição alta entre os dez primeiros da Popularidade de Linguagem de Programação PYPL e do Índice da Comunidade de Programação TIOBE.

Python não é mais uma linguagem jovem. É maduro e confiável. Não é de admirar. É uma estrela no firmamento de programação, e o tempo gasto aprendendo Python é um investimento muito bom.
Concluída 1.2.4 O que torna o Python tão especial?
## 1.2.4 O que torna o Python tão especial?
Concluída 1.2.4 O que torna o Python tão especial?
### Por que Python?

Como é que os programadores, novos e antigos, experientes e iniciantes, querem usá-lo? Como aconteceu que as grandes empresas adotaram o Python e implementaram seus principais produtos usando-o?

Há muitas razões - listamos algumas delas já, mas vamos enumerá-las novamente de uma forma mais prática:

    É fácil de aprender - o tempo necessário para aprender Python é mais curto do que para muitas outras linguagens; isso significa que é possível iniciar a programação real mais rapidamente;
    é fácil de ensinar - a carga de trabalho de ensino é menor do que a necessária em outros idiomas; isso significa que o professor pode colocar mais ênfase nas técnicas de programação geral (independentes do idioma), não desperdiçando energia em truques exóticos, estranhas exceções e regras incompreensíveis;
    É fácil de usar para escrever novos softwares - muitas vezes é possível escrever código mais rápido ao usar Python;
    é fácil de entender - também é mais fácil entender o código de outra pessoa com mais rapidez, se for escrito em Python;
    É fácil de obter, instalar e implantar – Python é gratuito, aberto e multiplataforma; nem todas as linguagens podem se orgulhar disso.

Concluída 1.2.5 Rivais do Python?

### 1.2.5 Rivais do Python?

O Python tem dois concorrentes diretos, com propriedades e predisposições comparáveis. São eles:

    Perl - uma linguagem de script criada originalmente por Larry Wall;
    Ruby - uma linguagem de script criada por Yukihiro Matsumoto.

O primeiro é mais tradicional e mais conservador do que o Python, e se assemelha a algumas das linguagens antigas derivadas da linguagem de programação clássica C.

Em contrapartida, o último é mais inovador e mais cheio de novas ideias do que o Python. O próprio Python está em algum lugar entre essas duas criações.

A Internet está cheia de fóruns com discussões infinitas sobre a superioridade de um desses três sobre os outros, caso você queira saber mais sobre cada um deles.
Concluída 1.2.6 Onde podemos ver o Python em ação?
### 1.2.6 Onde podemos ver Python em ação?

Vemos isso todos os dias e quase em todos os lugares. É amplamente utilizado para implementar serviços de Internet complexos, como mecanismos de pesquisa, armazenamento em nuvem e ferramentas, mídias sociais e assim por diante. Sempre que você usa qualquer um desses serviços, você está muito próximo do Python, embora não saiba.

Muitas ferramentas de desenvolvimento são implementadas em Python. Cada vez mais aplicativos de uso diário estão sendo escritos em Python. Muitos cientistas abandonaram ferramentas proprietárias caras e mudaram para o Python. Muitos testadores de projeto de TI começaram a usar o Python para realizar procedimentos de teste repetíveis. A lista é longa.
Concluída 1.2.7 Por que não Python?

### 1.2.7 Por que não Python?

Apesar da crescente popularidade do Python, ainda há alguns nichos nos quais o Python está ausente ou é raramente visto:

    programação de baixo nível (às vezes chamada de programação "próxima ao metal"): se você quiser implementar um driver ou mecanismo gráfico extremamente eficaz, não usará Python;
    aplicativos para dispositivos móveis: embora esse território ainda esteja esperando para ser conquistado pelo Python, provavelmente acontecerá algum dia.

Incompleta 1.2.8 Há mais de um Python
### 1.2.8 Há mais de um python
Incompleta 1.2.8 Há mais de um python
#### Python 2 vs. Python 3

Existem dois tipos principais de Python, chamados Python 2 e Python 3.

Python 2 é uma versão mais antiga do Python original. Seu desenvolvimento foi intencionalmente interrompido, embora isso não signifique que não há atualizações para ele. Pelo contrário, as atualizações são emitidas regularmente, mas não pretendem modificar a linguagem de forma significativa. Eles preferem corrigir bugs e falhas de segurança recém-descobertos. O caminho de desenvolvimento do Python 2 já chegou a um impasse, mas o próprio Python 2 ainda está vivo.

Python 3 é a versão mais recente (ou para ser mais preciso, a atual) da linguagem. Ela está seguindo seu próprio caminho evolutivo, criando seus próprios padrões e hábitos.

Essas duas versões do Python não são compatíveis entre si. Os scripts Python 2 não serão executados em um ambiente Python 3 e vice-versa. Se você quiser que o código Python 2 antigo seja executado por um intérprete Python 3, a única solução possível é reescrevê-lo, não do zero, é claro, pois grandes partes do código podem permanecer intocadas, mas você precisa revisar todo o código para encontrar todas as incompatibilidades possíveis. Infelizmente, esse processo não pode ser totalmente automatizado.

É muito difícil, muito demorado, muito caro e muito arriscado migrar uma aplicação antiga do Python 2 para uma nova plataforma, e é até possível que a reescrita do código introduza novos bugs nela. É mais fácil e mais sensato deixar esses sistemas em paz e melhorar o intérprete atual, em vez de tentar trabalhar dentro do código-fonte que já está em funcionamento.

O Python 3 não é apenas uma versão melhor do Python 2 - é uma linguagem completamente diferente, embora muito semelhante ao seu antecessor. Quando você os observa à distância, eles parecem ser os mesmos, mas quando você olha de perto, você percebe muitas diferenças.

Se você estiver modificando uma solução Python antiga, é muito provável que ela tenha sido codificada em Python 2. Essa é a razão pela qual o Python 2 ainda está em uso. Há muitos aplicativos Python 2 para descartá-lo completamente.

  Observação  

Se você vai começar um novo projeto Python, deve usar o Python 3, e esta é a versão do Python que será usada durante este curso.

É importante lembrar que pode haver diferenças menores ou maiores entre as versões subsequentes do Python 3 (por exemplo, o Python 3.6 introduziu chaves de dicionário ordenadas por padrão na implementação do CPython) - a boa notícia é que todas as versões mais recentes do Python 3 são compatíveis com as versões anteriores do Python 3. Sempre que significativo e importante, sempre tentaremos destacar essas diferenças no curso.

Todos os exemplos de código que você encontrará durante o curso foram testados em Python 3.4, Python 3.6, Python 3.7, Python 3.8 e Python 3.9.
Concluída 1.2.9 Implementações de Python
### 1.2.9 Implementações de Python

Além de Python 2 e Python 3, há mais de uma versão de cada.

Seguindo a página wiki do Python, uma implementação do Python se refere a "um programa ou ambiente, que oferece suporte para a execução de programas escritos na linguagem Python, conforme representado pela implementação de referência do CPython".

A implementação tradicional do Python, chamada CPython, é a versão de referência da linguagem de computação Python de Guido van Rossum, e na maioria das vezes é chamada apenas de "Python". Quando você ouve o nome CPython, ele provavelmente é usado para diferenciá-lo de outras implementações alternativas não tradicionais.

Mas, primeiro, as coisas. Existem Pythons mantidos por pessoas reunidas em torno do PSF (Python Software Foundation), uma comunidade que tem como objetivo desenvolver, melhorar, expandir e popularizar o Python e seu ambiente. O presidente do PSF é o próprio Guido von Rossum e, por essa razão, esses Pythons são chamados de canônicos. Eles também são considerados Pythons de referência, pois qualquer outra implementação da linguagem deve seguir todos os padrões estabelecidos pelo PSF.

Guido van Rossum usou a linguagem de programação "C" para implementar a primeira versão de sua linguagem, e essa decisão ainda está em vigor. Todos os Pythons provenientes do PSF são escritos na linguagem "C". Há muitas razões para essa abordagem. Uma delas (provavelmente a mais importante) é que, graças a ela, o Python pode ser facilmente portado e migrado para todas as plataformas com a capacidade de compilar e executar programas de linguagem "C" (praticamente todas as plataformas têm esse recurso, o que abre muitas expansões oportunidades para o Python).
![Pasted image 20230502183119.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230502183119.png)

É por isso que a implementação do PSF é conhecida como CPython. Este é o Python mais influente entre todos os Pythons do mundo.

**Cython** é uma das possíveis soluções para a mais dolorosa das características da Python - a falta de eficiência. Cálculos matemáticos grandes e complexos podem ser facilmente codificados em Python (muito mais fácil do que em "C" ou em qualquer outra linguagem tradicional), mas a execução de código resultante pode ser extremamente demorada.

Como essas duas contradições são reconciliadas? Uma solução é escrever suas ideias matemáticas usando Python, e quando você tiver certeza absoluta de que seu código está correto e produz resultados válidos, você pode convertê-lo em "C". Certamente, "C" será executado muito mais rápido do que Python puro.

Isso é o que o Cython se destina a fazer para converter automaticamente o código Python (limpo e claro, mas não muito rápido) em código "C" (complicado e falante, mas ágil).

Outra versão do Python é chamada **Jython**.

"J" é para "Java". Imagine um Python escrito em Java em vez de C. Isso é útil, por exemplo, se você desenvolver sistemas grandes e complexos escritos inteiramente em Java e quiser adicionar alguma flexibilidade Python a eles. O CPython tradicional pode ser difícil de integrar a esse ambiente, pois C e Java vivem em mundos completamente diferentes e não compartilham muitas ideias comuns.

O Jython pode se comunicar com a infraestrutura Java atual com mais eficiência. É por isso que alguns projetos acham útil e necessário.

Observação: a implementação atual do Jython segue os padrões do Python 2. Até o momento, não há nenhum Jython em conformidade com o Python 3.

O logotipo do **PyPy** é um jogo de quebra-cabeça. Você pode resolver o problema? Isso significa: um Python dentro de um Python. Em outras palavras, ele representa um ambiente Python escrito em uma linguagem semelhante a Python chamada **RPython** (Python restrito). Na verdade, é um subconjunto do Python.

O código fonte do PyPy não é executado na maneira de interpretação, mas, em vez disso, é traduzido para a linguagem de programação C e executado separadamente.

Isso é útil porque se você quiser testar qualquer novo recurso que possa ser (mas não precise ser) introduzido na implementação principal do Python, é mais fácil verificar isso com o PyPy do que com o CPython. É por isso que o PyPy é mais uma ferramenta para as pessoas que desenvolvem o Python do que para o restante dos usuários.

Isso não torna o PyPy menos importante ou menos sério do que o CPython, é claro.

Além disso, o PyPy é compatível com a linguagem Python 3.

Há muito mais Pythons diferentes no mundo. Você os encontrará se olhar, mas **este curso se concentrará no CPython**.

O **MicroPython** é uma implementação eficiente de software de código aberto do Python 3, que é otimizada para ser executada em **microcontroladores**. Ele inclui um pequeno subconjunto da biblioteca padrão do Python, mas é amplamente embalado com um grande número de recursos, como prompt interativo ou números inteiros de precisão arbitrária, bem como módulos que dão ao programador acesso ao hardware de nível inferior.

Originalmente criado por Damien George, um programador australiano que, no ano de 2013, realizou uma campanha bem-sucedida no Kickstarter e lançou a primeira versão do MicroPython com uma placa de desenvolvimento baseada em STM32F4 chamada **pyboard**.

Em 2017, o MicroPython foi usado para criar o **CircuitPython**, outra linguagem de programação de código aberto executada no hardware do microcontrolador, que é um derivado da linguagem MicroPython.

# 1.3 Seção 3 - Download e instalação do Python

>Bem-vindo à seção três, onde falaremos sobre as formas de obter, instalar e configurar o Python no seu computador local. Esta seção é opcional, pois durante o curso você poderá iniciar, testar e experimentar todos os seus programas Python no **Edube Interactive TM**, o ambiente de programação que integramos à plataforma de aprendizagem e a esses recursos de estudo. Ainda assim, se você pode baixar e instalar o Python em sua máquina local, é altamente recomendável.


# 1.4 Conclusão do módulo 1 - Teste de módulo

Teste do Módulo 1

Muito bem! Você chegou ao final do Módulo 1 e concluiu um grande marco na sua formação em programação em Python. Aqui está um breve resumo das áreas de tópicos abordadas no Módulo 1:

-   os fundamentos da programação de computadores, ou seja, como o computador funciona, como o programa é executado, como a linguagem de programação é definida e construída;
-   a diferença entre compilação e interpretação;
-   as informações básicas sobre Python e como ele está posicionado entre outras linguagens de programação e o que distingue suas diferentes versões;
-   como obter, instalar e configurar o Python em sua máquina local.

Agora você está pronto para fazer o **teste do módulo**, o que ajudará a avaliar o que você aprendeu até agora.

O teste a seguir tem como base o que você acabou de aprender. Há dez perguntas no total e você precisa marcar pelo menos 70% para passar.

Boa sorte!
![Pasted image 20230502184721.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230502184721.png)
(Segunta tentativa)

[[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023 2 Seção 1 - O Programa Olá, mundo\|LATAM 2023 2 Seção 1 - O Programa Olá, mundo]]
