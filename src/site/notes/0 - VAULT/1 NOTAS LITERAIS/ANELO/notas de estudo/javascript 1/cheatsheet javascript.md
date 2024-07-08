---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/notas-de-estudo/javascript-1/cheatsheet-javascript/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# cheatsheet javascript

## criado em: 
-  23-03-2023 - 16:49

### Conteúdo Relacionado
- notas: 
- tags: 
- Fontes & Links: 

---


# Cheat Sheet: JavaScript para iniciantes

## **Cheat Sheet: JavaScript para iniciantes**

### **Termos importantes:**

1. Variáveis: Armazenam valores que podem ser alterados e usados ao longo do código.
2. Constantes: Armazenam valores que não podem ser alterados.
3. Funções: Blocos de código que podem ser chamados e executados para realizar uma tarefa específica.
4. Parâmetros: Valores passados para uma função quando ela é chamada.
5. Condicionais: Instruções `if`, `else if` e `else` que permitem executar blocos de código com base em condições específicas.
6. Laços de repetição: Instruções `for`, `while` e `do-while` que permitem executar blocos de código várias vezes.
7. Arrays: Estrutura de dados que armazena uma lista de valores.
8. Objetos: Estrutura de dados que armazena informações em pares de chave-valor.
9. Eventos: Ações que ocorrem no navegador, como cliques, movimentos do mouse, etc.
10. DOM (Document Object Model): Representação dos elementos de uma página da web como objetos, que podem ser manipulados usando JavaScript.

**Funções importantes:**

1. `console.log()`: Exibe mensagens no console do navegador.
2. `alert()`: Mostra uma caixa de diálogo com uma mensagem.
3. `prompt()`: Mostra uma caixa de diálogo solicitando uma entrada do usuário.
4. `parseInt()`: Converte uma string em um número inteiro.
5. `parseFloat()`: Converte uma string em um número decimal.
6. `isNaN()`: Verifica se um valor é NaN (Not a Number).
7. `typeof()`: Retorna o tipo de dado de um valor.
8. `Math.random()`: Retorna um número aleatório entre 0 (inclusive) e 1 (exclusive).
9. `Math.floor()`: Arredonda um número para baixo para o número inteiro mais próximo.
10. `Math.ceil()`: Arredonda um número para cima para o número inteiro mais próximo.
11. `Math.round()`: Arredonda um número para o número inteiro mais próximo.
12. `Array.isArray()`: Verifica se um valor é um array.
13. `Array.push()`: Adiciona um elemento ao final de um array.
14. `Array.pop()`: Remove o último elemento de um array.
15. `Array.shift()`: Remove o primeiro elemento de um array.
16. `Array.unshift()`: Adiciona um elemento ao início de um array.
17. `Array.splice()`: Adiciona e/ou remove elementos de um array.
18. `Array.slice()`: Retorna uma cópia de uma parte de um array.
19. `Array.map()`: Cria um novo array com os resultados de chamar uma função para cada elemento do array original.
20. `Array.filter()`: Cria um novo array com todos os elementos que passam em um teste implementado por uma função fornecida.
21. `Array.reduce()`: Reduz um array a um único valor, aplicando uma função acumuladora que é fornecida.
22. `Array.find()`: Retorna o primeiro elemento em um array que satisfaz uma condição especificada.
23. `Array.findIndex()`: Retorna o índice do primeiro elemento em um array que satisfaz uma condição especificada.
24. `Array.includes()`: Verifica se um array contém um determinado elemento.
25. `Array.join()`: Junta todos os elementos de um array em uma única string.
26. `Array.reverse()`: Inverte a ordem dos elementos de um array.
27. `Array.sort()`: Ordena os elementos de um array.
28. `String.length`: Retorna o número de caracteres em uma string.
29. `String.charAt()`: Retorna o caractere em um determinado índice de uma string.
30. `String.concat()`: Combina duas ou mais strings.
31. `String.indexOf()`: Retorna a posição da primeira ocorrência de uma string em outra string.
32. `String.lastIndexOf()`: Retorna a posição da última ocorrência de uma string em outra string.
33. `String.replace()`: Substitui uma parte de uma string por outra.
34. `String.slice()`: Retorna uma parte de uma string.
35. `String.split()`: Divide uma string em um array de substrings.
36. `String.trim()`: Remove espaços em branco do início e do fim de uma string.
37. `Object.keys()`: Retorna um array contendo as chaves de um objeto.
38. `Object.values()`: Retorna um array contendo os valores de um objeto.
39. `Object.entries()`: Retorna um array contendo pares de chave-valor de um objeto.
40. `Object.assign()`: Copia propriedades de um objeto para outro objeto.
41. `JSON.parse()`: Converte uma string JSON em um objeto JavaScript.
42. `JSON.stringify()`: Converte um objeto JavaScript em uma string JSON.
43. `setTimeout()`: Executa uma função após um determinado tempo (em milissegundos).
44. `setInterval()`: Executa uma função repetidamente a cada intervalo de tempo (em milissegundos).
45. `clearTimeout()`: Cancela um temporizador definido com `setTimeout()`.
46. `clearInterval()`: Cancela um temporizador definido com `setInterval()`.

### **Exemplos de sintaxe:**

1. Variáveis e constantes:

```javascript
let variavel = "valor";
const CONSTANTE = "valor constante";
```

2. Funções:

```javascript
function nomeDaFuncao(parametro1, parametro2) {
  // Código da função
}
```

3. Condicionais:

```javascript
if (condicao) {
  // Código se a condição for verdadeira
} else if (outraCondicao) {
  // Código se a outra condição for verdadeira
} else {
  // Código se nenhuma das condições for verdadeira
}
```

4. Laços de repetição:

```javascript
for (let i = 0; i < 10; i++) {
  // Código a ser repetido
}

while (condicao) {
  // Código a ser repetido
}

do {
  // Código a ser repetido
} while (condicao);
```

5. Arrays:

```javascript
let array = ["elemento1", "elemento2", "elemento3"];
```

6. Objetos:

```javascript
let objeto = {
  chave1: "valor1",
  chave2: "valor2",
  chave3: "valor3"
};
```

7. Eventos:

```javascript
elemento.addEventListener("tipoDoEvento", function(event) {
  // Código a ser executado quando o evento ocorrer
});
```

8. Manipulação do DOM:

```javascript
let elemento = document.getElementById("idDoElemento");
elemento.innerHTML = "Novo conteúdo";
elemento.style.color = "red";
elemento.classList.add("classeCSS");
elemento.classList.remove("outraClasseCSS");
elemento.setAttribute("atributo", "valor");
elemento.removeAttribute("atributo");
```

## Bônus

O básico está coberto! No entanto, aqui estão mais alguns conceitos e funções úteis que você pode explorar à medida que avança no aprendizado do JavaScript:

1. Operadores de comparação: `==`, `===`, `!=`, `!==`, `<`, `>`, `<=`, `>=`
2. Operadores lógicos: `&&` (AND), `||` (OR), `!` (NOT)
3. Operadores de atribuição: `=`, `+=`, `-=`, `*=`, `/=`, `%=`
4. Operador ternário:

```javascript
condicao ? valorSeVerdadeiro : valorSeFalso;
```

5. Funções anônimas e arrow functions:

```javascript
const funcaoAnonima = function(parametro) {
  // Código da função
};

const arrowFunction = (parametro) => {
  // Código da função
};
```

6. Template literals:

```javascript
let nome = "João";
let saudacao = `Olá, ${nome}!`;
```

7. Destructuring assignment:

```javascript
let [a, b, c] = [1, 2, 3]; // Arrays
let { chave1, chave2 } = objeto; // Objetos
```

8. Funções de alta ordem e closures:

```javascript
function funcaoDeAltaOrdem(callback) {
  // Código que usa a função callback
}

function closure() {
  let variavelPrivada = "valor";
  return function() {
    // Código que pode acessar a variávelPrivada
  };
}
```

9. Promises e async/await:

```javascript
const promise = new Promise((resolve, reject) => {
  // Código que pode chamar resolve(valor) ou reject(erro)
});

promise
  .then((valor) => {
    // Código a ser executado quando a promise for resolvida
  })
  .catch((erro) => {
    // Código a ser executado quando a promise for rejeitada
  });

async function funcaoAssincrona() {
  try {
    let valor = await promise;
    // Código a ser executado quando a promise for resolvida
  } catch (erro) {
    // Código a ser executado quando a promise for rejeitada
  }
}
```

10. Módulos:

```javascript
// Exportando funções ou valores de um arquivo (module.js)
export function funcaoExportada() {
  // Código da função
}
export const valorExportado = "valor";

// Importando funções ou valores de outro arquivo (main.js)
import { funcaoExportada, valorExportado } from "./module.js";
```

Esses conceitos e funções adicionais são úteis para aprofundar seu conhecimento em JavaScript e desenvolver habilidades mais avançadas de programação.