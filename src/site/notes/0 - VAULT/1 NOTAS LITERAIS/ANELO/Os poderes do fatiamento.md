---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/os-poderes-do-fatiamento/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Os poderes do fatiamento

## criado em: 
-  09-05-2023 - 15:45

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/engessado na hora de codar\|engessado na hora de codar]]
- tags: #python #ANELO 
- Fontes & Links: 

---

The slicing operator `[:]` in Python can also be used to create a shallow copy of a list. 

For example, if you have a list `list_1` and you want to create a new list `list_2` that contains the same elements as `list_1`, you can use the slicing operator like this:

```
list_1 = [1, 2, 3, 4]
list_2 = list_1[:]
```

This creates a new list `list_2` with the same elements as `list_1`, but it is a separate list object in memory. Any modifications made to `list_1` will not affect `list_2`, and vice versa.

It's important to note that slicing creates a shallow copy, which means that if the original list contains mutable objects (like other lists or dictionaries), those objects will still be references to the same underlying objects in memory in the copied list. This means that changes made to those objects will be reflected in both the original and copied lists.

To create a deep copy of a list (i.e., a copy where all elements, including mutable objects, are also copied), you can use the `copy.deepcopy()` method from the `copy` module.