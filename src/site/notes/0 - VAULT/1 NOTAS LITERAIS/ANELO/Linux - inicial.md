---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/linux-inicial/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# Linux - inicial

## criado em: 
-  02-08-2023 - 10:00

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Linux - inicial - ZIP\|Linux - inicial - ZIP]]
- tags: #ANELO 
- Fontes & Links: [alura Linux I - cnhecendo e utilizando o terminal](https://cursos.alura.com.br/course/linux-ubuntu/task/3253)
- 

---

Aprendemos a criar um diretório com o comando `mkdir`, mas como podemos apagar um diretório? E um arquivo? Removemos um diretório usando o comando `rmdir` e para remover um arquivo utilizamos o comando `rm`, dentro de `workspace` por exemplo podemos fazer:

```bash
rmdir projetos-java
rm arquivo3.txt
```

Removemos/Apagamos o diretório `projetos-java` e o arquivo `arquivo3.txt`. Uma observação interessante é que o comando para remover diretórios só irá funcionar para aqueles diretórios que estiverem vazios. Ele não apaga os arquivos dentro do diretório automaticamente.

Dentro do diretório `workspace` atualmente há três arquivos e um diretório _(use o comando ls para listar os arquivos)_:

```undefined
arquivo10.txt arquivo1.txt  arquivo2.txt  projetos-php
```

No `arquivo10.txt` temos a frase "Bem vindo" e nos outros dois a frase "meu primeiro teste". Para que o terminal imprima os textos de todos os arquivos com um determinado nome, por exemplo, "arquivo...txt" podemos faz:

```bash
cat arquivo?.txt
```

O resultado será:

```undefined
meu primeiro teste
meu primeiro teste
```

Também podemos usar o caractere `*`:

```bash
cat arquivo*.txt
```

Mas o resultado será um pouco diferente do primeiro caso:

```undefined
Bem vindo
meu primeiro teste
meu primeiro teste
```

Esses caracteres de `?` e `*` são utilizados para que sejam buscados mais de um arquivo que tenham o mesmo nome base, porém existe uma pequena diferença: O `?` só encontra os arquivos que tenham apenas UM caractere diferente do nome base, enquanto o `*` busca quaisquer números de caracteres.

Por isso que o arquivo `arquivo10.txt` é encontrado no segundo exemplo, mas não no primeiro. O `*` consegue lidar com o `10` depois do trecho `arquivo` no nome do arquivo, enquanto o `?` não consegue, pois são dois caracteres em `10`.

**Atenção**: se buscarmos o arquivo como `"*.txt"`, ou seja, com aspas, o terminal interpreta o asterisco como se o mesmo fosse parte do nome do arquivo:

```bash
cat "*.txt"
```

O comando acima nos trará uma mensagem de erro como a seguinte:

```yaml
cat: *.txt: No such file or diretory
```

Comentamos anteriormente que não podíamos apagar um diretório que possuía outros subdiretórios ou arquivos. Na verdade podemos, com o comando `rm -r` isto é possível. Ele remove **Recursivamente**, ou seja, apaga o diretório e tudo que está dentro dele. Podemos fazer por exemplo:

```bash
rm -r workspace/
```

Dessa forma apagamos todo o diretório `workspace` e tudo que havia dentro dele. Muito cuidado na hora de utilizar este comando para não apagar diretórios importantes.

---

Dentro do diretório `Desktop` do seu usuário, utilize o comando `echo` para criar o arquivo `musicas-favoritas.txt`, com a palavra "Paganini".

Execute o comando necessário para escrever a palavra "Bach" no arquivo `musicas-favoritas.txt` de forma que o conteúdo antigo do arquivo seja mantido.

Utilize o `cat` para verificar se o conteúdo do arquivo está correto.

">" Escreve
">>" concatena

### Caracteres coringa

Crie um novo arquivo dentro do diretório `workspace`:

```shell
$ echo "bem vindo" > arquivo10.txt
```

Execute o comando necessário para ler todos os arquivos que contenham apenas um caractere após o nome "arquivo" e antes da extensão ".txt".

Para ler os arquivos que possuem apenas um caracter após o nome "arquivo" e antes da extensão ".txt", fazemos:

```shell
$ cat arquivo?.txt
meu primeiro teste
meu primeiro teste
meu primeiro teste
```

O retorno do comando `cat` foi o conteúdo dos arquivo `arquivo1.txt`, `arquivo2.txt` e `arquivo3.txt`.

Para retornar os arquivos que possuem qualquer quantidade de caracteres após o nome "arquivo" e antes da extensão ".txt":

```shell
$ cat arquivo*.txt
bem vindo
meu primeiro teste
meu primeiro teste
meu primeiro teste
```

Nesse caso, o `cat` imprimiu o conteúdo de todos os arquivos presentes no nosso diretório. Alternativamente, poderíamos imprimir o conteúdo de todos os arquivos com extensão `.txt`, que, neste exemplo, teria o mesmo efeito do comando anterior:

```shell
$ cat *.txt
bem vindo
meu primeiro teste
meu primeiro teste
meu primeiro teste
```