---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/media-mediana-e-moda/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Média, mediana e moda

## criado em: 
- 04-06-2024
- 18:52
## relacionados:
- notas:
1. [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Primeiros passos com R\|Primeiros passos com R]]
2. [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Estatística I - Entenda seus dados com R\|Estatística I - Entenda seus dados com R]]
- tags: #ANELO 
- Fontes & Links: 
---

>explique de forma simples os conceitos de Média, mediana e moda - adapte para alguem aprendendo a programar e usar o R no terminal

**Média:**

A média é a soma de todos os números dividida pelo número total de elementos. Em termos simples, se você tiver um conjunto de números, adicione todos eles e divida pelo número de elementos que você somou.

Por exemplo, para o conjunto de números 1, 2, 3, a média seria (1+2+3)/3 = 2.

No R, você pode calcular a média utilizando a função `mean()`. Assim, para o nosso exemplo, ficaria:

```r
numeros <- c(1, 2, 3)
media <- mean(numeros)
print(media)
```

**Mediana:**

A mediana é o número que está no meio de um conjunto de números quando esses números estão em ordem. Se houver um número ímpar de elementos, a mediana será o número no meio. Se houver um número par de elementos, a mediana será a média dos dois números do meio.

Por exemplo, para o conjunto de números 1, 2, 3, a mediana seria 2, pois 2 está no meio. Para o conjunto de números 1, 2, 3, 4, a mediana seria (2+3)/2 = 2.5, que é a média dos dois números do meio.

No R, você pode calcular a mediana utilizando a função `median()`. Assim, para o nosso exemplo, ficaria:

```r
numeros <- c(1, 2, 3, 4)
mediana <- median(numeros)
print(mediana)
```

**Moda:**

A moda é o número que ocorre mais frequentemente em um conjunto de números. Pode haver mais de uma moda se mais de um número ocorrer o máximo de vezes.

Por exemplo, para o conjunto de números 1, 2, 2, 3, a moda seria 2, pois 2 ocorre mais vezes.

No R, calcular a moda é um pouco mais complexo porque o R não tem uma função built-in para calcular a moda. Mas você pode criar sua própria função para calcular a moda:

```r
moda <- function(v) {
   uniqv <- unique(v)
   uniqv[which.max(tabulate(match(v, uniqv)))]
}

numeros <- c(1, 2, 2, 3)
m <- moda(numeros)
print(m)
```

Nesse código, a função `moda` calcula a moda do vetor `v`. A função `unique(v)` retorna um vetor de elementos únicos em `v`. A função `match(v, uniqv)` retorna um vetor dos mesmos comprimento que `v` com os elementos correspondentes de `uniqv`. A função `tabulate()` conta o número de vezes que cada elemento de `uniqv` ocorre em `v`. A função `which.max()` retorna o índice do máximo valor de ocorrências, que é usado para indexar `uniqv` para obter a moda.

>[!tips]

A escolha da medida de tendência central - média, mediana ou moda - depende do tipo de dados que estamos lidando e da distribuição dos dados. Aqui estão algumas dicas mais detalhadas:

1. **Dados Ordinais:** Para dados ordinais, onde os dados podem ser classificados, mas as diferenças entre os dados não são uniformes (por exemplo, classificação de filmes), as medidas mais adequadas de tendência central são a mediana e a moda. A mediana é o valor do meio quando os dados estão ordenados, e a moda é o valor que ocorre com mais frequência.

   Por exemplo, se tivermos uma lista de avaliações de filmes (1 a 5 estrelas), uma mediana pode dar a avaliação mediana (meio do pacote) e a moda pode indicar a avaliação mais comum dada.

2. **Dados Intervalares:** Para dados intervalares, onde as diferenças entre os dados são uniformes (como a temperatura em graus Celsius), a média aritmética é comumente usada. A média aritmética é calculada somando todos os valores e dividindo pelo número de valores.

   Contudo, a média é sensível a *outliers* (valores que são muito maiores ou menores que os demais), então se seu conjunto de dados tem outliers, você pode preferir usar a mediana, pois ela não é afetada por esses valores extremos.

3. **Histograma e Distribuição Normal:** Um histograma é um gráfico que mostra a frequência dos dados. Ele pode ser útil para visualizar a distribuição dos seus dados. Se os seus dados têm uma distribuição normal (em forma de sino), a média, a mediana e a moda serão todas iguais.

   Se o seu histograma parece uma distribuição normal, então a média é uma boa medida de tendência central. No entanto, se os seus dados estão enviesados para a esquerda ou para a direita, pode ser melhor usar a mediana. 

Em resumo, a melhor medida de tendência central depende do tipo de dados que você tem e de como eles estão distribuídos. É sempre uma boa ideia visualizar seus dados primeiro para ter uma ideia da distribuição antes de decidir qual medida usar.