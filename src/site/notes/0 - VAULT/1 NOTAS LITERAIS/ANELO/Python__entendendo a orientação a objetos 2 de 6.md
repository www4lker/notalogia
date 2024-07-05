---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-entendendo-a-orientacao-a-objetos-2-de-6/","tags":["python","alura","poo","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# Python__entendendo a orientação a objetos 2 de 6

## criado em: 
-  20-05-2023 - 11:18

### Conteúdo Relacionado
- notas: 
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python__entendendo a orientação a objetos 1 de 6\|Python__entendendo a orientação a objetos 1 de 6]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python__entendendo a orientação a objetos 2 de 6\|Python__entendendo a orientação a objetos 2 de 6]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python__entendendo a orientação a objetos 3 de 6\|Python__entendendo a orientação a objetos 3 de 6]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python__entendendo a orientação a objetos 4 de 6\|Python__entendendo a orientação a objetos 4 de 6]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python__entendendo a orientação a objetos 5 de 6\|Python__entendendo a orientação a objetos 5 de 6]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python__entendendo a orientação a objetos 6 de 6\|Python__entendendo a orientação a objetos 6 de 6]]
- tags: #python #alura #poo #ANELO 
- Fontes & Links: https://cursos.alura.com.br/formacao-Python-linguagem

---

## Classe e Objeto

Vimos que o paradigma da Orientação a Objetos está relacionado com a organização do código, um conceito que começamos a aplicar no código. Juntamos as características — como `numero`, `titular`, `saldo` e `limite` — com as funcionalidades de uma conta.

Organizamos o código, porém, será que devemos continuar com essa abordagem? No mundo procedural, não somos obrigados a adotar OO, não há algo que reforça a necessidade de utilizarmos essa maneira mais organizada de escrever o código. Ou seja, cabe ao desenvolvedor decidir se quer adotar o paradigma OO.

Em um sistema maior, é grande a chance de que as funções fiquem separadas em arquivos e módulos diferentes do projeto. No entanto, pode ser trabalhoso encontrar onde está cada trecho do código e isso, pode resultar em retrabalho e escrever funções já existentes. O paradigma Orientado a Objetos nos incentiva a agrupar funcionalidades relacionadas em um mesmo lugar. Este é um dos principais problemas.

Mas existe ainda outro problema, nós temos a opção de acessar o saldo diretamente no console, sem chamar uma funcionalidade e definir um novo valor como veremos abaixo:

```python-repl
>>> conta["saldo"] = -300.0
```

Porém, ninguém deveria ter acesso ao saldo diretamente, sendo primeiramente necessário **depositar** ou **sacar** o dinheiro. Deveríamos manipular os dados somente por meio das funções.

Nós queremos resolver essas duas questões utilizando OO. Para isto, criaremos um objeto, no caso, falamos de uma conta. Trabalharemos com algo do mundo real, uma conta é algo concreto e inclui diversos dados. Porém, antes de termos um objeto, devemos definir as suas características.

A seguir faremos uma analogia: quando preparamos um bolo, geralmente, seguimos uma receita que define os ingredientes e o modo de preparação. A nossa conta é um objeto concreto assim como o bolo, e também precisamos definir antes uma receita. Porém, a "receita" no mundo OO recebe o nome de classe. Ou seja, antes de criarmos um objeto definiremos uma classe.

O próximo passo será gerar um novo arquivo Python, que receberá o nome de `conta.py`.

![criando novo arquivo pyhton](https://s3.amazonaws.com/caelum-online-public/693-python-oo/Transcri%C3%A7%C3%A3o/2.1_1_criando+novo+arquivo+python.png)

Dentro do arquivo gerado, definiremos a classe, que será antecedida pela palavra reservada `class`, utilizada na linguagem **Python** para definir a "receita". A classe vai receber o nome `Conta`, que por não ser uma palavra reservada, poderia ser outro qualquer.

Poderíamos ter adotado `ContaCorrente` como nome da classe, por exemplo. Desta forma, seguiríamos o padrão **CamelCase**, no qual cada palavra é iniciada com a letra maiúscula. Seguiremos esta boa prática e escreveremos `Conta` com a primeira letra em caixa alta, seguida pela pontuação `:`, com isto indicaremos que se trata do início de um bloco de código.

Todo o conteúdo adicionado após `:` fará parte desta classe. Para fazer o código funcionar, incluiremos a palavra-chave `pass` no arquivo `conta.py`.

```kotlin
class Conta:

    pass
```

Em seguida, reiniciaremos o console e importaremos do módulo conta.

```python-repl
>>> from conta import Conta
```

Para criarmos um primeiro objeto, no console, digitaremos o nome da classe `Conta` utilizando os parênteses (**`()`**) para que o código seja executado.

```python
>>> Conta()
<conta.Conta object at 0x10715f518>
```

Ele imprimiu a informação de que temos um objeto baseado na classe `Conta`, localizado dentro do módulo `conta`. Observe que a letra maiúscula foi utilizada para diferenciar as duas nomenclaturas. O objeto foi criado em memória e imprime o endereço `0x10715f518`.

Seguiremos com a analogia do bolo... É como se tivéssemos passado a receita para uma fábrica, determinando a tarefa de fabricação do objeto para outro. No entanto, onde essa fábrica vai criar o bolo? Temos um endereço, mas não precisaremos manuseá-lo. A linguagem Python irá abstrair esse dado para nós.

Se quisermos trabalhar com o objeto, teremos que fazer algo a mais. Chamaremos a classe `Conta` novamente, guardando o retorno dentro da referência `conta`.

```python-repl
>>> conta = Conta()
```

Esta referência guardará o endereço em memória para localizar o objeto posteriormente. É como se a fábrica nos avisasse em qual armário o bolo foi guardado, porém, o endereço não é o objeto em si. Trata-se apenas de uma referência.

Se executarmos a linha `conta = Conta()` não teremos nenhum retorno, porque o resultado da execução da `Conta` foi atribuída a `conta`. Mas, se executarmos `conta` no console, teremos o seguinte retorno:

```python
>>> conta
<conta.Conta object at  0x10715fe10>
```

Observe que o endereço retornado é diferente do que foi impresso na primeira execução. Isto ocorreu porque chamamos a classe e foi criado um segundo objeto.

Geramos dois objetos do tipo `conta`, baseada na mesma classe. Vale lembrar que uma classe pode gerar vários objetos, porém, queremos que ela tenha várias informações. É necessário que `Conta` trabalhe com vários dados para depositar e sacar.

---

Seguimos com nossa introdução ao mundo de Orientação a Objetos, vimos três conceitos fundamentais. A classe `Conta` está praticamente vazia, mas ela já existe e funciona como a receita do projeto, que é construído a partir da seguinte execução:

```python-repl
>>> conta = Conta()
>>> conta
<conta.Conta object at 0x10715fef0>
```

Chamaremos a classe como se fosse uma função. O objeto é criado em memória por baixo dos panos pelo Python. Ele abstrai este processo, portanto não devemos nos preocupar com isso.

O objeto será criado na hora de chamar a classe `Conta`. Em memória, o objeto é criado e o Python devolve o endereço que será guardado dentro da variável `conta`.

Em Orientação a Objetos, as variáveis são denominadas: **referências**.

Estes conceitos servem para diversas linguagens, além de Python. Se trabalharmos com PHP ou Java, faremos o mesmo. Teremos uma referência, uma classe, uma construção de objeto que poderemos aplicar em outra linguagem.

Nossa classe continua vazia, a seguir, definiremos o conteúdo dela, definindo quais são suas **características**. No mundo Orientação a Objetos, essas características são chamadas de **atributos**.

Os atributos da conta são: `numero`, `titular`, `saldo` e `limite`. Na hora de criar um objeto, o Python pode executar uma função, automaticamente, dentro da classe para definir os atributos.

Sendo uma função automática, receberá um nome especial. Adicionaremos dois caracteres `_` antes e depois do nome da função construtora, para criarmos `__init__`. O Python constrói o objeto, cria um lugar na memória e depois chama a função `__init__`. Como demonstração, segue o código:

```ruby
class Conta:
    def __init__(self):
        print("Construindo objeto...")
```

Em seguida, reiniciaremos o console e importaremos novamente:

```python-repl
>>> from conta import Conta
>>> conta = Conta()
Construindo objeto ...
```

Automaticamente ele retornou `Construindo objeto...`, pois o Python cria o objeto em memória, encontra um espaço e, depois, a função construtora é chamada.

Criamos uma função, mas a ideia é definir os atributos e as características. Para isso, precisaremos da variável `self`, que está dentro da função `__init__()`.

Em seguida, no arquivo `conta.py`, usaremos interpolação e `format(self)` dentro de `print()`. O Python cria automaticamente `self`.

```python
class Conta:
    def __init__(self):
        print("Construindo objeto...{}".format(self))
```

Reiniciaremos o console e testaremos o código.

```python-repl
>>> from conta import Conta
>>> conta = Conta()
Construindo objeto ... <conta.Conta object at 0x1020d7f28>
```

Repare que ele já conhece esta saída. Localizamos a conta, o objeto e o endereço. Considerando que é a mesma saída, ele imprimirá o valor da referência.

> `self` é a referência que sabe encontrar o objeto construído em memória.

Agora que temos o endereço, utilizaremos `self` para acessar o objeto e definir seus atributos e características.

```python
class Conta:

    def __init__(self):
        print("Construindo objeto...{}".format(self))
        self.numero = 123
        self.titular = "Nico"
        self.saldo = 55.0
        self.limite = 1000.0
```

Em `self.numero`, o caractere "ponto" (`.`) é um comando de ida ao objeto e `numero`, `titular`, `saldo` e `limite` são atributos.

Reiniciaremos o console e testaremos novamente, agora, com os atributos. Tudo continua funcionando, sem mudanças porque não utilizamos os atributos.

No entanto, não queremos deixar o valor dos atributos fixos, o ideal é que eles variem de acordo com a conta que está sendo criada.

Em `teste.py`, nós havíamos definido alguns parâmetros na função `cria_conta ()`,:

```cpp
def cria_conta(numero, titular, saldo, limite):
    conta = {"numero": numero, "titular": titular, "saldo": saldo, "limite": limite}
    return conta
```

De volta a `conta.py`, o próximo passo será também definir parâmetros para a função `__init__()`, aproveitando os mesmo dados da função `cria_conta()`:

```python
class Conta:

    def __init__(self, numero, titular, saldo, limite):
        print("Construindo objeto...{}".format(self))
        self.numero = 123
        self.titular = "Nico"
        self.saldo = 55.0
        self.limite = 1000.0
```

Além do `self` que é passado automaticamente, queremos que os dados sejam alterados, por isso, adicionaremos os nomes dos parâmetros.

```python
class Conta:

    def __init__(self, numero, titular, saldo, limite):
        print("Construindo objeto...{}".format(self))
        self.numero = numero
        self.titular = titular
        self.saldo = saldo
        self.limite = limite
```

Desta forma, o limite do objeto (`self.limite`) será o `limite` recebido do parâmetro da função `__init__()`. E qual é a origem dos dados? O valor do `self` é passado pelo Python, responsável pela criação final do objeto em memória. No entanto, os valores dos parâmetros como `numero` deverão ser definidos usando a aplicação.

Iremos importar `Conta` no console, criar a conta e especificar os valores:

```python-repl
>>> from conta import Conta

>>> conta = Conta(123, "Nico", 55.5, 1000.0)
Construindo objeto ... <conta.Conta object at 0x11077bcc0>
```

Observe que passamos os parâmetros da conta e nosso código foi executado. Isso é um bom sinal e, por isso, criaremos novos objetos.

```python-repl
>>> conta2 = Conta(321, "Marco", 100.0, 1000.0)
```

Será gerada a `conta2`, sendo possível acessar as duas contas criadas pelo console.

```python
>>> conta
<conta.Conta object at 0x11077bcc0>

>>> conta2
<conta.Conta object at 0x1109e1da0>
```

Cada conta possui um número, titular, saldo e limite, agora, falta trabalharmos com esses atributos. Nós faremos isso a seguir.