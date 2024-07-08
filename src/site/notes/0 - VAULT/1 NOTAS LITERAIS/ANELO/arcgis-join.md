---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/arcgis-join/","tags":["geo","geo-processo","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# arcgis-join

## criado em: 
- 30-11-2023
- 09:00
## relacionados:
- [[0 - VAULT/1 NOTAS LITERAIS/PSICOGEOGRAFIA/DISCIPLINA DE GEOPROCESSAMENTO\|DISCIPLINA DE GEOPROCESSAMENTO]]
- [[0 - VAULT/1 NOTAS LITERAIS/Interesses de Pesquisa/cartografia social\|cartografia social]]
- [[0 - VAULT/1 NOTAS LITERAIS/888/GEOPROCESSAMENTO - COM CRIS E EDU\|0 - VAULT/1 NOTAS LITERAIS/888/GEOPROCESSAMENTO - COM CRIS E EDU]]
- tags: #geo #geo-processo #ANELO
- Fontes & Links: 
---


Mapas socioeconômicos a partir de ligação de atributos a um shapefile - ArcMap 10.3

### Utilizando ferramentas do arquivo X para associar dados 
 O professor Daniel Magalhães mostrou como pode-se utilizar as ferramentas do arquivo X para associar dados de uma tabela excel na tabela xls com o shape file do arc gis, permitindo assim a junção da informação no arquivo que diz respeito aos setores censitários do IBGE 
### Convertendo código do excel para texto 
 Para evitar problemas na junção da tabela a partir do código com o sheik fire do arc gis, o professor mostrou a utilização do Excel para converter os números para texto. 
 ### Marcação de níveis e salvamento de arquivo 
 No vídeo, o autor ensina a marcação e transferência de números em células específicas do Excel para que sejam exibidos como texto. Ele também ensina como salvar o arquivo no formato Excel 97-2003 (xls) para que seja compatível com outras ferramentas de análise de dados. 
### Adicionando setores censitários 
 O autor adiciona uma tabela de dados com informações sobre os setores censitários dos bairros São Bernardo e Belo Horizonte. Em seguida, ele explica que os setores censitários são unidades territoriais que apresentam homogeneidade socioeconômica e ensina os procedimentos para visualizar e associar códigos únicos de identificação para os polígonos vizinhos. 
### Passo a passo para unir informações em uma planilha 
 Os passos para unir as informações em uma planilha para o setor censitário foram descritos detalhadamente. Primeiro, é necessário escolher as variáveis de um a doze e selecionar o setor censitário com o botão direito do mouse. Em seguida, escolher a opção juntar e selecionar o campo a ser utilizado para fazer a junção, que será o código. Depois, é preciso escolher qual planilha a ser utilizada e qual campo utilizado para fazer o juntar. Em seguida, gerar um arquivo permanente do shape file para não perder a junção. Por fim, exportar os dados para gerar uma cópia e salvar na pasta shape file em bg formato. O processo não deve ser interrompido, e a cópia gerada deve ser adicionada ao mapa. 
### Variáveis para simbolizar na planilha básica 
 Ao trabalhar com a planilha básica, uma informação importante a ser considerada é a variável 3, que informa a média do número de moradores e a variável 5, que informa o valor médio do rendimento das pessoas responsáveis por domicílios. Para simbolizar essas variáveis na planilha, pode-se utilizar a aba de simbologia e selecionar o método quantitativo, já que são valores quantitativos. O sistema reconhece o menor e maior valor e faz a divisão dos dados em cinco classes pelo método brics. Dá-se a opção de escolher as cores e aplicá-las aos valores de maior e menor renda. É importante lembrar que existem várias opções de simbolização para esses dados e pode-se utilizar a classe finn para excluir valores com zero de renda. 
### Áreas sem moradores 
 O mapa de renda pode ser ajustado para excluir áreas sem moradores, como a lagoa da Pampulha e a UFMT, para garantir que os resultados não sejam distorcidos. Além disso, é possível definir intervalos de classe para os salários mínimos e escolher as classes da forma como o pesquisador achar melhor. É também importante observar as variáveis da planilha domiciliar e selecionar a variável correta para avaliar o abastecimento de água por setor censitário. 
### Normalização dos dados da copasa 
 A normalização dos dados feita pela variável 2 que contém o total de domicílios e a variável 12 que contém informações da copasa. O resultado da normalização é dado em porcentagem onde 0,9 significa 90% e 1 significa 100%. O mapa é colorido de acordo com a situação da porcentagem, onde verde significa uma boa situação e vermelho uma ruim. Esses dados foram criados especificamente para Belo Horizonte, com possíveis áreas com apenas 3%. Para resolver esse problema, é necessário recortar o dado para São Bernardo, onde dessa forma, conseguimos simbolizar a variável 12 e avaliar a situação para ver onde ela é melhor e onde é pior. 

 ---

 No QGIS (anteriormente conhecido como Quantum GIS), você também pode realizar operações semelhantes de "Join" e "Relate" para combinar dados de diferentes camadas. Vou explicar como fazer isso no QGIS:

**Join**:

Para realizar um "Join" no QGIS, siga os passos abaixo:

**Passo 1**: Abra o QGIS.

**Passo 2**: Adicione as camadas que contêm as informações que você deseja combinar ao projeto. Você pode fazer isso indo para "Camada" > "Adicionar Camada" ou simplesmente arrastando os arquivos de camada para a janela de visualização.

**Passo 3**: Certifique-se de que as camadas que você deseja combinar possuam um campo em comum (por exemplo, um ID ou um nome) que será usado como chave de junção.

**Passo 4**: Clique com o botão direito na camada da qual você deseja adicionar informações (a camada de destino) e selecione "Propriedades".

**Passo 5**: Na janela de propriedades da camada, vá para a seção "Joins" (ou "Junção" em algumas versões).

**Passo 6**: Clique no botão "+" para adicionar um novo "Join".

**Passo 7**: Escolha a camada de origem (a camada que contém os dados a serem adicionados) e o campo em comum.

**Passo 8**: Escolha o campo de destino na camada de destino.

**Passo 9**: Escolha como deseja tratar os registros sem correspondência (por exemplo, manter todos os registros ou apenas os correspondentes).

**Passo 10**: Clique em "OK" para concluir o "Join".

Agora, as informações da camada de origem estão vinculadas à camada de destino com base no campo comum.

**Relate**:

Para criar um relacionamento entre duas camadas no QGIS e visualizar informações em uma tabela de resumo, siga estes passos:

**Passo 1**: Adicione as camadas ao projeto, como mencionado anteriormente.

**Passo 2**: Certifique-se de que as camadas possuam um campo em comum que será usado como chave de relacionamento.

**Passo 3**: Clique com o botão direito na camada de destino (a camada da qual você deseja ver informações) e vá para "Propriedades".

**Passo 4**: Na janela de propriedades da camada, vá para a seção "Relacionamentos".

**Passo 5**: Clique no botão "+" para adicionar um novo relacionamento.

**Passo 6**: Escolha a camada relacionada (a camada com informações que você deseja visualizar) e o campo em comum.

**Passo 7**: Escolha o tipo de relacionamento (geralmente "1 para 1" ou "1 para muitos", dependendo da sua necessidade).

**Passo 8**: Clique em "OK" para criar o relacionamento.

Agora, você pode selecionar um objeto na camada de destino e ver as informações relacionadas na tabela de resumo da camada relacionada.

Esses são os passos para realizar "Join" e "Relate" no QGIS. Lembre-se de que a interface do usuário pode variar um pouco dependendo da versão específica do QGIS que você está usando, mas a lógica geral é a mesma.