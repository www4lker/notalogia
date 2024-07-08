---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-avancando-na-linguagem-4-de-7/","tags":["python","alura","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON AVANÇANDO NA LINGUAGEM - 4 DE 7
## Conhecendo e trabalhando com Tuplas

## criado em: 
-  11-05-2023 - 15:29

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON AVANÇANDO NA LINGUAGEM - 1 DE 7\|PYTHON AVANÇANDO NA LINGUAGEM - 1 DE 7]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON AVANÇANDO NA LINGUAGEM - 2 DE 7\|PYTHON AVANÇANDO NA LINGUAGEM - 2 DE 7]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON AVANÇANDO NA LINGUAGEM - 3 DE 7\|PYTHON AVANÇANDO NA LINGUAGEM - 3 DE 7]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON AVANÇANDO NA LINGUAGEM - 5 DE 7\|PYTHON AVANÇANDO NA LINGUAGEM - 5 DE 7]]- 
- tags: #python #alura #ANELO 

---
## O que são tuplas?

No capítulo anterior, vimos que **strings** e **listas** são tipos de **sequências**. Além dessas sequências, também há o **range**, que vimos no curso anterior, e a **tupla**, que veremos agora.

## Conhecendo mais uma sequência, a tupla

Nós gostaríamos de definir os dias da semana, então podemos defini-los em uma lista:

```python-repl
>>> dias = ["Domingo", "Segunda", "Terça", "Quarta", "Quinta", "Sexta", "Sábado"]
```

Faz sentido apagar um dia da semana? Provavelmente não, já que a semana sempre possui sete dias. Assim como também não faz sentido criarmos um novo dia da semana, mas nada nos impede de criarmos um:

```python
>>> dias = ["Domingo", "Segunda", "Terça", "Quarta", "Quinta", "Sexta", "Sábado"]
>>> dias.append("Sábado2")
>>> dias
['Domingo', 'Segunda', 'Terça', 'Quarta', 'Quinta', 'Sexta', 'Sábado', 'Sábado2']
```

Portanto, essa lista deveria ser fixa, inalterável. Para isso existe o **tuple**, que é uma lista imutável.

## Criando uma tupla

Para criar uma tupla, é bem simples. É do mesmo jeito que criamos uma lista, mas ao invés de usar colchetes, usamos parênteses:

```python
>>> dias = ("Domingo", "Segunda", "Terça", "Quarta", "Quinta", "Sexta", "Sábado")
>>> type(dias)
<class 'tuple'>
```

Agora não conseguimos adicionar, nem remover elementos. Por exemplo:

```python
>>> dias = ("Domingo", "Segunda", "Terça", "Quarta", "Quinta", "Sexta", "Sábado")
>>> dias.append("Sábado2")
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'tuple' object has no attribute 'append'
```

## Listas e tuplas juntas

### Tuplas dentro de uma lista

Agora queremos armazenar instrutores, cada um com o seu nome e sua idade:

```python-repl
>>> instrutor1 = ("Nico", 39)
>>> instrutor2 = ("Flávio", 37)
```

Agora podemos criar uma **lista de instrutores**:

```python-repl
>>> instrutor1 = ("Nico", 39)
>>> instrutor2 = ("Flávio", 37)
>>> instrutores = [instrutor1, instrutor2]
```

Isso mesmo! A lista pode armazenar tuplas dentro dela. Ao imprimi-la, vemos:

```css
>>> instrutores
[('Nico', 39), ('Flávio', 37)]
```

Podemos acessar somente um tupla pelo seu índice na lista:

```less
>>> instrutores[0]
('Nico', 39)
```

E podemos também acessar, através da lista, somente um elemento da tupla. Por exemplo, para acessar a idade do Nico, acessamos a sua tupla, e acessamos a sua idade passando mais um índice:

```css
>>> instrutores[0][1]
39
```

E podemos fazer o contrário também, podemos colocar listas dentro de tuplas :)

## Convertendo listas em tuplas

Agora temos a seguinte situação: precisamos ler de um arquivo, mas não sabemos quantas linhas esse arquivo tem. Então, vamos lendo linha por linha, e adicionando-as em uma lista:

```python-repl
>>> linhas = []
>>> linhas.append("linha 1")
>>> linhas.append("linha 2")
>>> linhas.append("linha 3")
```

Em algum momento o arquivo irá acabar, e quando esse momento chegar, não queremos mais adicionar linhas à lista. Então, devemos transformar a lista em uma lista imutável, no caso uma tupla. E o Python possui uma função específica para isso, a **`tuple()`**, que recebe por parâmetro a lista a ser convertida:

```python
>>> linhas_tuple = tuple(linhas)
>>> type(linhas_tuple)
<class 'tuple'>
>>> linhas_tuple
('linha 1', 'linha 2', 'linha 3')
```

## Convertendo tuplas em listas

Com uma simples função, transformamos uma lista em uma tupla! E o contrário também pode ser feito, com a função **`list()`**:

```python
>>> linhas_list = list(linhas_tuple)
>>> type(linhas_list)
<class 'list'>
>>> linhas_list
['linha 1', 'linha 2', 'linha 3']
```

#### Para saber mais: Set

##### Quando uma sequência não é suficiente

Já aprendemos algumas características das sequências. Elas guardam valores de qualquer tipo de dado e possuem uma determinada ordem, pois possuem um índice. As sequências também são chamadas de coleções e são o _arroz e feijão_ para qualquer desenvolvedor Python!

Agora dá uma olhada no exemplo abaixo onde criamos uma lista de CPFs:

```ini
lista = [11122233344, 22233344455, 33344455566]
```

Nada errado aqui, mas imagine agora que você precisa evitar que exista algum CPF duplicado nesta lista. Isso é algo muito comum no dia-a-dia! Em muitas circunstâncias precisamos de uma coleção que não permita valores duplicados, mas nada nos impede adicionar um mesmo CPF nessa lista, por exemplo:

```bash
lista.append(11122233344) #funciona!
```

Isso também funciona se fosse uma tuple! Uma tuple também permite elementos duplicados!

##### Conhecendo o set

E agora? Será que o Python não oferece alguma coleção onde não podem existir elementos duplicados? Claro que existe uma coleção com esse propósito e ela se chama **set**.

Veja o mesmo exemplo, mas agora inicializando um set:

```ini
colecao = {11122233344, 22233344455, 33344455566}
```

Repare que usamos `{}` chaves para declarar os elementos iniciais. Pouca diferença comparando com as sequências, não?

##### Adicionando elementos no set

Para adicionar um elemento a um set devemos chamar a função `add` (ao invés da `append`):

```csharp
colecao.add(44455566677) #vai adicionar pois não existe ainda
```

E se usarmos um CPF que já existe? Não deve funcionar, certo? Vamos testar,e ver que o set vai ignorá-lo:

```bash
colecao.add(11122233344) #nao vai adicionar pois este CPF já existe!
```

##### set não possui um índice

É importante notar que o set não é uma sequência, pois não tem um índice. O código abaixo não funciona:

```vbnet
colecao[0]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'set' object does not support indexing
```

Isso mesmo, não tem índice. E como não temos um índice não sabemos em qual ordem vem os valores quando imprimimos um **set** de dentro de um laço `for`:

```bash
for cpf in colecao:
     print(cpf)
```

Imprime:

```undefined
11122233344
44455566677
33344455566
22233344455
```

Repare que os elementos foram listados fora da ordem de inserção. Isso acontece porque o set não é ordenado.

##### Resumindo

_Um set é uma coleção não ordenada de elementos. Cada elemento é único, isso significa que não existem elementos duplicados dentro do set._

Respire fundo e fique tranquilo pois o `set` será abordado ainda com mais detalhe em outros cursos. Vamos continuar?

# Para saber mais: Dictionary

Você aguenta aprender mais um pouco sobre coleções? Então vamos lá :)

Vamos lembrar rapidamente do último exemplo no vídeo quando misturamos as listas e tuples. Primeiro criamos pessoas com nome e idade usando `tuple`s:

```ini
pessoa1 = ("Nico", 39)
pessoa2 = ("Flavio", 37)
pessoa3 = ("Marcos", 30)
```

Depois guardamos as tuples dentro de uma lista:

```ini
instrutores = [pessoa1, pessoa2, pessoa3]
```

Se imprimimos `instrutores` recebemos:

```css
[('Nico', 39), ('Flavio', 37), ('Marcos', 30)]
```

Para saber a idade do `Flavio`, devemos usar os índices (primeiro da lista, depois da tuple). Lembrando que acessamos o índice com os `[]`:

```css
instrutores[1][1]
37
```

Agora vem o problema: E se não sabemos a posição do `Flavio`? Em geral, como podemos descobrir a idade de um instrutor sem saber a posição dele?

## Instrutor pelo nome

Repare que temos, na nossa coleção, sempre um **nome** _associado_ com a **idade**. Sempre temos um par de valores, aqui é:

```yaml
nome : idade
```

Invés de usar a posição gostaria de descobrir a idade através do nome, algo assim:

```css
instrutores['Flavio']
```

Só que isso não vai funcionar com lista, nem com tuple, nem combinando os dois :( É preciso usar uma nova estrutura de dados, o **Dictionary**!

## Conhecendo o dictionary

Para criar um dicionário devemos inicializar os instrutores de um modo um pouco diferente. Veja o código:

```ini
instrutores = {'Nico' : 39, 'Flavio': 37, 'Marcos' : 30}
```

Repare que usamos as chaves `{}` (como se fosse um set), mas sempre tem em pares. O primeiro par é `'Nico' : 39`, o segundo é `'Flavio': 37`, etc.

Nesse par, temos no lado esquerdo a **chave** e no lado direito o `valor`. Isso é importante pois usamos a chave para recuperar um valor e assim resolvemos nosso problema:

```css
instrutores['Flavio']
```

Imprime:

```undefined
37
```

Isso foi apenas uma introdução, mas não se preocupe pois veremos ainda mais sobre dicionários dentro da carreira Python 3.

