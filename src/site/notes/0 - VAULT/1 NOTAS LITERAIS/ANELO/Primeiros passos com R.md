---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/primeiros-passos-com-r/","tags":["ANELO","AnáliseDeDadosComR","IntroduçãoAoR","RStudioParaIniciantes","AprendendoR","AnaliseEstatísticaComR","ExplorandoDadosComR","ConstruindoGráficosComR","ModelosPreditivosComR","ImportandoDadosComR","CorrelaçãoEmR","EstatísticaAplicada"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Primeiros passos com R

## criado em: 
-  04-08-2023 - 09:08

### Conteúdo Relacionado

- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Primeiros passos com R# Primeiros passos com R\|# Primeiros passos com R]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/R para análise de Dados\|R para análise de Dados]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Média, mediana e moda\|Média, mediana e moda]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/shapiro teste e summary em R\|shapiro teste e summary em R]]
- #ANELO 
- tags: - #AnáliseDeDadosComR
- #IntroduçãoAoR
- #RStudioParaIniciantes
- #AprendendoR
- #AnaliseEstatísticaComR
- #ExplorandoDadosComR
- #ConstruindoGráficosComR
- #ModelosPreditivosComR
- #ImportandoDadosComR
- #CorrelaçãoEmR
- #EstatísticaAplicada 
- Fontes & Links: https://cursos.alura.com.br/course/business-analytics-com-r/task/32790

---

Começamos nosso curso de Estatística com os tipos de dados, agora passaremos à prática. Esta aula servirá basicamente para introduzir a ferramenta **R**, uma linguagem de programação muito utilizada por estatísticos, com inúmeros comandos prontos.

> Muitas pessoas gostam de utilizar o Microsoft Excel, que é uma boa ferramenta, mas não tanto para trabalhos mais avançados.


Nas nossas aulas utilizaremos a linha de comando diretamente, por ela ser independente do sistema operacional. Caso prefira, é possível baixar a versão com a interface gráfica.

Ao digitarmos `R` logo na primeira linha, o programa retorna diversas informações relacionadas à linguagem, como a versão instalada e algumas dicas. O R interpreta tudo que escrevermos: se digitarmos “1”, retornará “1”, se digitarmos “1+1”, retornará “2”. Ou seja, qualquer expressão matemática retornará seu resultado:

```csharp
1

[1] 1

1+1

[1] 2

3*8+2/5

[1] 24.4

(3*7)/4

[1] 5.25
```

Também podemos utilizar parênteses para definir a precedência de operações, e outros operadores a que já estamos acostumados.

### Variáveis

Podemos querer guardar resultados de operações para utilizarmos depois. Para tal, utilizamos o símbolo `<-`, que tem formato de seta, após o nome que queremos dar à essa variável (por exemplo “numero”):

```r
numero <- (3*7)/4
```

Depois disso, toda vez que digitarmos `numero` e pressionarmos "Enter", o programa retornará o resultado da conta atribuída a essa variável:

```csharp
numero
[1] 5.25
```

Podemos fazer contas com ela:

```csharp
numero * 2
[1] 10.5
```

### Listas

Outro comando muito importante para se guardar informações é o método `c( )`, que guardará uma lista de números. Funciona da mesma forma como guardamos uma variável:

```r
lista <- c(1, 2, 3, 4, 5, 6)
```

Se digitarmos `lista`, teremos:

```csharp
lista
[1] 1 2 3 4 5 6
```

Assim, podemos fazer operações com uma lista:

```csharp
lista * 2
[1] 2 4 6 8 10 12
```

### Conjunto de dados e histograma

Agora vamos utilizar o método de criar listas para montar histogramas, usando o exemplo da aula passada, em que tínhamos os dados de quantas aulas cada aluno assistiu na escola:

```r
aulas <- c(2, 4, 4, 6, 6, 6, 6, 8, 8, 10)
```

Com esta lista de dados guardada podemos plotar um histograma de forma muito simples:

```scss
hist(aulas)
```

Será aberta uma janela com o histograma desenhado:

![gráfico cujo eixo X representa a quantidade de aulas, e o Y a frequência delas](https://s3.amazonaws.com/caelum-online-public/introducao-a-estatistica/est_2_1.png)

Temos a opção de customizar esse histograma por meio de comandos que encontramos digitando `?hist`. Para voltar às linhas de comando basta digitarmos `q`.

Como você deve ter percebido, o R possui seu próprio manual. Dê uma lida nele para ir se acostumando com os comandos, uma vez que todas essas funções dão suporte a muitos usos. Outra opção é procurar esse manual, ou partes dele, na internet. Tente digitar “hist R” no Google.

---

Muito provavelmente você já deve ter estudado esse assunto na escola, e se pedirmos para você calcular a média, por exemplo, de 1, 2, 3 e 4, fará:

```undefined
(1 + 2 + 3 + 4)/4 = 10/4 = 2,5
```

Portanto, de modo geral, teremos:

```bash
(x1 + x2 + x3 + ... + xn)/n
```

Será mesmo que, para todo conjunto de números, devemos utilizar a **Média Aritmética** para encontrarmos uma **Tendência Central**? Talvez. Devemos saber que tipo de dado possuímos, lembra-se da primeira aula de Estatística? A média serve para dados Ordinais ou Intervalares? Vejamos um exemplo:

Imagine que você é um professor, e que no final da aula você entrega um formulário para os alunos preencherem com a nota que eles te dariam, em um intervalo de 1 a 10:

```vbnet
Nota: ( )1 ( )2 ( )3 ( )4 ( )5 ( )6 ( )7 ( )8 ( )9 ( )10  [dado do tipo Ordinal]
```

Segue que:

- 1º aluno: 10
- 2º aluno: 1
- 3º aluno: 1
- 4º aluno: 1

Fazendo a média:

```undefined
(10 + 1 + 1 + 1)/4 = 3,25
```

Não é estranho? O 10 dado pelo primeiro aluno não parece exceção? Você é, claramente, um professor nota 1! Perceba que escolher a Média Aritmética sem levar em conta o tipo de dado pode te levar a uma informação estranha.

Veja outro exemplo que pode nos enganar:

Em uma empresa, os salários dos funcionários são como se segue:

- 1º funcionário: 2000 reais
- 2º funcionário: 2000 reais
- 3º funcionário: 2000 reais
- 4º funcionário: 100.000 reais

Calculando a média:

```yaml
100.000 + 2000 + 2000 + 2000/4 = 26500
```

Você diria que a média dos salários da empresa é de 26500 reais? Não, porque 100.000 reais é uma exceção, e confunde a média real. Chegamos à conclusão de que precisamos pensar em outras soluções para o cálculo da Tendência Central de um conjunto de dados. A Média Aritmética é totalmente sensível aos valores que chamamos de **_outliers_**, ou **pontos fora da curva**.

A seguir, veremos outras maneiras de calcular a tendência central de um conjunto de dados.

## Mediana

Para o cálculo da mediana, colocamos os valores dados em ordem crescente e escolhemos aquele que é central. Isso é fácil para quantidades ímpares de dados, pois haverá um número localizado bem no meio da amostra. Veja um exemplo:

```undefined
1 1 6 1 5 10 1 1 1
```

Em ordem crescente:

```undefined
1 1 1 1 1 1 5 6 10
```

O valor central é o 1, que é a nossa mediana. Para quantidades pares de dados, pegamos os dois valores centrais e calculamos sua Média Aritmética:

```undefined
1 1 5 1 2 10 1 6 
```

Em ordem crescente:

```undefined
1 1 1 1 2 5 6 10
```

Os valores centrais são, respectivamente, 1 e 2. A média entre eles é 1,5, e esta é a mediana que queríamos encontrar. Perceba que ela é menos suscetível aos _outliers_. Obviamente, não significa que a Média Aritmética não é uma boa medida de Tendência Central. Se sua distribuição é estável, a Média pode ser boa.

Então, como saber qual das duas usar? Inicialmente, verifique se os _outliers_ são muito grandes e distantes do resto da amostra. Outra regra é que, se o tipo de dado for Ordinal, a média não é um bom método.

## Moda

A moda é o elemento que mais se repete na distribuição:

```undefined
1 1 2 2 2 2 2 3 3 5 5 5
```

Nessa amostra, o número 2 é o que mais se repete, logo ele é a nossa moda. Esta pode ser uma maneira honesta de se calcular a medida de Tendência Central.

Você irá perceber que, em uma amostra **bem distribuída**, a média, mediana e moda são **iguais** ou possuem **valores muito próximos**.

### Dicas:

- com dados Ordinais usamos mediana ou moda;
- utilizamos a Média Aritmética em dados Intervalares, salvo aqueles que possuam _outliers_;
- desenhe um histograma e verifique se consegue desenhar uma linha parecida com a Normal. Se você tiver uma **distribuição normal**, o cálculo da média é um método razoável.