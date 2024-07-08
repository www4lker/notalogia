---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/shapiro-teste-e-summary-em-r/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# shapiro teste e summary em R

## criado em: 
- 04-06-2024
- 19:36
## relacionados:
- notas:
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Estatística I - Entenda seus dados com R\|Estatística I - Entenda seus dados com R]] 
- tags: #ANELO 
- Fontes & Links: 
---

1. **shapiro.test():** Esta é uma função que realiza o Teste de Shapiro-Wilk, que é usado para testar a normalidade de um conjunto de dados. Isso é importante, pois muitos testes estatísticos assumem que os dados são normalmente distribuídos.

   A função `shapiro.test()` recebe como argumento um vetor de dados e retorna um resultado de teste que inclui o valor W de Shapiro-Wilk e o valor p do teste.

   A hipótese nula do teste é que os dados são provenientes de uma distribuição normal. Portanto, se o valor p for menor que o nível de significância (geralmente 0,05), rejeitamos a hipótese nula e concluímos que os dados não são normalmente distribuídos.

   Aqui está um exemplo de como usar a função:

   ```R
   # Criar um conjunto de dados
   dados <- rnorm(100)  # 100 números aleatórios de uma distribuição normal

   # Realizar o teste de Shapiro-Wilk
   resultado <- shapiro.test(dados)

   # Imprimir o resultado
   print(resultado)
   ```

2. **summary():** A função `summary()` no R fornece um resumo estatístico de um objeto. Para um vetor numérico, ela irá retornar um resumo de seis números: mínimo, primeiro quartil (Q1), mediana (segundo quartil, Q2), média, terceiro quartil (Q3) e máximo.

   Para um modelo estatístico, ela irá retornar um resumo mais detalhado incluindo os coeficientes do modelo, os valores p, etc.

   Aqui está um exemplo de como usar a função com um vetor numérico:

   ```R
   # Criar um conjunto de dados
   dados <- c(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)

   # Obter um resumo dos dados
   resumo <- summary(dados)

   # Imprimir o resumo
   print(resumo)
   ```

Espero que isso tenha sido útil e claro! Estou aqui para responder a quaisquer outras perguntas que você possa ter.