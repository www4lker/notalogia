---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/r-para-analise-de-dados/","tags":["AnáliseDeDadosComR","IntroduçãoAoR","RStudioParaIniciantes","AprendendoR","AnaliseEstatísticaComR","ExplorandoDadosComR","ConstruindoGráficosComR","ModelosPreditivosComR","ImportandoDadosComR","CorrelaçãoEmR","EstatísticaAplicada","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# R para análise de Dados

## criado em: 
-  04-08-2023 - 08:23

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Primeiros passos com R\|Primeiros passos com R]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/R para análise de Dados\|R para análise de Dados]]
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
#ANELO 
---

## Transcrição

Olá! Sejam bem-vindos ao curso de **Introdução a Análise de Dados com R**. Sou Rodolpho Bernabel, e minha intenção é que a partir deste curso vocês estejam aptos a fazerem suas primeiras análises estatísticas, quantitativas e preditivas de dados.

Utilizaremos o [**_RStudio_**](https://www.rstudio.com), uma plataforma que funciona como ferramenta de auxílio gráfico para aprender a Linguagem R. O download do programa será explicado durante o curso.

A imagem abaixo mostra como é sua interface:

![Interface RStudio](https://s3.amazonaws.com/caelum-online-public/719+-business-analysis-com-R/Transcri%C3%A7%C3%A3o/719.1.01.01_Interface+RStudio.png)

Ela é composta por 4 partes e cada uma possui uma função:

- na parte superior à esquerda, fica o _script_, onde digitamos os comandos;
- na parte inferior à esquerda está o console, onde os comandos do _script_ são executados e visualizamos seus resultados, bem como as estatísticas;
- na parte superior à direita estão os bancos de dados com que estamos trabalhando e alguns botões que auxiliam na importação deles;
- na parte inferior à direita, visualizamos os gráficos que estamos construindo. Nela aprenderemos a:
    - elaborar histogramas;
    - mudar elementos estéticos, como cor e títulos;
    - desenvolver gráficos que na visualização estejam da forma planejada, e gráficos de dispersão;
    - como ajustar modelos preditivos lineares e não lineares;
    - analisar gráficos avançados;
    - exportar gráficos em figuras, em `.jpg` e `.pdf`, que possam ser anexados em editores de texto e outros softwares, para ilustrar apresentações.

Estudaremos conceitos estatísticos e como são feitos e especificados em termos de comandos, que virão com a explicação do nome e da função. Explicaremos o que está sendo pedido, por quê é importante e quais problemas queremos resolver.

Para isso, o curso será baseado em um projeto hipotético, no qual uma empresa de vídeos online pede uma análise dos cursos e vídeos da plataforma, a partir de uma amostra do banco de dados. Veremos a média de tempo que os alunos levam para concluir as aulas, quais são os cursos e quais vídeos de cada um deles são os mais acessados.

Faremos análise de correlação, verificando se a popularidade do curso está relacionada à sua média de duração. Importaremos bancos de dados e juntaremos informações externas, que precisamos ter em um mesmo local para fazer a análise.

Para concluir, sugiro para quem nunca estudou estatística ou estudou e está um pouco "enferrujado" que faça o curso [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Estatística I - Entenda seus dados com R\|Estatística I - Entenda seus dados com R]] da Alura, antes de começar o de "Introdução a Análise de Dados com R".

No curso sugerido, a Linguagem R é utilizada de maneira auxiliar no aprendizado de conceitos estatísticos. Assim, os alunos aprendem estatística, juntamente com alguns comandos de R.

Espero que gostem! Vamos lá!