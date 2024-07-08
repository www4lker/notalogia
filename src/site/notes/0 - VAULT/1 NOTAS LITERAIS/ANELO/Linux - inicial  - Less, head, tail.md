---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/linux-inicial-less-head-tail/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# Linux - inicial  - Less, head, tail

## criado em: 
-  03-08-2023 - 09:55

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Linux - inicial\|Linux - inicial]]
- tags: #ANELO 
- Fontes & Links: 

---

## Transcrição

Continuando nossos estudos sobre manipulação de arquivos, vamos primeiramente, criar um da maneira visual, por meio do navegador de pastas um arquivo de texto chamado `google.txt` dentro do diretório `workspace`:

![](https://s3.amazonaws.com/caelum-online-public/ubuntu/Ubuntu1_cp8_1.png)

Vamos adicionar conteúdo nesse arquivo. Para isso entremos no site da [Wikipedia](https://en.wikipedia.org) na página que fala sobre o [Google](https://en.wikipedia.org/wiki/Google) e vamos copiar uma parte considerável do texto para o arquivo.

No terminal, sabemos que podemos utilizar o comando `cat` para ler o arquivo criado, ele nos retornará todo o texto:

```bash
cat google.txt
```

Porém é muito texto. Se quisermos ler apenas o começo do arquivo, usamos o comando `head`. Ele retorna apenas as dez primeiras linhas do arquivo:

```bash
head google.txt
```

Para especificarmos a quantidade de linhas que queremos retornar, podemos usar a opção `-n` informando o número de linha queremos:

```bash
head -n 3 google.txt
```

Dessa maneira o Terminal retorna apenas as três primeiras linhas do começo do arquivo. O inverso também é possível, ler as últimas linhas do arquivo. Para lermos as últimas linhas usamos o comando `tail`:

```bash
tail google.txt
```

O `tail` por padrão retorna as dez últimas linhas, assim como o `head`, para alterar esse limite, podemos usar o `-n` assim como fizemos no comando anterior:

```bash
tail -n 3 google.txt
```

Além do `head` e do `tail`, ainda temos o comando `less`, que nos permite abrir e navegar pelo texto do arquivo no Terminal utilizando as setas para cima e para baixo do teclado:

```undefined
less google.txt
```

E podemos fechar o arquivo utilizando a tecla `q` do teclado.