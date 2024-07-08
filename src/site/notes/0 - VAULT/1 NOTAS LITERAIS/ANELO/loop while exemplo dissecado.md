---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/loop-while-exemplo-dissecado/","tags":["python","chatgpt","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# loop while exemplo dissecado

## criado em: 
-  05-05-2023 - 14:43

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023 - 3.1 Section 1 – Making decisions in Python\|LATAM 2023 - 3.1 Section 1 – Making decisions in Python]]
- tags: #python #chatgpt #ANELO 
- Fontes & Links: 

---
```python
# Um programa que lê uma sequência de números  
# e conta quantos números são pares e quantos são ímpares.  
# O programa termina quando zero é digitado.  
  
odd_numbers = 0  
even_numbers = 0  
  
# Leia o primeiro número.  
number = int(input("Digite um número ou digite 0 para parar: "))  
  
# 0 termina a execução.  
while number != 0:  
# Verifique se o número é ímpar.  
if number % 2 == 1:  
# Aumente o contador odd_numbers.  
odd_numbers += 1  
else:  
# Aumente o contador even_numbers.  
even_numbers += 1  
# Leia o número seguinte.  
number = int(input("Digite um número ou digite 0 para parar: "))  
  
# Imprimir resultados.  
print("Números ímpares contam:", odd_numbers)  
print("Números pares contam:", even_numbers)
```


Claro, com prazer! Este é um programa simples que lê uma sequência de números digitados pelo usuário e conta quantos números são pares e quantos são ímpares. O programa para de ler números quando o usuário digita zero.

Vamos dissecar o código linha por linha:

python

`odd_numbers = 0 even_numbers = 0`

Essas duas linhas inicializam duas variáveis de contagem: `odd_numbers` (números ímpares) e `even_numbers` (números pares) com zero cada.

python

`number = int(input("Digite um número ou digite 0 para parar: "))`

Esta linha lê o primeiro número digitado pelo usuário e armazena na variável `number`.

python

`while number != 0:`

Este é o início de um loop `while` que irá continuar enquanto o valor de `number` não for igual a zero.

python

`if number % 2 == 1:     odd_numbers += 1 else:     even_numbers += 1`

Dentro do loop `while`, a primeira coisa que o programa faz é verificar se `number` é ímpar ou par. Isso é feito com a verificação `if number % 2 == 1`. Se o número for ímpar, o programa adiciona `1` à variável `odd_numbers`. Caso contrário, o programa adiciona `1` à variável `even_numbers`.

python

`number = int(input("Digite um número ou digite 0 para parar: "))`

Esta linha solicita ao usuário que digite outro número ou zero para parar e armazena o valor digitado em `number`.

python

`print("Números ímpares contam:", odd_numbers) print("Números pares contam:", even_numbers)`

Quando o usuário digita zero, o loop `while` é interrompido e o programa imprime o número de números ímpares e pares contados durante a execução.

Espero que isso ajude você a entender o código. Qualquer dúvida ou pergunta, sinta-se à vontade para perguntar.

### como simplificar ainda mais o código

Podemos simplificar ainda mais o código usando um loop infinito `while True` em vez de repetir as mesmas linhas de código duas vezes para obter a entrada do usuário. O loop continuará até que o usuário digite o número 0, e a condição de saída será colocada dentro do loop usando a instrução `break`.

Além disso, podemos usar a função `format` para imprimir os resultados finais de uma maneira mais clara e legível.

Aqui está o código simplificado:

```python

# estabelecendo as varíaveis pares e iímpares
odd_numbers = 0
even_numbers = 0

# usando um loop infinito
# de modo a evitar a redundância de pedir duas input duas vezes

while True:
# while True foi pedido pelo instrutor
    number = int(input("Digite números para saber se são pares ou não, e zero para efetuar contagem: "))
    if number == 0:
        break
    elif number % 2 == 0:
        even_numbers += 1
    else:
        odd_numbers += 1

print("Números ímpares contam: {}".format(odd_numbers))
print("Números pares contam: {}".format(even_numbers))

```

Com essas mudanças, o código ficou mais conciso, legível e fácil de entender.