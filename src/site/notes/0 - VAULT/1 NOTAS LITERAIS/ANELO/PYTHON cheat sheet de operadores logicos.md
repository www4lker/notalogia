---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-cheat-sheet-de-operadores-logicos/","tags":["python","logica","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON cheat sheet de operadores logicos

## criado em: 
-  06-05-2023 - 18:06

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023 - 3.1 Section 3 - Lógica e operações de bit em Python\|LATAM 2023 - 3.1 Section 3 - Lógica e operações de bit em Python]]
- tags: #python #logica #ANELO 
- Fontes & Links: 

---

Claro, segue abaixo um cheat sheet dos operadores lógicos em Python:

Operadores lógicos em Python:

-   `and`: Retorna `True` se ambos os operandos forem verdadeiros, caso contrário, retorna `False`.
-   `or`: Retorna `True` se pelo menos um dos operandos for verdadeiro, caso contrário, retorna `False`.
-   `not`: Retorna o oposto do valor do operando. Se o operando for verdadeiro, retorna `False`, caso contrário, retorna `True`.

Exemplos:

```python
a = True
b = False
c = True

# Exemplo com operador 'and'
print(a and c)  # True
print(a and b)  # False

# Exemplo com operador 'or'
print(a or b)   # True
print(b or b)   # False

# Exemplo com operador 'not'
print(not a)    # False
print(not b)    # True
```



Também é possível combinar operadores lógicos para criar expressões mais complexas:

```python

a = True
b = False
c = True

# Exemplo com múltiplos operadores lógicos
print((a and b) or (not c))    # True
print((not a) and (b or c))    # False

```

Nesses exemplos, as expressões entre parênteses são avaliadas primeiro, seguindo a ordem de precedência dos operadores (primeiro o `not`, depois o `and` e, por fim, o `or`).
