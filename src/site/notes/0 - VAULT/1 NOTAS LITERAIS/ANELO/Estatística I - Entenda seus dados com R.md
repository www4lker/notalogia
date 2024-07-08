---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/estatistica-i-entenda-seus-dados-com-r/","tags":["EstatísticaAplicada","DesmistificandoEstatística","EntendendoDados","CiênciaDosDados","EstatísticaNoDiaADia","CategóricoOrdinalIntervalar","DecifrandoHistogramas","MédiaMedianaCorrelação","TesteEstatísticoAdequado","CurvaNormal","AnaliseEstatísticaComR","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# "Estatística I - Entenda seus dados com R"

## criado em: 
-  04-08-2023 - 08:26

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/R para análise de Dados\|R para análise de Dados]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Qual a diferença entre numeros ordinais, racionais, intervalais e categoricos\|Qual a diferença entre numeros ordinais, racionais, intervalais e categoricos]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/curva normal e histograma - didatico\|curva normal e histograma - didatico]]
- tags: - #EstatísticaAplicada
- #DesmistificandoEstatística
- #EntendendoDados
- #CiênciaDosDados
- #EstatísticaNoDiaADia
- #CategóricoOrdinalIntervalar
- #DecifrandoHistogramas
- #MédiaMedianaCorrelação
- #TesteEstatísticoAdequado
- #CurvaNormal
- #AnaliseEstatísticaComR 
- #ANELO 
- Fontes & Links: https://cursos.alura.com.br/course/introducao-a-estatistica-1/task/6901

---

## Transcrição

A ideia deste curso é ensinar **Estatística Aplicada**, ou seja, queremos que você aprofunde seus conhecimentos em média, mediana ou correlação, e saiba quando usar cada uma delas. Temos certeza que você já ouviu aquela frase: "existem mentiras, grandes mentiras e estatística". E isso não é tão mentira, porque se você não souber escolher o teste que irá aplicar, a função de média que usará, vai chegar em números que não explicam nada sobre o conjunto de dados que você tem.

Atualmente, a estatística é fundamental. Temos uma quantidade absurda de informações, na política, economia, esportes, ou mesmo na empresa em que trabalhamos, que vende inúmeros produtos para várias pessoas, e de onde é possível extrair informações. A estatística nos ajuda a entender um pouco mais sobre dados que envolvem a popularidade de um produto, daquilo que se vende menos, ajudando inclusive a predizer qual produto venderá mais, e quando isso vai ocorrer.

Mas, obviamente, é preciso entender estatística a fundo. Aqui, não adentraremos aquele "matematiquês" de como cada teste estatístico funciona. Claro, haverá um pouco de matemática pois não temos como fugir disso, no entanto este curso não é voltado para matemáticos, e sim para quem quer usar estatística e aplicá-la no dia a dia.

O primeiro ponto a ser entendido sobre estatística é em relação a números, e os tipos de dados que estamos usando naquele momento. Imagine um formulário indagando sobre seu sexo, cujas opções são as seguintes:

- ( ) Masculino
- ( ) Feminino
- ( ) Não quero declarar

Trata-se de um tipo de dado que chamamos de **Categórico**, pois cada um é diferente do outro e não possuem relação ou hierarquia.

Outro tipo de dado comum é conhecido por dado **Ordinal**. Por exemplo, você acabou de fazer um curso e pedem para que o professor seja avaliado em uma escala de 1 a 10:

```makefile
Nota: ( )1 ( )2 ( )3 ( )4 ( )5 ( )6 ( )7 ( )8 ( )9 ( )10
```

Neste tipo, existe uma ordem: 1 < 2 < 3 <...< 10. Mas não conseguimos fazer comparações do 1 para o 2. Existe a sensação de que de 1 para 2 é a mesma coisa que de 2 para 3, porém não conseguimos medir isto de maneira precisa. Esses intervalos podem variar de pessoa para pessoa. É diferente de medir, por exemplo, uma temperatura: em um ser humano com 36ºC, saberemos que é um valor preciso. De 36 para 37 a diferença é de exatamente um grau Celsius.

A temperatura, então, é um exemplo de dado **Intervalar**, e a diferença entre cada valor é precisa e mensurável:

```lua
25ºC -- 25,2ºC -- 26ºC
```

Outro tipo de dado, menos comum, é o **Racional**, bem parecido com o Intervalar, sendo composto de números em ordem, e cuja diferença de um para outro é mensurável. Porém, nesse tipo de dado, o 0 (zero) significa a ausência daquilo. Em se tratando da temperatura em Celsius, 0ºC significa que está frio, mas não a ausência de temperatura. Em graus Kelvin, 0K indica a ausência de temperatura. Nos estudos em Física, faz sentido lidar com os dados Racionais, porém em Estatística trabalharemos com os três primeiros tipos de dados: Categórico, Ordinal e Intervalar.

Dependendo do tipo de dado, é necessário escolher o método estatístico mais adequado. Posteriormente veremos se a média aritmética que aprendemos na escola faz sentido para qualquer tipo de dado. **Conhecer o tipo de dado a ser trabalhado é fundamental**.

Tendo isso em mente, vamos continuar. Em Estatística, raramente analisaremos apenas um número; nós a utilizamos porque temos vários dados e precisamos reduzi-los a um número que os traduza, para que possamos entendê-los de maneira fácil.

Vamos começar a agrupar dados!

### Exemplo

Temos os nomes dos alunos de uma escola e a quantidade de aulas que cada um assistiu:

- Maurício: 2 aulas
    
- Natália: 4 aulas
    
- Felipe: 4 aulas
    
- João: 6 aulas
    
- José: 5 aulas
    

Agora queremos entender essas informações: quantas aulas os alunos assistem na escola? Para tal, utilizaremos um **histograma**, um gráfico que mostra a quantidade de frequências e quantas vezes elas se repetem.

|Quantidade de aulas assistidas|Quantidade de alunos|
|---|---|
|2|1|
|4|2|
|5|1|
|6|1|

Perceba que temos a mesma informação disposta de outra maneira. Com essa tabela, conseguimos criar um gráfico que mostra a frequência dos acontecimentos na distribuição. Nesse exemplo utilizamos poucos dados, mas imaginemos uma distribuição maior.

Se traçarmos uma linha passando pelos topos desse gráfico, teremos uma curva muito importante chamada de **Curva Normal**. É essa curva que esperamos em uma distribuição comum. Se, por exemplo, desenharmos o histograma da altura de um homem brasileiro, teremos que poucos estarão nas faixas menores e maiores, e muitos nas faixas centrais.

Isto é, muita gente estará na média, e pouca nos dois extremos. Entender se a distribuição está dentro ou fora dessa curva também é de extrema importância para escolhermos o teste estatístico ideal. Falaremos sobre isso mais adiante.

### Resumindo

- antes de estudarmos a média, o Teste de Correlação ou Teste de Hipótese, devemos entender os tipos de dados: **Categóricos**, **Ordinais** e **Intervalares**;
- depois pensamos no formato da distribuição. Uma maneira fácil é desenhando um **histograma** que nos mostra a frequência da distribuição. Os testes a serem aplicados mudam se ela for Normal ou não.

Com essas informações, estamos prontos para começar a entender mais sobre estatística. Até a próxima aula!
