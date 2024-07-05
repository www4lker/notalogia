---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/readme-pd-e/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# readme  PdE

## criado em: 
-  02-06-2023 - 15:35

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/joguinho monty hall em python\|joguinho monty hall em python]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Portas da Esperança\|Portas da Esperança]]
- tags: #ANELO 
- Fontes & Links: 

---

## O jogo

O problema de Monty Hall é um quebra-cabeça de probabilidade do game show "Let's Make a Deal". No quebra-cabeça, um participante escolhe uma das três portas para ganhar um prêmio. Depois que o participante escolhe, o apresentador, Monty Hall, abre uma das portas restantes para revelar que ela não contém o prêmio. O participante tem então a opção de *manter sua escolha original ou mudar para a outra porta fechada*. Surpreendentemente, a troca de portas aumenta as chances de vitória do participante.

Para entender melhor o problema, sugere-se modelá-lo usando a programação Python. Assim, aplicam-se dois cenários: um em que o participante não troca de porta e outro em que ele troca. Usando geradores de números aleatórios, demonstra-se a probabilidade de vitória em cada cenário.Finalmente, fica claro que quando o participante mantém sua escolha original, suas chances de ganhar permanecem em um terço. Entretanto, se ele trocar de porta, suas chances aumentam para dois terços.

Enfatiza-se que a execução de um grande número de testes, como 1.000, revela o verdadeiro impacto da troca de portas. Os resultados mostram que, com a troca de portas, os participantes ganham cerca de dois terços das vezes, o que é consistente com a solução teórica. Reconhece-se que esse resultado contraintuitivo pode ser difícil de entender, mas pode ser explicado pelo fato de que a revelação de Monty oferece uma oportunidade extra de troca, aumentando as chances.

Conclui-se que, para explicar, jogar o jogo apenas uma vez não permite que o participante observe a vantagem de trocar de porta. Entretanto, com mais tentativas, a *lei dos grandes números* entra em ação, garantindo que os resultados se aproximem do valor esperado. Esse conceito se aplica a outras situações baseadas no acaso, como os jogos de cassino, em que a vantagem da casa se torna aparente com um grande número de jogos.