---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/restinho-em-aritmetica-e-programacao/","tags":["meth","python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Restinho em aritmética & programação
## isto: %

## criado em: 
-  03-05-2023 - 12:34

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023 2 S 2 - Operadores - ferramentas de manipulação de dados\|LATAM 2023 2 S 2 - Operadores - ferramentas de manipulação de dados]]
- tags: #meth #python #ANELO 
- Fontes & Links: 

---
>
## Porque teríamos um símbolo somente para o resto da divisão, qual sua aplicabilidade e se é uma pratica comum em linguagens de programação de alto nível usar esse tipo de operação

>além das tradicionais operacoes aritmeticas o Python usa este símbolo (%) para calcular resto de divisão. Agora explique para uma pessoa que não lembra de quase nada das aulas de algebra por que teriamos um simbolo somente para o resto da divisao, qual sua aplicabilidade e se é uma pratica comum em linguagens de programação de alto nivel usar esse tipo de operação

A operação de módulo ou resto da divisão é uma operação matemática comum que consiste em calcular o resto de uma divisão inteira entre dois números. Em outras palavras, dado um dividendo `a` e um divisor `b`, o operador `%` retorna o resto da divisão inteira de `a` por `b`.

Por exemplo, se a divisão de 7 por 3 for realizada, o resultado seria 2 com um resto de 1. Isso significa que 7 pode ser dividido por 3 duas vezes, com um resto de 1. O operador `%` é usado para obter esse resto.

Em programação, o operador `%` é útil em várias situações, como verificar se um número é par ou ímpar (um número é par se seu resto da divisão por 2 é zero), gerar números aleatórios dentro de um intervalo específico ou realizar cálculos em ciclos repetitivos (loops) para executar uma ação a cada x iterações.

Em relação à sua pergunta sobre a prática comum em linguagens de programação de alto nível, sim, muitas linguagens de programação modernas, como C++, Java, JavaScript, Ruby e Python, suportam o operador de módulo. É uma operação matemática simples, mas bastante útil em muitas aplicações de programação.

### exemplos

Aqui estão alguns exemplos práticos de como o operador `%` é usado no mundo da programação:

1. Verificar se um número é par ou ímpar:
```python
num = 7
if num % 2 == 0:
    print(num, "é par")
else:
    print(num, "é ímpar")
```
Resultado: `7 é ímpar`

2. Gerar números aleatórios dentro de um intervalo específico:
```python
import random

# gerar um número aleatório entre 0 e 99 (múltiplos de 5)
num = random.randint(0, 19) * 5
print(num)

# Neste exemplo, a função `randint` gera um número inteiro aleatório entre 0 e 19, que é então multiplicado por 5 para obter um múltiplo de 5 entre 0 e 99. O operador `%` não é utilizado diretamente neste exemplo, mas a ideia é similar: obter um valor baseado no resto da divisão por um número específico (no caso, 5).
```

3. Realizar cálculos em ciclos repetitivos (loops) para executar uma ação a cada x iterações:
```python
for i in range(1, 11):
    if i % 2 == 0:
        print(i, "é um número par")

```

Resultado:
```
2 é um número par
4 é um número par
6 é um número par
8 é um número par
10 é um número par

```
Esses são apenas alguns exemplos de como o operador `%` pode ser usado em programação. Ele é uma ferramenta bastante útil e versátil, e pode ser aplicado em muitas outras situações.