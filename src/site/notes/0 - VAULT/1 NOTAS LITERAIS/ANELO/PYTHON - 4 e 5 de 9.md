---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-4-e-5-de-9/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# PYTHON - 4 e 5 de 9

## criado em: 
-  27-04-2023 - 12:55

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON - 3 de 9\|PYTHON - 3 de 9]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON - 6 de 9\|PYTHON - 6 de 9]]
- tags: #python #ANELO 
- Fontes & Links: 

---

Os sistemas operacionais baseados no Debian já possuem o Python 3 pré-instalado, mas o comandos para instalá-lo pelo terminal é:

```sql
sudo apt-get update
sudo apt-get install python3
```

Assim como no Windows, você pode verificar se o Python 3 está instalado executando o seguinte comando:

```undefined
python3 -V
```

E para executar o Python 3, basta rodar o comando **`python3`** no terminal.

## Instalando o Python no MacOS

Para instalar o Python 3 no MacOS, temos duas opções, através do [Homebrew](http://brew.sh/index_pt-br.html), fazemos:

```sql
brew update
brew install python3
```

Mas caso você não utiliza o Homebrew, podemos baixar o instalador do Python através do seu [site oficial](https://www.python.org/). Assim como no Windows, na sessão de Downloads, o site automaticamente já detectará o seu sistema operacional e disponibilizará o instalador específico para o seu MacOS, portanto é só baixar o Python 3, na sua versão mais atual.

E assim como nos sistemas baseados no Debian, verificamos a versão do Python com o seguinte comando:

```undefined
python3 -V
```

E o executamos rodando o comando **`python3`** no terminal.

---

Também conseguimos utilizar o Python sem instalá-lo na nossa máquina, executando-o através de um serviço na web. Há vários sites que disponibilizam esse serviço, entre eles o [**repl.it**](https://repl.it/). Nele podemos programar em várias linguagens, para começar basta clicar em **_Start coding now!_** e escolher o **Python3**.

À esquerda escrevemos o código em Python e à direita é a saída. Podemos testar esse serviço, imprimindo uma mensagem:

```bash
print("ola aluno! bem vindo!!")
```

Ao clicar em **_run_**, a mensagem é impressa à direita.

É uma boa alternativa caso não tenhamos o Python instalado localmente, mas é bom ter em mente que em algum momento a instalação local será necessária :)