---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/lists-store-references-to-the-underlying-object-in-memory-rather-than-copies-of-the-object-itself/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# lists store references to the underlying object in memory rather than copies of the object itself

## criado em: 
-  09-05-2023 - 15:34

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023 - 3.5 Section 5 – sorting simple lists\|LATAM 2023 - 3.5 Section 5 – sorting simple lists]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Os poderes do fatiamento\|Os poderes do fatiamento]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023 - 3.6 Seção 6 - Operações em listas\|LATAM 2023 - 3.6 Seção 6 - Operações em listas]]
- tags: #ANELO 
- Fontes & Links: 

---

>Can you explain this? 
```python
list_1 = [1] 
list_2 = list_1 
list_1 [0] = 2 
print(list_2) #retorna o valor último e não o primeiro

```

In Python, variables that store lists are actually references to the list object in memory. When you create a new list and assign it to a variable (like `list_1 = [1]`), Python creates a new list object in memory and assigns a reference to that object to the variable `list_1`.

When you assign `list_2 = list_1`, you are creating a new variable (`list_2`) that references the same list object in memory as `list_1`. In other words, `list_2` is not a copy of `list_1`, but rather a reference to the same underlying list object.

So, when you modify the contents of the list using `list_1[0] = 2`, you are actually modifying the underlying list object that both `list_1` and `list_2` reference. As a result, when you print `list_2`, you will see the modified list: `[2]`.

It's worth noting that this behavior is not unique to lists in Python. Variables that store other types of objects (like dictionaries, sets, or custom classes) also store references to the underlying object in memory rather than copies of the object itself. If you want to create a copy of a list (or any other object), you need to explicitly create a new copy of the object using a method like `list.copy()` or `copy.deepcopy()`.