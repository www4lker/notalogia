---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/gatsby-jardim-digital-avancado/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# gatsby jardim digital av

## criado em: 
-  11-04-2023 - 18:05

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/gatsby jardim digital basico\|gatsby jardim digital basico]]
- tags: #ANELO 
- Fontes & Links: 

---

eu estou me inspirando nesse jardim digital com os seguintes features: A set of packages to create a digital garden with Gatsby. gatsby-remark-double-brackets-link: Transform [[page\|page]] into a proper link. gatsby-remark-double-parenthesis-link: Transform ((page)) into a proper link. react-stacked-pages-hook: Manage a stack of pages in Gatsby. gatsby-transformer-markdown-references: Extract references between markdown nodes.

Entendi! Vou te ajudar a integrar esses recursos em seu projeto. Primeiro, instale os pacotes necessários:

``bash


`npm install gatsby-remark-double-brackets-link gatsby-remark-double-parenthesis-link react-stacked-pages-hook gatsby-transformer-markdown-references`

Agora, siga estas etapas para configurar e usar os recursos no seu projeto:

1.  Atualize o arquivo `gatsby-config.js` para incluir os plugins:

javascript

``// ... {   resolve: `gatsby-transformer-remark`,   options: {     plugins: [       `gatsby-remark-double-brackets-link`,       `gatsby-remark-double-parenthesis-link`,     ],   }, }, `gatsby-transformer-markdown-references`, // ...``

2.  Crie um componente que utilizará o `react-stacked-pages-hook`. Vamos chamá-lo de `StackedPages`:

javascript

`// src/components/StackedPages.js import React from "react"; import { useStackedPages } from "react-stacked-pages-hook"; import { Link } from "gatsby";  const StackedPages = ({ location }) => {   const [stackedPages, stackedPagesRef] = useStackedPages({     location,     threshold: 0.2,   });    return (     <div ref={stackedPagesRef}>       {stackedPages.map((page) => (         <div key={page.id}>           <Link to={page.slug}>{page.title}</Link>           <div dangerouslySetInnerHTML={{ __html: page.html }} />         </div>       ))}     </div>   ); };  export default StackedPages;`

3.  Atualize o componente `Sidebar` para incluir o componente `StackedPages`. Substitua a seção `<main>{children}</main>` em `src/components/layout.js`:

javascript

`// ... import StackedPages from "./StackedPages"; // ... <main>   <StackedPages location={location} /> </main> // ...`

Para usar o `StackedPages`, você precisa passar a propriedade `location` para o componente `Layout` e, em seguida, passá-la para o componente `StackedPages`. Atualize o componente `Layout`:

javascript

`const Layout = ({ children, location }) => {   // ...   return (     // ...     <StackedPages location={location} />     // ...   ); };`

E passe a propriedade `location` no componente `Layout` em suas páginas, como `src/pages/index.js`:

javascript

`import Layout from "../components/layout";  const IndexPage = ({ location }) => (   <Layout location={location}>     {/* ... */}   </Layout> );`

Com essas etapas, você deve ter uma configuração básica para o seu jardim digital com suporte a links de colchetes duplos, links de parênteses duplos e empilhamento de páginas. Adapte e personalize ainda mais o projeto de acordo com suas necessidades e preferências.