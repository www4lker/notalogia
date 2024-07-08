---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/funcoes/","tags":["python","teoria","chatgpt","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# Funções

## criado em: 
-  20-05-2023 - 11:14

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Maratona LATAM 2023_PYTHON_SENAC\|Maratona LATAM 2023_PYTHON_SENAC]]
- tags: #python #teoria #chatgpt #ANELO 
- Fontes & Links: 

---

Uma função em Python é um bloco de código reutilizável que realiza uma tarefa específica. Elas são definidas usando a palavra-chave `def`, seguida do nome da função, parênteses `()` e dois pontos `:`. As funções podem ter parâmetros opcionais e retornar valores usando a palavra-chave `return`. Aqui está um exemplo básico:

```python
# Definindo uma função
def saudacao(nome):
    return f'Olá, {nome}!'

# Chamando a função
mensagem = saudacao('João')
print(mensagem)  # Saída: Olá, João!

```

Funções também podem ter parâmetros padrão, que são valores atribuídos aos parâmetros caso nenhum valor seja fornecido durante a chamada da função. Aqui está um exemplo:

```python

def saudacao(nome='amigo'):
    return f'Olá, {nome}!'

mensagem = saudacao()  # Nenhum valor fornecido, usa o padrão 'amigo'
print(mensagem)  # Saída: Olá, amigo!

```