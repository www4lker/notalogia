---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/linux-inicial-touch/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# Linux - inicial- touch

## criado em: 
- 04-06-2024
- 18:47
## relacionados:
- notas:
1. 
- tags: #ANELO 
- Fontes & Links: 
---

[[Linux - inicial  - Less, head, tail \|Linux - inicial  - Less, head, tail ]]

Se entrarmos dentro do diretório `workspace` e observarmos os detalhes do arquivo `bemvindo.txt` com a ajuda do comando `ls -la` veremos a algo como seguinte saída para este arquivo:

```less
[...]
-rw-rw-r-- 1 user user 10 Jun 11 15:42 bemvindo.txt
[...]
```

Repare que a data da última atualização dele é de 11 de Junho às 15:42. Se quisermos apenas que essa data modifique-se para a data e hora atual, isto é, apenas encostar nesse arquivo sem modificá-lo, usamos o comando `touch`:

```bash
touch bemvindo.txt
```

Após isso, se verificarmos seus detalhes novamente com o comando `ls -la`, veremos que a data e hora de modificação foram alterados para as mais atuais:

```less
[...]
-rw-rw-r-- 1 user user 10 Jun 11 22:15 bemvindo.txt
[...]
```

O arquivo em si não altera-se, mas sua data de modificação sim. Para provar que realmente houve essa mudança, podemos ver o horário do sistema com o comando `date` e comparar com as informações do arquivo. A saída do comando `date` é semelhante a encontrada abaixo:

```yaml
Tue Jun 11 22:15:33 BRT 2013
```

De fato, acabamos de "modificar" o arquivo, **não seu conteúdo, mas sua data de última modificação**.# Linux - inicial- touch

## criado em: 
-  02-08-2023 - 11:20

### Conteúdo Relacionado
- notas: 
- tags: 
- Fontes & Links: 

---

# Para saber mais: obtendo ajuda e formatando datas

Já vimos que podemos obter ajuda na documentação do Linux, as man pages, através do comando `man`. Uma outra forma de obter ajuda sobre a utilização do comando, de uma forma mais resumida, é utilizando o parâmetro `--help` suportado por alguns comandos, ou utilizando o comando `help`.

O `help` é um comando interno do interpretador `bash`, que, quando executado sem parâmetros, retorna uma lista com todos os demais comandos internos do shell `bash`. Quando executado com parâmetro, o comando `help` retorna a sintaxe de utilização e uma descrição do comando interno que estamos interessados.

```shell
$ help pwd
$ date --help
```

Quando fazemos `date --help`, encontramos, dentre outras coisas, ajuda sobre como formatar a nossa data. Podemos imprimir, por exemplo, a data no formato `dia/mes/ano`:

```perl
$ date "+%d/%m/%Y"
23/01/2016
```

Aproveite para testar esses comandos no seu Linux!

Sempre que precisar consultar os parâmetros que um comando suporta, você pode pedir ajuda através do `help` ou `--help`.