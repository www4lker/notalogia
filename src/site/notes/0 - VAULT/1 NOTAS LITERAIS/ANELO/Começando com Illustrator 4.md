---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/comecando-com-illustrator-4/","tags":["design","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Começando com Illustrator 4
## elementos finais e refinamentos
## criado em: 
-  20-04-2023 - 14:32

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Começando com Illustrator 3\|Começando com Illustrator 3]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Começando com Illustrator 5\|Começando com Illustrator 5]]
- tags: #design #ANELO
- Fontes & Links: 

---
### Nessa aula nós aprenderemos:

-   Opções avançadas do Image Trace;
-   Ferramenta de Pattern;
-   Blending Modes (modos de mesclagem de cor) para criar textura;
-   Inserir Drop Shadow para destacar elementos;

## aula 4.1

Seguiremos nosso projeto e importaremos, dessa vez, a imagem da atleta para a área de trabalho do Illustrator. Nessa etapa, aprenderemos a usar a ferramenta _Image Trace_. Para que essa fotografia da atleta tenha a nossa identidade visual, devemos realizar algumas modificações e ajustes. Queremos, ainda, que a imagem possa ser ampliada para que possamos usá-la em outros formatos, como um outdoor ou outra forma de marketing visual.

Para superar os limites da qualidade da imagem devemos vetorizá-la. No cabeçalho de ferramentas, selecionaremos "Window > Image Trace" . Teremos um painel de configurações da ferramenta, e na opção "Preset" selecionaremos "Low Fidelity". O Illustrator realizará a vetorização automática da imagem.

Começaremos, agora, a limpar o fundo da imagem, já que apenas a atleta nos interessa e não o cenário que ela está inclusa. Para tanto, limparemos vetor por vetor da paisagem, até que reste apenas o que nos interessa.

Com a imagem em evidência, conseguimos perceber alguns problemas na vetorização automática: uma parte do cabelo foi confundida com o fundo, o relógio da atleta não foi percebido e o tênis ainda possui muito ruído visual.

Selecionaremos a ferramenta Eyedroper Tool, e retiraremos a logomarca presente no tênis da atleta. Em seguida, utilizaremos a borracha para remover pontas e projeções que não fazem sentido, como a falha no cabelo da atleta. Por fim, no ponto do relógio da atleta, ampliaremos o vetor de forma que não haja nenhum ponto falho, ou seja, o braço estará totalmente preenchido.

O resultado está interessante, mas a cor do vetor ainda está muito pálida. Para editarmos a coloração do vetor, o selecionaremos e acessaremos no cabeçalho de ferramentas "Edit > Edit Colors". Então, começaremos a trabalhar com a saturação da imagem. Moveremos a barra de saturação até que as cores fiquem um pouco mais escuras e vibrantes.

---

**Atleta - Image Trace**

Entendemos como funciona a “IMAGE TRACE”, a forma automática de vetorizar. Porém, é importante conhecer esta ferramenta um pouco mais a fundo, pois nesta etapa da composição precisamos vetorizar uma figura mais complexa: a atleta.

Vamos abrir a janela Image Trace para entender melhor como podemos criar uma definição mais específica e como o Illustrator vai entender a imagem para vetorizá-la automaticamente.

Para habilitar esta janela basta ir em “WINDOW => IMAGE TRACE”. Através dela podemos definir algumas configurações que nos permitem ter um pequeno controle da qualidade da vetorização automática, como por exemplo, a quantidade de pontos, ou a quantidade de cores, e assim por diante. Para compreender melhor, veja a janela abaixo:

![img](https://caelum-online-public.s3.amazonaws.com/949-vetor-illustrator-comp/04/image_trace_2.jpg)

**A -** Ícones que trazem pré-definições de configurações. Ao clicar, o software já aplica essas pré-definições; **B -** Área para definir um preset a ser usado, como será a visualização do efeito e a quantidade de cores que o Illustrator deve considerar no momento de aplicar o “IMAGE TRACE”; **C -** Área de refinamento do efeito onde você pode definir a quantidade de “pontos/caminhos” ele deve criar - se as bordas serão drásticas ou mais suavizadas (mais ou menos bordas), nível de ruído (detalhamento) do efeito juntamente com a área para definir como será o corte do efeito. O método é semelhante ao TRIM e ao MERGE: enquanto um identifica e mescla cores iguais, o outro separa todos os elementos, tipo de preenchimento, e o que é habilitado apenas no modo black and white devido à sua complexidade mais baixa de criação e opções para ignorar o branco e alinhar os componentes do objeto; **D -** Informações sobre a complexidade do caminho criado; **E -** Habilitar a pré-visualização do efeito ou não;

Entendendo estas propriedades podemos melhorar alguns pontos da nossa vetorização automática. No nosso caso, aplicamos alguns destes efeitos em cima da imagem de uma atleta na posição de corrida, assim podemos inserir na nossa composição.

**Refinando o resultado do IMAGE TRACE** Após a aplicação do efeito, vamos utilizar o que já conhecemos e refinar algumas áreas que não ficaram legais, afinal, foi feito de forma automática.

Vamos utilizar a ferramenta “EYE DROP” para pegar as propriedades de objetos próximos e conseguir remover qualquer logo que exista na imagem, no nosso caso, o da NIKE.

Para conseguir remover alguns pontos sobressalentes vamos utilizar a ferramenta “ERASER TOOL”, a famosa borracha, para apagar parte dos elementos que ficaram estranhos no resultado. Por último, vamos refinar suas cores para melhor se encaixarem na composição.

Vamos selecionar a personagem toda e clicar em “EDIT => EDIT COLORS => SATURATE”. Esta propriedade vai pegar todas as cores selecionadas e saturar ou dessaturar um pouco, sendo importante por aplicar à todas as cores de uma só vez, sem ficar artificial. Pronto, agora falta apenas mais um elemento e podemos encaixar tudo na composição.

---

Já terminamos todas as vetorizações do nosso projeto. Agora, entraremos na **etapa de composição**, que nos permitirá conhecer uma nova ferramenta chamada _Pattern Tool_.

Primeiramente, posicionaremos os elementos dentro da área do documento, isto é, a área que contém a composição do fundo com cores intercaladas entre elas. Inseriremos a atleta, ajustando seu tamanho e a posição que ela ocupará. Em seguida, começaremos a inserir os outros elementos na cena. Ao diminuirmos o tamanho dos elementos vetorizados que criamos que possuem stroke - o contorno - perceberemos que ele não é reduzido proporcionalmente: quanto menor for o objeto, mais grossa será sua linha de stroke.

Precisamos corrigir esse problema. Para tanto, selecionaremos todos os elementos, pressionaremos o botão direito do mouse e escolheremos as opções "Transform > Scale". Teremos acesso a uma nova caixa de diálogo, nela marcaremos a opção "Scale Strokes & Effects". Agora podemos diminuir o tamanho dos elementos à vontade, pois todas as linhas serão reduzidas proporcionalmente.

Podemos já adicionar nossos elementos na cena. Posicionaremos o foguete próximo ao pé da atleta, assim como o par de tênis. O garrafa de água colocaremos próxima à cabeça e, por fim, a barra de ferro próxima à mão. Para deixar mais em evidência estes objetos, aumentaremos seu stroke no cabeçalho de ferramentas, isto é, faremos os contornos ficarem mais visíveis e expressivos.

Todos os elementos já estão em cena, mas ainda precisamos trabalhar mais no fundo. Criaremos algumas texturas e elementos visuais circulares, de forma que a nossa arte apresente uma composição mais refinada.

Utilizaremos a ferramenta Pattern, que possibilita a criação de padronagens. Padronagens são elementos gráficos que se repetem em uma composição. Iremos criar nossa própria padronagem no Illustrator partindo de uma forma circular.

Criaremos um circulo branco sem contorno. Com essa forma selecionada, clicaremos no cabeçalho de ferramentas sobre "Object > Pattern > Make". Em seguida, teremos uma nova janela de diálogo com as configurações de padronagem. Será criada uma organização padrão em que as formas circulares se organizam lado a lado, não é isso que queremos, então na opção "Tile Type", selecionaremos "Hex by Column".

A opção que selecionamos nos permite organizar manualmente a distribuição das formas em nossa padronagem. Clicaremos sobre "Pattern Tile Tool", dessa maneira teremos uma forma base poligonal que servirá de modelo para organizarmos nossa composição.

Terminada a organização, clicaremos em "Done", no cabeçalho de ferramentas. Nosso padrão estará disponível na paleta de padrões na parte direita da tela, e ele poderá ser usado como uma cor e preencher espaços e formas fechadas.

Criaremos alguns círculos preenchidos com o nosso padrão em pontos específicos da imagem: próximo ao joelho da atleta, nas costas e assim por diante, cada um com tamanhos diferentes, mas ainda harmoniosos entre si. O padrão ainda pode ser editado, basta clicarmos na aba de cores, selecionarmos a nossa padronagem e clicarmos sobre a opção "Edit Pattern".

Para que a atleta esteja posicionada na frente das padronagens que criamos, basta selecionarmos a imagem da atleta, clicarmos com o botão direito e escolhermos as opções "Arrange > Bring to Front".

---

Bolinhas - Pattern

Para finalizar a composição vamos encaixar os elementos e trazer balanço para a arte final. Nós já temos todos os objetos separados, então agora basta diminuir e rotacionar os objetos para que se encaixem na composição.

Lembre-se de habilitar a propriedade “SCALE STROKES & EFFECTS”, pois assim, ao reduzir um objeto, os efeitos e as linhas (bordas) serão reduzidos proporcionalmente. Selecione os objetos que deseja reduzir, aperte o botão direito do mouse e vá em “TRANSFORM => SCALE”. Dentro da propriedade de escala basta você habilitar o efeito de reduzir proporcionalmente todo o objeto.

![img](https://caelum-online-public.s3.amazonaws.com/949-vetor-illustrator-comp/04/scale.jpg)

Após encaixar os elementos na composição, temos um resultado mais ou menos assim:

![img](https://caelum-online-public.s3.amazonaws.com/949-vetor-illustrator-comp/04/composicao.jpg)

A nossa composição ainda possui alguns vazios que tiram sua harmonia, mas eu não quero trazer mais nenhuma figura que represente nada: já conseguimos passar o que queríamos com a arte. Então, como resolver?

Nós vamos criar uma forma abstrata baseada em um “PATTERN”, padrões que criam texturas interessantes para utilizar em composições. O próprio Illustrator traz uma ferramenta de criação de padrões muito interessante para a gente.

**O que são padrões?** O padrões são formas que se repetem de maneira ordenada com o objetivo de formar uma textura “infinita” na sua composição, como a imagem abaixo exemplifica:

![img](https://caelum-online-public.s3.amazonaws.com/949-vetor-illustrator-comp/04/patterns.jpg)

**Criando o padrão** Para conseguirmos criar o padrão criamos primeiro o elemento principal que vai compô-lo, em nosso caso, um círculo. Ao selecionar o objeto criado fomos ao menu “OBJECT => PATTERN => MAKE”, assim o Illustrator leva a gente para uma outra área de edição onde conseguimos ver como aquele objeto está sendo editado dentro daquele padrão.

![img](https://caelum-online-public.s3.amazonaws.com/949-vetor-illustrator-comp/04/pattern_window.jpg)

Basicamente o que o software mostra para gente é, um “TILE” (o quadrado com borda azul ao centro), que é a base para mostrar o que e como será repetido o elemento que está dentro deste “TILE”. Imagine que este quadrado será repetido infinitamente para todas as direções, por isso é possível ver na imagem vários outros círculos: é uma repetição do que existe dentro do quadrado.

No momento em que entramos nesta tela, também apareceu a janela para conseguirmos editar o nosso padrão, ou seja, editar este “TILE” e como o objeto vai se comportar ali dentro.

![img](https://caelum-online-public.s3.amazonaws.com/949-vetor-illustrator-comp/04/Pattern_tool.jpg)

**A -** Ferramenta que nos permite editar a forma do “TILE”. Ao invés de ser um quadrado perfeito, eu quero aumentar seu tamanho e transformá-lo em um retângulo; **B -** Área para escolher como o meu “TILE” vai se comportar, o nome do novo padrão, o tipo de “TILE”, se vai ser um quadrado ou um hexágono, tijolos, etc. e como suas dimensões e elementos vão se comportar caso fique um acima do outro; **C -** Área para tratar da pré-visualização do padrão. Estamos vendo o “TILE” ser copiado 5 vezes na horizontal e 5 vezes na vertical;

Após definir como queremos o nosso padrão podemos confirmar no pequeno menu que surgiu na parte superior da janela, clicamos em “Done” e pronto. Nosso padrão funciona como uma cor da paleta de cores, ou seja, podemos aplicar este modelo padronizado em qualquer objeto, que o seu preenchimento vai ficar repetindo eternamente o modelo padronizado que criamos.

Depois de editarmos e criarmos o padrão, aplicamos ele em alguns círculos nas áreas vazias da composição, trazendo assim mais balanço para si. Agora falta muito pouco para finalizar, vamos lá?

---

Estamos chegando ao fim da nossa composição, e agora aprenderemos sobre o painel de aparências. Inseriremos sombras e texturas em nossa composição.

Abriremos o painel "Appearance" pressionando "Shift + F6". Neste novo painel, conseguimos editar praticamente tudo que diz respeito à aparência de um elemento, como linha, preenchimento e opacidade.

Nossa primeira ação será adicionar algumas sombras aos elementos que acompanham a atleta. Selecionaremos todos esses elementos - garrafa, tênis, foguete e barra de peso - e por fim selecionaremos também a atleta. Na parte inferior do painel Appearance, teremos o botão "Add New Effect", e então selecionaremos "Stylize > Drop Shadow". Teremos acesso a um novo painel específico para este efeito, com configurações de intensidade, eixo e assim por diante. Manteremos a configuração padrão.

Dessa maneira, temos uma sombra sutil nos elementos. A próxima etapa é adicionar textura em nosso fundo. Importaremos um arquivo para nossa área de trabalho que foi disponibilizado nos materiais extras do curso.

Ampliaremos a imagem da textura e a colocaremos sobre a nossa composição. Em seguida, utilizando o painel Appearance, reduziremos a opacidade da figura para 50%. A nossa composição terá um aspecto esbranquiçado, e não é isso que desejamos. Precisaremos, portanto, mixar as cores de forma que elas se agreguem à textura.

Ainda no painel Appearance, teremos a opção "Blending Mode", e escolheremos a configuração "Multiply". Teremos as texturas mescladas com a composição. Esse resultado ficou interessante para o fundo, mas prejudica o aspecto visual da atleta. Queremos então manter a textura apenas no cenário.

Para isso, travaremos todo o resto da composição, selecionaremos a atleta, clicaremos sobre o botão direito e escolheremos "Arrange > Bring to Front". Dessa maneira a atleta está realçada e o fundo mais refinado.

---

Textura - Blending e Drop Shadow Para finalizar nossa composição vamos realçar os principais elementos e aplicar uma textura ao fundo para deixar a arte mais orgânica e harmônica. Para fazer isto, vamos utilizar a janela “APPEARANCE”, que é responsável por conter todas as informações de efeitos do objeto, sua cor de preenchimento, sua borda e outros efeitos que podemos aplicar.

Para abrir esta janela podemos ir em “WINDOW => APPEARANCE” e com ela editar o que queremos de cada objeto.

![img](https://caelum-online-public.s3.amazonaws.com/949-vetor-illustrator-comp/04/APPEARANCE.jpg)

**A -** Stroke, definições e efeitos aplicados na borda do objeto; **B -** Fill, definições e efeitos aplicados no preenchimento do objeto; **C -** Opacity, propriedades de transparência e mesclagem do objeto; **D -** Efeitos que podem ser aplicados ao objeto e a criação de novas bordas ou preenchimentos;

Já que sabemos como abrir a janela de aparências, vamos selecionar todos os objetos que queremos aplicar o efeito de sombra.

**Efeito de sombra** Após selecionar todos os objetos clicamos no ícone “Fx” da janela de aparências: ela nos mostra vários efeitos que podemos aplicar aos objetos. Em nosso caso utilizamos o efeito “STYLIZE => DROP SHADOW”, que é o responsável por criar uma sombra embaixo dos objetos selecionados.

![img](https://caelum-online-public.s3.amazonaws.com/949-vetor-illustrator-comp/04/drop_shadow.jpg)

**A -** Área para definir a mesclagem da sombra com o fundo e sua transparência; **B -** Área para definir a distância horizontal (X Offset) e distância vertical (Y Offset) da sombra; **C -** Área para definir a intensidade da sombra, se ela vai ser mais dispersa ou mais concentrada próxima ao objeto;

Depois de aplicar a sombra no nosso objeto, já estamos com uma composição com mais realce nos principais elementos. Agora para trazer mais profundidade e finalizar a composição vamos aplicar uma textura no fundo.

Aplicando a textura Para aplicar a textura, nós pegamos a imagem que se parece com papel amassado, no material disponível para baixar o conteúdo do curso, e vamos encaixar esta imagem em cima de toda a composição.

Para ela mesclar melhor com a composição, abrimos o menu “APPEARANCE” e clicamos em “OPACITY”, para visualizar as propriedades de transparência e mesclagem da imagem.

![img](https://caelum-online-public.s3.amazonaws.com/949-vetor-illustrator-comp/04/blending.jpg)

Nesta tela mudamos um pouco sua opacidade e alteramos seu modo de mesclagem de “NORMAL” para o modo que melhor se adequa à composição. Lembre-se de trazer os objetos que não precisam receber a textura para frente com o “ARRANGE => BRING TO FRONT”. Pronto, finalizamos a nossa composição. Agora basta salvar e enviar para o cliente.