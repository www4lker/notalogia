---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/compartilhando-o-trabalho/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# compartilhando
## parte dois de seis da série sobre git

-   Criamos um repositório remoto usando o comando git init --bare em uma pasta chamada "oquequiser". Note que poder ser uma pastra online ou local.
-   Adicionamos o caminho do repositório remoto ao repositório local usando o comando git remote add, dando-lhe um nome, como "local".
-   Verificamos se o repositório remoto foi adicionado corretamente usando o comando git remote -v.
-   Clonamos o repositório remoto em outro local usando o comando git clone seguido do caminho do repositório remoto.
-   É possível renomear a pasta clonada usando o comando git clone seguido do caminho do repositório remoto e o nome desejado da pasta.
-   Para enviar nossas alterações para o repositório remoto, usamos o comando git push, especificando o nome do repositório remoto e o branch que desejamos enviar.
-   Para buscar as alterações feitas em um repositório remoto, usamos o comando git fetch, que busca as alterações do repositório remoto para o repositório local, mas não as mescla com o código atual. Podemos mesclar as alterações buscadas usando o comando git merge ou git pull.

