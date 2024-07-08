---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/linux-inicial-zip/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# Linux - inicial - ZIP

## criado em: 
-  02-08-2023 - 10:35

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Linux - inicial\|Linux - inicial]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Linux - inicial- touch\|Linux - inicial- touch]]
- tags: #ANELO 
- Fontes & Links: 

---

# 02 Criando e abrindo ZIP

Agora que já sabemos como trabalhar com arquivos e diretórios, copiá-los, movê-los, etc, vamos ver como compactá-los. Queremos, por exemplo, compactar o `workspace`, cujo conteúdo podemos conferir utilizando o comando `ls`:

```r
bemvindo2.txt  bemvindo.txt  projetos-c#  projetos-java  projetos-php
```

Primeiramente precisamos estar no diretório ao qual ele pertence com o comando `cd ..` para subir um diretório acima e depois usamos o comando `zip` informando o nome do arquivo que será gerado e o que o comando deve compactar:

```python
zip work.zip workspace/
```

A mensagem `adding: workspace/ (stored 0%)` será exibida. Lembre-se que `work.zip` é o nome que demos para o arquivo de compactação. Podemos verificar rapidamente o conteúdo do arquivo compactado utilizando o comando `unzip -l work.zip` (o comando após unzip é a letra L minúscula, e não o número 1) dessa forma conseguimos observar quais arquivos e diretórios foram compactados.

É importante observar que, da mesma forma que os comandos para apagar e copiar, o comando `zip` não é suficiente para compactar todos os arquivos e diretórios dentro de `workspace`. Se você conferiu o conteúdo do _zip_, percebeu que apenas o diretório `workspace` foi compactado, mas nenhum dos seus arquivos e subdiretórios estava presente no _zip_ final. Para isso precisamos usar a ferramenta de recursividade aqui também, ou seja, o `-r` em conjunto com o comando `zip`:

```python
zip -r work.zip workspace/
```

Esse comando apresentará uma saída diferente, informando os arquivos encontrados e adicionados ao zip final.

```bash
updating: workspace/ (stored 0%)
  adding: workspace/bemvindo2.txt (stored 0%)
  adding: workspace/projetos-php/ (stored 0%)
  adding: workspace/projetos-java/ (stored 0%)
  adding: workspace/projetos-java/bemvindo.txt (stored 0%)
  adding: workspace/bemvindo.txt (stored 0%)
  adding: workspace/projetos-c#/ (stored 0%)
  adding: workspace/projetos-c#/bemvindo.txt (stored 0%)
```

Para descompactar o arquivo _zip_ utilizamos o comando `unzip`, informando o nome do arquivo `work.zip`.

```bash
Archive: work.zip
    creating: workspace/
  extracting: workspace/bemvindo2.txt
    creating: workspace/projetos-php/
    creating: workspace/projetos-java/
  extracting: workspace/projetos-java/bemvindo.txt
  extracting: workspace/bemvindo.txt
    creating: workspace/projetos-c#/
  extracting: workspace/projetos-c#/bemvindo.txt
```

> Descompactar os arquivos do _zip_ no mesmo diretório irá sobrescrever os arquivos já existentes. Experimente remover o diretório `workspace` com o comando `rm` antes de descompactar o arquivo `work.zip`. Utilize também o comando `ls` para verificar o resultado de cada comando.

Perceba que tanto o _zip_ quanto o _unzip_ são comandos muito verborrágicos, ou seja, imprimem muita informação. O modificador `-q` permite que o retorno seja vazio (apesar de o resto funcionar perfeitamente):

```css
unzip -q work.zip
```

E para _zip_:

```python
zip -rq work.zip workspace
```

Podemos deixar juntos o `-q` e o comando de recursividade `-r` formando o `-rq`.

Nesta aula aprendemos os comandos para compactar e descompactar arquivos, além de esconder as informações que eles retornam, com o comando `-q`.

# usando o método TAR

Aprendemos a compactar arquivos e diretórios utilizando a extensão _zip_, com o comando `zip`, que é uma extensão muito famosa no sistema operacional Windows. No Linux, uma outra extensão é mais convencional de se utilizar, a extensão **_tar_**. Vamos, então, fazer o mesmo trabalho da aula passada mas utilizando o comando `tar`. Para compactar o diretório _workspace_ fazemos:

```undefined
tar -cz workspace > work.tar.gz
```

O `tar` sozinho não serve para compactar arquivos. Na verdade o `tar` serve para empacotar vários diretórios e arquivos em um único arquivo, facilitando a transferência. Para compactar usaremos o `tar` combinado com o `zip`, o primeiro empacota e o segundo compacta.

O modificador `-cz` indica que o arquivo _tar_ será criado (`-c`) e será compactado pelo _zip_(`-z`) usando o redirecionamento `>`. Uma observação interessante é que comando `tar` já é automaticamente recursivo.

> Lembre-se de utilizar o comando `ls` para verificar o arquivo criado e de remover o diretório `workspace` antes de descompactar os arquivos com o comando `rm`.

Para descompactar o arquivo `.tar.gz` que criamos, fazemos:

```undefined
tar -xz < work.tar.gz
```

Perceba que houveram apenas duas diferenças em relação ao comando de compactação, a presença `-x` de "_extract_", para extrair os arquivos e a direção do redirecionamento `<` que agora em vez de indicar saída de dados, indica entrada de dados.

Mas não é muito bom ficarmos o tempo todo trabalhando com redirecionamento, é meio chato. Para isso o comando `tar` possui o modificador `-f` para podermos passar o nome do arquivo que queremos criar:

```undefined
tar -czf work.tar.gz workspace/
```

Note que inversão no nome do arquivo e diretório a ser compactado, com redirecionamento, o nome do arquivo final vem depois, agora ele está vindo antes. Agora para descompactar fazemos:

```undefined
tar -xzf work.tar.gz
```

Uma outra característica que faz o comando `tar` diferente do `zip` é que ele não é verborrágico por padrão. Consequentemente não precisamos dar comandos para que as informações de compactação não apareçam. Pelo contrário, para que as informações apareçam, usamos o modificador `-v` (de "_verbose_"):

```undefined
tar -vxzf work.tar.gz
```

A saída será semelhante a mostrada abaixo:

```bash
workspace/
workspace/bemvindo2.txt
workspace/projetos-php/
workspace/projetos-java/
workspace/projetos-java/bemvindo.txt
workspace/bemvindo.txt
workspace/projetos-c#/
workspace/projetos-c#/bemvindo.txt
```

Existem muitos modificadores para compactar e descompactar diretórios, tanto em `zip` quanto em `tar`. Por isso podemos recorrer sempre que necessário à documentação usando o comando `man`. Como por exemplo: `man tar` para sabermos sobre outras opções de modificadores disponíveis para o comando `tar`.

>[!tip] 
>
>O parâmetro `-c` indica ao comando `tar` que desejamos criar um novo arquivo.
>
O comando `tar` apenas empacota vários arquivos em um único arquivo, sem realizar compactação, e por isso passamos o parâmetro `-z` para indicar que queremos, além de criar um único arquivo, realizar um processo de compactação utilizando o formato `.gz`. Quando compactamos podemos reduzir o tamanho.
O parâmetro `-f` indica que compactaremos para um arquivo.

---

Vimos que o comando `tar` não compacta, apenas empacota os arquivos. E que podemos utilizá-lo em conjunto com outros compactadores. Vimos como compactar no formato `.gz`, que é o formato gerado pelo compactador `gzip`.

Um outro formato de compactação que podemos utilizar junto com o `tar` é o formato `.bzip2`. Esse formato é mais eficiente na compactação, conseguindo criar arquivos menores. Porém o tempo que o `.bzip2` leva para criar o arquivo compactado é maior do que o tempo do `gzip`.

Para criar um arquivo `.tar` compactado com o `bzip2`, substituímos o `-z` (de `gzip`) por um `-j`. O formato que utilizamos é o `.tar.bz2`.

Aproveite e faça um teste, compactando seu diretório `workspace`:

```ruby
$ tar -cjf work.tar.bz2 workspace/
```

Você pode obter mais [informações sobre o `bzip2` na página do projeto](http://www.bzip.org/). Existe também um [artigo na Wikipédia sobre o `bzip2`](https://pt.wikipedia.org/wiki/Bzip2).