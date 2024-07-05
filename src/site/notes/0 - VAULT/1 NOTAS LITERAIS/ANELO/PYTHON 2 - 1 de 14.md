---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-2-1-de-14/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON 2 - 1 de 14

## criado em: 
-  27-04-2023 - 13:34

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 2 - 3 de 14\|PYTHON 2 - 3 de 14]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON - 10 de 9\|PYTHON - 10 de 9]]
- tags: #python #ANELO 
- Fontes & Links: 

---
## instalar o pyCharm

![Pasted image 20230429192022.png](/img/user/0%20-%20VAULT/1%20NOTAS%20LITERAIS/ANELO/Pasted%20image%2020230429192022.png)

No capítulo anterior fizemos os primeiros passos com o Python, desde a sua instalação e até vimos um pouco da sua sintaxe no console. Mas para escrever uma aplicação completa, utilizando o console, não parece ser uma boa ideia. Podemos ter um editor de texto que nos auxilie nessa programação, nos permitindo trabalhar com vários arquivos, auxiliando a nossa vida.

Há várias opções de editores de texto no mercado, entre elas o [Atom](https://atom.io/) e o [Sublime Text](https://www.sublimetext.com/). Apesar de esses editores nos ajudarem a escrever o código, eles não são focados no Python, e sim em dar suporte a várias linguagens. Então, vamos utilizar uma ferramenta (**IDE**, do inglês _**I**ntegrated **D**evelopment **E**nvironment_) só focada para o Python, assim como existe o Eclipse para o Java.

## Instalando o PyCharm

Uma IDE que é voltada exclusivamente para o Python é o [**PyCharm**](https://www.jetbrains.com/pycharm/), e é ela que iremos utilizar aqui no treinamento. A sua instalação é bem simples, basta acessar a sessão de [**Download**](https://www.jetbrains.com/pycharm/download/) do site oficial, baixar e instalar a versão **_Community_** da IDE, já que a versão **_Professional_** é paga.

## Conhecendo o PyCharm e criando o primeiro projeto

Após instalar o PyCharm, vamos abri-lo e criar o nosso primeiro projeto, clicando em **_Create New Project_**. Na tela que irá se abrir, nos é perguntado a localização do projeto e a versão do Python. Vamos criar o projeto **jogos**, dentro da pasta **PycharmProjects** mesmo, e nos atentar à versão do Python (caso você tenha mais de uma versão instalada) ela deve ser a **versão 3**.

O projeto ficará sendo exibido na esquerda, e para criar o primeiro arquivo Python dentro dele, basta clicar com o botão direito do mouse em cima dele e clicar em **_New -> Python File_**, vamos colocar o nome do arquivo de **adivinhacao.py**.

A fim de testes, vamos imprimir uma mensagem simples:

```bash
print("Bem vindo ao jogo de Adivinhação!")
```

Para executar o arquivo, clicamos em **_Run -> Run..._** no menu superior, e selecionamos o arquivo que acabamos de criar. O console do PyCharm é aberto e exibe a saída do nosso programa, que é a mensagem **Bem vindo ao jogo de Adivinhação!**.

Em uma só tela, conseguimos ver os arquivos do projeto, o seu código fonte e o console, que exibe a saída do programa que for executado. Há vários outros recursos que ainda veremos mais à frente, mas o primeiro passo foi realizado!