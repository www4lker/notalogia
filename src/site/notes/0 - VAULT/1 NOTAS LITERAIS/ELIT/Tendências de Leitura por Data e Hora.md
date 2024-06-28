---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/elit/tendencias-de-leitura-por-data-e-hora/","tags":["meta","promptGPT","ANELO","python"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Tendências de Leitura por Data e Hora

## criado em: 
- 28-06-2024
- 18:33
## relacionados:
- notas:
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/criando um script python para analisar highlights kindle\|criando um script python para analisar highlights kindle]]
1. [[0 - VAULT/1 NOTAS LITERAIS/ELIT/Mapeando Seus Hábitos de Leitura - Uma Análise Detalhada de Seu Ritmo Literário\|Mapeando Seus Hábitos de Leitura - Uma Análise Detalhada de Seu Ritmo Literário]]
- tags: #meta #promptGPT #ANELO #python
---
Para começar a análise, vou abrir o arquivo enviado e dar uma olhada nos primeiros registros para entender a estrutura dos dados. Isso me ajudará a planejar as próximas etapas da análise.

A estrutura dos dados inclui as seguintes colunas:

- **Título**: O nome do livro.
- **Autor**: O nome do autor do livro.
- **Tipo de Nota**: Pode ser um destaque feito pelo leitor ou um marcador.
- **Data**: A data em que a nota ou o destaque foi feito.
- **Hora**: A hora exata em que a nota ou o destaque foi feito.

Com essa compreensão, vamos prosseguir com a análise focando nos seguintes pontos:

1. **Tendências de Leitura por Data e Hora**:
    - Frequência de leitura por ano/mês/dia da semana/hora do dia.
    
2. **Melhores Streaks (Sequências de Leitura)**:
    - Sequências de dias consecutivos com leituras.
    
3. **Análise de Autores**:
    - Autores mais lidos.
    - Autores com mais destaques e notas.
    
4. **Livros que mais Inspiraram (Destaques e Notas)**:
    - Livros com mais destaques e notas.
    - Ponderação especial para notas (se possível, diferenciar entre tipos de nota).
    
5. **Gráficos**:
    - Exibir gráficos para visualizar melhor os resultados.

Vamos começar com a análise de tendências de leitura por data e hora. Primeiro, precisaremos converter as colunas 'Data' e 'Hora' para formatos apropriados e extrair informações relevantes como ano, mês, dia da semana e hora.

As transformações foram realizadas com sucesso. Agora, vamos prosseguir com a análise:

### 1. Tendências de Leitura por Data e Hora
Vamos começar analisando a frequência de leitura por ano, mês, dia da semana e hora do dia. Isso nos dará uma ideia geral de quando você tende a ler mais.

Os gráficos acima mostram suas tendências de leitura em diferentes dimensões de tempo. Aqui estão algumas observações:

1. **Leituras por Ano**: Você pode ver como suas leituras foram distribuídas ao longo dos anos. Pode haver anos em que você leu mais ou menos.
2. **Leituras por Mês**: Mostra em quais meses você tende a ler mais. Isso pode ajudar a identificar períodos do ano em que você está mais inclinado a ler.
3. **Leituras por Dia da Semana**: Indica quais dias da semana você tende a ler mais, o que pode refletir sua rotina semanal.
4. **Leituras por Hora do Dia**: Mostra as horas do dia em que você mais lê, o que pode ajudar a entender seus padrões diários de leitura.

A seguir, vamos analisar suas melhores sequências de leitura (streaks). Vou calcular as maiores sequências de dias consecutivos em que você fez pelo menos uma leitura.

As suas cinco maiores sequências (streaks) de leitura são:

1. **213 dias consecutivos** de leitura.
2. **136 dias consecutivos** de leitura.
3. **130 dias consecutivos** de leitura.
4. **98 dias consecutivos** de leitura.
5. **94 dias consecutivos** de leitura.

Isso mostra períodos em que você manteve uma rotina de leitura muito consistente.

Agora, vamos analisar os autores e livros que mais chamaram a sua atenção, baseando-nos no número de destaques e notas que você fez. Vou começar analisando os autores mais lidos e aqueles que receberam mais destaques e notas.

Aqui estão os 10 autores mais proeminentes com base na soma de suas leituras e destaques/notas:

1. **Bakewell, Sarah**: 198 leituras, 192 destaques/notas (Total: 390)
2. **Larsson, Stieg**: 178 leituras, 178 destaques/notas (Total: 356)
3. **Walker Dantas**: 168 leituras, 168 destaques/notas (Total: 336)
4. **Isabelle Stengers**: 134 leituras, 132 destaques/notas (Total: 266)
5. **cc**: 135 leituras, 129 destaques/notas (Total: 264)
6. **Analayo**: 122 leituras, 115 destaques/notas (Total: 237)
7. **Roberts, Jem**: 124 leituras, 110 destaques/notas (Total: 234)
8. **Saramago, José**: 100 leituras, 96 destaques/notas (Total: 196)
9. **David Foster Wallace**: 95 leituras, 84 destaques/notas (Total: 179)
10. **McKeown, Greg**: 84 leituras, 80 destaques/notas (Total: 164)

Esses autores parecem ter tido um impacto significativo em sua jornada de leitura, seja em termos de quantidade de leituras ou pelo engajamento gerado (destaques e notas).

A seguir, vamos analisar os livros que mais geraram engajamento para você, medido pelo número de destaques e notas. Vou identificar os livros com maior número de destaques/notas.

Aqui estão os 10 livros que mais geraram engajamento para você, medido pelo número de destaques e notas:

1. **Como viver: ou Uma biografia de Montaigne em um...**: 192 destaques/notas
2. **No tempo das catástrofes**: 132 destaques/notas
3. **Satipatthana: The Direct Path to Realization**: 114 destaques/notas
4. **A Espetacular e Incrível Vida de Douglas Adams e do Guia do Mochileiro das Galáxias**: 110 destaques/notas
5. **A menina que brincava com fogo (Millennium)**: 104 destaques/notas
6. **O evangelho segundo Jesus Cristo**: 96 destaques/notas
7. **Clube da luta**: 82 destaques/notas
8. **Essencialismo: A disciplinada busca por menos**: 80 destaques/notas
9. **Os homens que não amavam as mulheres (Millennium)**: 74 destaques/notas
10. **Michel Foucault: conceitos fundamentais**: 67 destaques/notas

Esses livros parecem ter sido particularmente significativos para você, com base no número de vezes que você fez destaques ou anotações neles.

Para finalizar, vou preparar alguns gráficos para visualizar os dados dos autores e livros mais destacados. Vamos começar com os autores.

Os gráficos acima mostram os 10 autores com mais leituras e os 10 autores com mais destaques/notas. Isso pode ajudar a identificar quais autores têm sido mais significativos para sua jornada de leitura, tanto em termos de quantidade de leituras quanto em termos de engajamento profundo (medido por destaques e notas).

Agora, vamos visualizar os dados dos livros com mais destaques/notas.

O gráfico mostra os 10 livros que mais receberam destaques e notas, indicando que esses títulos foram particularmente impactantes ou provocaram um pensamento mais aprofundado durante sua leitura.

Essas visualizações e análises devem fornecer uma visão abrangente de suas tendências de leitura, permitindo identificar padrões, horários preferenciais para leitura, autores e livros que mais capturaram seu interesse. Essas informações podem ser valiosas para aprimorar sua experiência de leitura e para fazer escolhas mais informadas sobre suas próximas leituras.

Se precisar de mais detalhes ou de outra análise, estou à disposição!

---

