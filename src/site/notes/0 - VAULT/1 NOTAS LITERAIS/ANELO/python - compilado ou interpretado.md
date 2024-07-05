---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-compilado-ou-interpretado/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# python - compilado ou interpretado

## criado em: 
-  30-04-2023 - 17:40

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON 9 - final\|PYTHON 9 - final]]
- tags: #python #ANELO 
- Fontes & Links: 

---
## Python é interpretado ou compilado?

O senso comum é que o Python é uma **linguagem interpretada**. **_Interpretado_** significa que não há um processo de compilação que traduz o código fonte em algum código nativo, que o seu computador entende. A [documentação do Python](https://docs.python.org/3/glossary.html) confirma isso, no entanto também menciona a presença de um compilador:

**_"Python is an interpreted language, as opposed to a compiled one, though the distinction can be blurry because of the presence of the bytecode compiler."_**

Traduzido livremente: **"Python é uma linguagem interpretada, em oposição às compiladas, embora a distinção possa ficar desfocada devido à presença do compilador de bytecode."**

Temos um compilador, porém de bytecode. Bytecode é um código intermediário, normalmente independente do sistema operacional. Então, Python é uma linguagem compilada também? Em 2003, Fredrik Lundh, em seu artigo [Compiling Python Code](http://effbot.org/zone/python-compile.htm), título que perverte o senso comum, começa:

**_"Python source code is automatically compiled into Python byte code by the CPython interpreter. Compiled code is usually stored in PYC (or PYO) files, and is regenerated when the source is updated, or when otherwise necessary."_**

Novamente traduzindo livremente: **_"O código fonte é automaticamente compilado para bytecode do Python pelo interpretador CPython. O código compilado é comumente armazenado nos arquivos no PYC (ou PYO), sendo regerado quando o arquivo fonte é atualizado ou quando é necessário."_**

E aí? Python é uma linguagem interpretada ou compilada? As duas coisas? Há discussões acaloradas entre desenvolvedores, cada um com sua opinião. Então, [uma resposta interessante](http://stackoverflow.com/questions/6889747/is-python-interpreted-or-compiled-or-both) está no StackOverFlow, aliás, a resposta mais bem avaliada:

**_"First off, interpreted/compiled is not a property of the language but a property of the implementation (...) Python is compiled. Not compiled to machine code ahead of time (i.e. "compiled" by the restricted and wrong, but also common definition), "only" compiled to bytecode"_**

Traduzindo: **_"O fato de uma linguagem ser interpretada ou compilada não é uma questão da linguagem, mas da sua implementação. (...) Python é compilada. Não compilada para o código de máquina antes da execução, apenas para o bytecode._**

Isso significa que alguém pode implementar o Python totalmente compilado, totalmente interpretado ou ambos, a linguagem continua a mesma. Ser compilada/interpretada é mais propriedade da implementação do Python do que da linguagem.

E você, o que pensa dessa definição?
