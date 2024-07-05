---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/reset-css-bonus/","tags":["css","chatgpt","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# reset CSS - bonus

## criado em: 
-  30-03-2023 - 14:52

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/reset CSS - o que é\|reset CSS - o que é]]
- tags: #css #chatgpt #ANELO 

---

## Reset CSS: o que é e como usar em seu projeto web

Ao desenvolver um site, é comum que os navegadores apresentem diferentes comportamentos na apresentação dos elementos, como a altura da linha padrão ou as medidas para o margin superior e inferior em títulos. Essas inconsistências podem afetar profundamente a aparência e o layout do site, tornando difícil para os desenvolvedores garantir uma experiência consistente em todos os navegadores.

Para solucionar esse problema, os desenvolvedores Front-end criaram a técnica de reset CSS, que consiste em definir valores genéricos para as propriedades de todas as tags HTML, como margin, padding e border. Essa técnica tem como objetivo suavizar as diferenças entre os navegadores e padronizar a estilização, sobrepondo a formatação original dos browsers com uma folha de estilo.

Um dos primeiros a levantar a discussão sobre as inconsistências dos navegadores foi Eric Meyer, em 2007, que desenvolveu um arquivo de reset CSS que se tornou muito popular entre os desenvolvedores. Em seu código, ele divide as tags em grupos que recebem valores genéricos e outros que precisam de valores mais específicos. O arquivo de Eric Meyer pode ser encontrado em seu blog, onde ele explica um pouco sobre a técnica e como desenvolveu o seu código reset.

No entanto, também é possível criar um arquivo de reset CSS personalizado para atender às necessidades do seu projeto. Há várias formas de fazer isso, incluindo a utilização de seletores universais que definem valores para todas as tags HTML, como margin e padding.

Embora a técnica de reset CSS tenha muitas vantagens, também apresenta alguns desafios e problemas que os desenvolvedores devem estar cientes. Por exemplo, pode levar algum tempo para entender os efeitos de cada propriedade e decidir quais devem ser mantidas ou modificadas. Além disso, é possível que o reset CSS remova estilos necessários para o funcionamento de um plugin ou componente do site, o que pode causar problemas.

Uma alternativa ao reset CSS é a técnica Normalize CSS, que tem como objetivo deixar consistente a estilização padrão entre os navegadores, mantendo alguns padrões úteis e corrigindo bugs comuns nas estilizações padrões. O código do Normalize CSS é modular e possui uma documentação detalhada sobre as modificações.

Em resumo, a técnica de reset CSS é uma forma eficaz de padronizar a estilização de elementos em diferentes navegadores, mas os desenvolvedores devem estar cientes dos desafios e problemas que podem surgir ao usá-la. A utilização de um arquivo de reset CSS personalizado ou a técnica Normalize CSS podem ser alternativas interessantes para garantir uma experiência consistente em todos os navegadores.