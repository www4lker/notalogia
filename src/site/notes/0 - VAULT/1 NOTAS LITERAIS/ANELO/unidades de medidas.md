---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/unidades-de-medidas/","tags":["css","HTML","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# unidades de medidas

## criado em: 
-  03-04-2023 - 14:31

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/HTML e CSS 4\|HTML e CSS 4]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/adaptando elementos\|adaptando elementos]]
- tags: #css #HTML #ANELO 
- Fontes & Links: 

---
## Nessa aula, você aprendeu:

-   Sobre medidas relativas e absolutas;
-   Utilizar a documentação sobre unidade de medidas;
-   Utilizar a unidade de medida REM;
-   Alterar a aparência do navegador em configurações.


---

**Guilherme:** Olá! Meu nome é **Guilherme Lima**.

**Rafaela:** Olá! Eu sou a **Rafaela Ballerine**.

**Guilherme:** E vamos nos aprofundar em HTML e CSS e continuar o desenvolvimento do nosso projeto.

**Rafaela:** Agora não o teremos apenas no nosso computador, mas também conseguiremos acessá-lo de qualquer computador. Portanto conseguiremos compartilhá-lo com nossos amigos e nossa família, que poderão acessar não apenas do desktop e notebook.

**Guilherme:** Mas também do celular.

E para isso aprenderemos a trabalhar com unidades de medidas diferentes, criaremos um repositório e uma conta no GitHub.

**Rafaela:** Também vamos fazer testes com o design da página, movimentando a imagem dependendo do tamanho da tela.

**Guilherme:** Construiremos um projeto incrível juntos.

E para que este projeto seja preparado, nosso **objetivo** é trabalhar com **responsividade**.Vocês perceberão que não basta diminuir e aumentar o tamanho e os posicionamentos, precisamos pensar em como esses elementos ficarão disponíveis na tela.

---

**Guilherme:** Vamos iniciar nossos estudos de HTML e CSS mergulhando mais profundamente no tema. Agora estudaremos **Unidades de medida**.

**Rafaela:** Nós começamos a aprender sobre elas quando falamos sobre pixels e porcentagens, mas agora iremos realmente compreender o que é ideal para utilizar em cada situação, assim como conceitos novos.

**Guilherme:** Começando pelo primeiro ponto: nós definimos a maioria dos valores do nosso projeto utilizando a unidade de medida **pixel**, porém esses valores não são adaptáveis com as configurações do navegador da pessoa.

Vamos fazer esse exemplo, Rafa.

**Rafaela:** Vamos, lógico!

**Guilherme:** No canto direito da barra superior da janela do Chrome, após a barra de endereço, clica nos três pontos verticais. Em seguida, no menu, acessa "Configurações".

Somos direcionados para outra página, onde tem um menu de navegação na lateral esquerda. Nesse menu, vamos clicar em "Aparência". Com isso, no centro da tela aparecem algumas opções relacionadas à aparência do navegador.

Entre elas, temos a propriedade "Tamanho da fonte". Essa é uma propriedade que o navegador nos permite escolher. Ao abrirmos as opções, que ficam no canto direito dessa opção, notamos que podemos escolher entre: muito pequena, pequena, média (recomendado), grande e muito grande.

Rafa, conseguimos deixar nosso projeto e essa tela de configurações lado a lado?

**Rafaela:** Conseguimos! Eu vou abrir a página do nosso projeto, pressionar "Windows + ←" e, entre as opções que surgem para ocupar a metade direita da tela, vou clicar na janela de configurações.

**Guilherme:** Legal! O que eu quero fazer, Rafa, é alterar as configurações de aparência do navegador e quero que o projeto acompanhe essa alteração.

Então vamos mudar o tamanho da fonte para "muito grande".

**Rafaela:** Quando eu cliquei, mudou o tamanho da fonte do menu, mas no nosso projeto nada se alterou.

**Guilherme:** Isso é muito ruim, gente, porque não estamos com nosso projeto adaptável com as configurações da pessoa.

**Rafaela:** E isso é importante para muitas pessoas. Nós achamos que não, e tendemos a deixar com uma configuração padrão, mas para muitas pessoas conseguirem enxergar e clicar, até pelo _touch_ do celular. Portanto o tamanho da fonte é importante para acompanhar o que a pessoa quer.

**Guilherme:** Então vamos abrir a documentação, Rafa, para descobrir qual unidade de medida precisamos usar para acompanhar essas configurações.

**Rafaela:** Vamos. Vou procurar no Google por "_units in css_".

**Guilherme:** Se puder deixar a fonte maior para conseguirmos visualizar.

**Rafaela:** Ok! Vou expandir a janela e clicar no [**link do W3Schools**](https://www.w3schools.com/cssref/css_units.php).

**Guilherme:** Ele explica sobre as medidas com valores absolutos. Vamos mudar para o português para entendermos melhor.

Podemos perceber que existem dois grandes grupos de medidas. Temos as **absolutas**, que é um valor que determinamos e ele não muda, como centímetros (cm), milímetros (mm) e pixels (px). Também temos as medidas **relativas**, que aprenderemos mais agora.

Existem diversas **medidas relativas**: em, ex, ch, rem, vw, vh, vmin, vmx e % (porcentagem). Qual vamos utilizar nesse momento, Rafa? Tem como testarmos?

**Rafaela:** Tem como testarmos. O que você quer testar?

**Guilherme:** Vamos testar o H1 que estamos utilizando? Qual medida vamos mudar?

**Rafaela:** Acho que seria interessante testarmos com o **_rem_**, porque ele é uma medida relativa que vai usar o **_root-element_**, que é o elemento raiz, ou seja, a página HTML. É o que a pessoa que está utilizando a página definiu no navegador.

**Guilherme:** É justamente o que queremos.

**Rafaela:** Exatamente, então vou deixar novamente a tela dividida com a janela do nosso portfólio à esquerda e nossas preferências de aparência à direita. Em seguida, vou sobrepor a janela do VS Code sobre a do código, portanto também à direita. Depois voltamos para a página com a aparência.

Nesse código, vamos alterar o H1, que tem a classe `apresentacao__conteudo__titulo`. Portanto vamos abrir o arquivo `style.css` e acessar as configurações dessa classe, que começam na linha 55.

**Guilherme:** Na linha 56 está marcado o tamanho da fonte como 36px. Nós precisamos alterar para `rem`.

**Rafaela:** Exatamente. E falando sobre a transformação de medidas entre si, nós usamos uma escala para mudar de pixels para rem. Nessa escala utiliza-se o valor mais recomendado pelos navegadores, que é de 16, então 16px equivale a 1rem e 32px equivale a 2rem.

E para converter os 36px, nós dividimos esse valor por 16px. Ao dividirmos 36 por 16, temos como resultado 2,25. Então 36px equivale a 2,25rem.

Parece um número quebrado, mas até o 0,25 é válido usar. Caso fosse um número muito quebrado, como 2,1752, poderíamos arredondar, mas o 2,25 é um bom valor.

**Guilherme:** Então pegamos o valor da medida em pixel e dividimos pode 16 e temos o valor em rem.

**Rafaela:** Isso! Quanto mais usarem, mais vocês irão se acostumar com essa medida. Por exemplo, para 16px vocês já usarão 1rem e para 32px, vocês usarão 2.

**Guilherme:** Rafa, conseguimos visualizar nosso portifólio enquanto alteramos o código para observarmos o que acontece?

**Rafaela:** Vamos. A janela do portifólio à esquerda e a do VS Code à direita da tela e vou alterar a linha 56 para `font-size: 2.25rem;`.

```css
.apresentacao__conteudo__titulo {
    font-size: 2.25rem;
    font-family: var(--fonte-primaria);
}
```

Salvamos e nada se altera, porque não mudamos a configuração do nosso navegador. É para ele estar com a mesma medida, porque fizemos a conta.

Contudo, se abrirmos novamente a janela de aparências, à direita da tela, e alterarmos o tamanho da fonte para "Muito grande", reparamos, no nosso portifólio que está à esquerda, que o tamanho do título acompanha essa mudança.

**Guilherme:** Muito bom! Ficou a dica. Vamos mudar para o tamanho "Muito pequeno" para testarmos também.

**Rafaela:** Vamos. Quando eu mudo para "Muito pequeno" ele se altera e fica bem pequeno.

**Guilherme:** Nosso próximo desafio será configurar toda página para que ela fique com esse valor relativo.

**Rafaela:** Exato, mudar para o valor relativo em todas os elementos que queremos utilizar.

**Guilherme:** Isso!

---

**Guilherme:** Agora que entendemos que codando com `rem` nós acompanhamos a unidade de medida do navegador, vamos aplicar isso para os nossos próximos textos, porque acho isso importante.

**Rafaela:** Vou abrir o nosso arquivo `styles.css`, e em todos os lugares que tivermos `font-size` faremos o cálculo da medida de pixel para rem.

**Guilherme:** Nós podemos procurar com "**Ctrl + F**", que é o atalho para encontrar uma palavra rapidamente no navegador, e pesquisamos "font-size", que já encontraremos todos.

**Rafaela:** Boa ideia! Então quando procuramos, descobrimos que temos seis resultados.

O primeiro está no `.cabecalho__menu__link`. Nós temos 24px, e ao dividirmos por 16px temos 1.5rem.

```css
.cabecalho__menu__link {
    font-family: var(--font-secundaria);
    font-size: 1.5rem;
    font-weight: 600;
    color: var(--cor-terciaria);
    text-decoration: none;
}
```

Vamos salvar e vamos para o próximo, clicando na seta para baixo na barra de busca, que é o segundo ícone do lado direito. O seguinte é o título, que já tínhamos alterado. Clicando na seta para baixo novamente, temos o `.apresentacao__conteudo__texto`, com o valor de 24px novamente, ou seja, mudamos para 1.5rem.

```css
.apresentacao__conteudo__texto {
    font-size: 1.5rem;
    font-family: var(--font-secundaria);
}
```

O próximo é o `.apresentacao__links__subtitulo`, que também tem 24px:

```css
.apresentacao__links__subtitulo {
    font-family: var(--fonte-primaria)
    font-weight: 400;
    font-size:1.5rem;
}
```

Em seguida temos o `.apresentacao__links__link`, que é o botão com os links. Ele também tem o font-size de 24px, então mudamos para `1.5rem`. Por fim temos o rodapé, que também vamos mudar para `font-size: 1.5rem;`.

Feita essas alterações, podemos voltar para nossa página de portfólio no navegador e analisar como ficou, e se nossas mudanças fizeram sentido.

**Guilherme:** Inicialmente está igual, que é o que queríamos.

**Rafaela:** Isso. Então vamos fazer o teste se funcionou o que queríamos fazer. Vou deixar a página de portfólio ocupando apena a lateral esquerda e a página com as configurações de aparência na lateral direita.

**Guilherme:** Estamos usando o padrão recomendado no tamanho da fonte, que é o médio. Vamos deixar como "Muito grande", já exagerando mesmo no tamanho.

Quando mudamos percebemos que os textos da nossa página do portfólio se adaptam, então está tudo funcionando, certo, Rafa?

**Rafaela:** Sim, está tudo funcionando.

**Guilherme:** Vamos deixar um pouco menor, deixa apenas no "Grande". O texto já diminui. Se mudarmos para o "Médio" ele diminui mais um pouco.

**Rafaela:** E continua diminuindo quando optamos pelos tamanhos de fonte "Pequeno" e "Muito pequeno".