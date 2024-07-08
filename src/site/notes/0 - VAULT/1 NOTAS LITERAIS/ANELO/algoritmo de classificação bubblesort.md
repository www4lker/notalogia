---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/algoritmo-de-classificacao-bubblesort/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# algoritmo de classificação bubblesort

## criado em: 
-  09-05-2023 - 15:05

### Conteúdo Relacionado
- notas: 
- tags: #python #ANELO
- Fontes & Links: 

---

Bubble sort is a simple sorting algorithm that repeatedly steps through a list of items, compares adjacent elements and swaps them if they are in the wrong order. This process is repeated until the list is sorted. 

Here's how the algorithm works:

1. Start at the beginning of the list of items to be sorted.
2. Compare the first two items. If the first item is larger than the second item, swap them.
3. Move to the next pair of items, i.e. the second and third items, and compare them. If the second item is larger than the third item, swap them.
4. Continue in this way, comparing each pair of adjacent items and swapping them if they are in the wrong order, until the end of the list is reached.
5. At this point, the largest item in the list will be in its correct position. Repeat the above steps for all the remaining items in the list, except for the last one that was already sorted.
6. The process will continue until no more swaps are needed, indicating that the list is now sorted.

Bubble sort is called bubble sort because as the algorithm iterates through the list, the smaller items "bubble" to the top of the list while the larger items sink to the bottom.

While bubble sort is a simple algorithm, it has a time complexity of O(n^2), which means it is not very efficient for sorting large lists. However, it is useful for teaching basic sorting algorithms and can be used for small datasets or in cases where simplicity is more important than efficiency.