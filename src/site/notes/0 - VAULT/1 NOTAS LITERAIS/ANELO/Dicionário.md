---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/dicionario/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# Dicionário

## criado em: 
-  20-05-2023 - 11:10

### Conteúdo Relacionado
- notas: 
- tags: #python #ANELO 
- Fontes & Links: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python__entendendo a orientação a objetos 1 de 6\|Python__entendendo a orientação a objetos 1 de 6]]

---

Um dicionário é uma estrutura de dados em Python que permite armazenar pares chave-valor. Cada chave é única e usada para acessar o valor correspondente. Os dicionários são declarados usando chaves `{}` e os pares chave-valor são separados por dois pontos `:`. Aqui está um exemplo simples de um dicionário:

```python
# Criando um dicionário
dicionario = {'chave1': valor1, 'chave2': valor2, 'chave3': valor3}

# Acessando valores no dicionário
print(dicionario['chave1'])  # Saída: valor1

# Adicionando um novo par chave-valor
dicionario['chave4'] = valor4

# Iterando sobre as chaves do dicionário
for chave in dicionario:
    print(chave, dicionario[chave])

```