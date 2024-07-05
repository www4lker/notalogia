---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-10-de-9/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON - 10 de 9

## criado em: 
-  27-04-2023 - 13:26

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON - 6 de 9\|PYTHON - 6 de 9]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 2 - 1 de 14\|PYTHON 2 - 1 de 14]]
- tags: #python #ANELO 
- Fontes & Links: 

---

Ainda no console do Python, vimos no vídeo anterior que uma variável sempre terá um tipo associado:

```bash
pais = "Brasil"
type(pais)
```

**Resultado**

```javascript
<class 'str'>
```

Mas em nenhum local definimos explicitamente que a variável **`pais`** receberá valores do tipo string. Talvez você já tenha visto isso em outras linguagens, como C, C++, Java, em que definimos o tipo da variável na hora da sua declaração, algo como:

```java
str pais = "Brasil"
```

Mas isso em Python **não funciona**. Ou seja, no mundo Python não somos obrigados a definir explicitamente o tipo da variável. Podemos até passar outros tipos de valores para a variável:

**Primeiro teste**

```bash
pais = "Brasil"
type(pais)
```

**Resultado**

```javascript
<class 'str'>
```

**Segundo teste**

```bash
pais = 644
type(pais)
```

**Resultado**

```javascript
<class 'int'>
```

Além de funcionar, o tipo da variável também muda! O tipo da variável mudou dinamicamente, de acordo com o valor que é atribuído a ela, logo, o tipo da variável é definido de acordo com o valor que ela guarda, isso faz parte da **tipagem dinâmica** do Python.

Agora temos tudo para começar o nosso projeto no próximo capítulo!
