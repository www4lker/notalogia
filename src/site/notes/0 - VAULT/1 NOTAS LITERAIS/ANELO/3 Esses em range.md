---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/3-esses-em-range/","tags":["python","ANELO","ChatGPT"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# 3 Esses em range

## criado em: 
-  06-05-2023 - 18:03

### Conteúdo Relacionado
- notas: 
- tags: #python #ANELO
- Fontes & Links: 

---

Como funciona o range em python?

#ChatGPT

A função `range()` é usada para gerar uma sequência de números em Python. Ela pode ser usada em loops (por exemplo, `for`) para repetir uma ação várias vezes ou para criar uma lista de números que possa ser usada em outros contextos.
### START STOP STEP

A sintaxe básica da função `range()` é a seguinte:

```
range(start, stop, step)
```



Onde:

-   `start`: o número inicial da sequência. Por padrão, o valor é 0.
-   `stop`: o número final da sequência (não incluso). Esse argumento é obrigatório e não pode ser omitido.
-   `step`: o tamanho do passo (incremento) entre os números da sequência. Por padrão, o valor é 1.

Por exemplo, o código abaixo cria uma sequência de números de 0 a 9:

scss

`for i in range(10):     print(i)`

Isso é equivalente a:

scss

`for i in range(0, 10, 1):     print(i)`

A função `range()` também pode ser usada para criar uma lista de números. Por exemplo, o código abaixo cria uma lista de números pares de 0 a 8:

scss

`numeros_pares = list(range(0, 10, 2)) print(numeros_pares)`

Isso produz a saída:

csharp

`[0, 2, 4, 6, 8]`

Observe que o último número especificado no intervalo (`stop`) não é incluído na sequência. Além disso, o terceiro argumento (`step`) especifica o tamanho do passo entre os números da sequência.

Também é possível usar valores negativos para `step`, o que resulta em uma sequência decrescente. Por exemplo, o código abaixo cria uma lista de números ímpares de 9 a 1:

scss

`numeros_impares = list(range(9, 0, -2)) print(numeros_impares)`

Isso produz a saída:

csharp

```csharp
[9, 7, 5, 3, 1]
```