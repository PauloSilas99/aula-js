# Principais Conceitos de JavaScript

## 1. Variáveis e Constantes

### var, let e const

```javascript
// var - escopo de função (não recomendado)
var nome = "João";

// let - escopo de bloco, pode ser reatribuída
let idade = 25;
idade = 26; // OK

// const - escopo de bloco, não pode ser reatribuída
const PI = 3.14159;
// PI = 3.14; // ERRO!
```

## 2. Tipos de Dados

### Tipos Primitivos

```javascript
// String
let texto = "Olá, mundo!";
let texto2 = 'JavaScript';

// Number
let numero = 42;
let decimal = 3.14;

// Boolean
let verdadeiro = true;
let falso = false;

// Undefined
let indefinido = undefined;

// Null
let nulo = null;

// Symbol (ES6)
let simbolo = Symbol('id');

// BigInt (ES2020)
let grande = 9007199254740991n;
```

### Tipos de Referência

```javascript
// Object
let pessoa = {
  nome: "Maria",
  idade: 30
};

// Array
let frutas = ["maçã", "banana", "laranja"];

// Function
function somar(a, b) {
  return a + b;
}
```

## 3. Operadores

### Aritméticos

```javascript
let a = 10;
let b = 3;

console.log(a + b); // 13 (adição)
console.log(a - b); // 7 (subtração)
console.log(a * b); // 30 (multiplicação)
console.log(a / b); // 3.333... (divisão)
console.log(a % b); // 1 (módulo/resto)
console.log(a ** b); // 1000 (exponenciação)
```

### Comparação

```javascript
console.log(5 == "5");  // true (igualdade solta)
console.log(5 === "5"); // false (igualdade estrita)
console.log(5 != "5");  // false
console.log(5 !== "5"); // true
console.log(5 > 3);     // true
console.log(5 < 3);     // false
console.log(5 >= 5);    // true
console.log(5 <= 3);    // false
```

### Lógicos

```javascript
console.log(true && false); // false (E)
console.log(true || false); // true (OU)
console.log(!true);         // false (NÃO)
```

## 4. Estruturas de Controle

### if/else

```javascript
let idade = 18;

if (idade >= 18) {
  console.log("Maior de idade");
} else {
  console.log("Menor de idade");
}

// Operador ternário
let status = idade >= 18 ? "Adulto" : "Menor";
```

### switch

```javascript
let dia = 3;
let nomeDia;

switch (dia) {
  case 1:
    nomeDia = "Domingo";
    break;
  case 2:
    nomeDia = "Segunda";
    break;
  case 3:
    nomeDia = "Terça";
    break;
  default:
    nomeDia = "Dia inválido";
}
```

### Loops

```javascript
// for
for (let i = 0; i < 5; i++) {
  console.log(i);
}

// while
let contador = 0;
while (contador < 5) {
  console.log(contador);
  contador++;
}

// do...while
let x = 0;
do {
  console.log(x);
  x++;
} while (x < 5);

// for...of (arrays)
let frutas = ["maçã", "banana", "laranja"];
for (let fruta of frutas) {
  console.log(fruta);
}

// for...in (objetos)
let pessoa = { nome: "João", idade: 30 };
for (let chave in pessoa) {
  console.log(chave + ": " + pessoa[chave]);
}
```

## 5. Funções

### Declaração de Função

```javascript
function somar(a, b) {
  return a + b;
}

console.log(somar(2, 3)); // 5
```

### Expressão de Função

```javascript
const multiplicar = function(a, b) {
  return a * b;
};

console.log(multiplicar(2, 3)); // 6
```

### Arrow Functions (ES6)

```javascript
// Forma curta
const dividir = (a, b) => a / b;

// Forma completa
const subtrair = (a, b) => {
  return a - b;
};

// Sem parâmetros
const saudacao = () => console.log("Olá!");

// Um parâmetro (sem parênteses)
const dobrar = x => x * 2;
```

### Parâmetros Padrão

```javascript
function saudar(nome = "Visitante") {
  console.log(`Olá, ${nome}!`);
}

saudar();        // "Olá, Visitante!"
saudar("Maria"); // "Olá, Maria!"
```

### Rest Parameters

```javascript
function somar(...numeros) {
  return numeros.reduce((acc, num) => acc + num, 0);
}

console.log(somar(1, 2, 3, 4)); // 10
```

## 6. Arrays

### Criação e Acesso

```javascript
let frutas = ["maçã", "banana", "laranja"];
console.log(frutas[0]); // "maçã"
console.log(frutas.length); // 3
```

### Métodos Importantes

```javascript
let numeros = [1, 2, 3, 4, 5];

// map - transforma cada elemento
let dobrados = numeros.map(n => n * 2);
// [2, 4, 6, 8, 10]

// filter - filtra elementos
let pares = numeros.filter(n => n % 2 === 0);
// [2, 4]

// reduce - reduz a um único valor
let soma = numeros.reduce((acc, n) => acc + n, 0);
// 15

// find - encontra primeiro elemento
let maiorQue3 = numeros.find(n => n > 3);
// 4

// forEach - itera sobre elementos
numeros.forEach(n => console.log(n));

// push/pop - adiciona/remove do final
numeros.push(6);
numeros.pop();

// shift/unshift - remove/adiciona do início
numeros.shift();
numeros.unshift(0);

// includes - verifica se contém
console.log(numeros.includes(3)); // true

// indexOf - encontra índice
console.log(numeros.indexOf(3)); // 2
```

## 7. Objetos

### Criação e Acesso

```javascript
let pessoa = {
  nome: "João",
  idade: 30,
  cidade: "São Paulo"
};

// Acesso por notação de ponto
console.log(pessoa.nome); // "João"

// Acesso por colchetes
console.log(pessoa["idade"]); // 30

// Adicionar propriedades
pessoa.email = "joao@email.com";

// Métodos
let calculadora = {
  somar: function(a, b) {
    return a + b;
  },
  // Forma curta (ES6)
  subtrair(a, b) {
    return a - b;
  }
};
```

### Destructuring

```javascript
let pessoa = { nome: "Maria", idade: 25, cidade: "Rio" };

// Destructuring de objeto
let { nome, idade } = pessoa;
console.log(nome); // "Maria"

// Com renomeação
let { nome: nomeCompleto } = pessoa;

// Destructuring de array
let [primeiro, segundo] = [1, 2, 3];
console.log(primeiro); // 1
```

### Spread Operator

```javascript
// Copiar array
let arr1 = [1, 2, 3];
let arr2 = [...arr1, 4, 5];
// [1, 2, 3, 4, 5]

// Copiar objeto
let obj1 = { a: 1, b: 2 };
let obj2 = { ...obj1, c: 3 };
// { a: 1, b: 2, c: 3 }

// Passar argumentos
function somar(a, b, c) {
  return a + b + c;
}
let numeros = [1, 2, 3];
console.log(somar(...numeros)); // 6
```

## 8. Template Literals

```javascript
let nome = "João";
let idade = 30;

// Interpolação
let mensagem = `Olá, meu nome é ${nome} e tenho ${idade} anos.`;

// Multilinha
let texto = `
  Linha 1
  Linha 2
  Linha 3
`;
```

## 9. Classes e POO

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    return `Olá, sou ${this.nome} e tenho ${this.idade} anos.`;
  }
}

class Estudante extends Pessoa {
  constructor(nome, idade, curso) {
    super(nome, idade);
    this.curso = curso;
  }

  estudar() {
    return `${this.nome} está estudando ${this.curso}.`;
  }
}

let aluno = new Estudante("Maria", 20, "JavaScript");
console.log(aluno.apresentar());
console.log(aluno.estudar());
```

## 10. Promises e Async/Await

### Promises

```javascript
function buscarDados() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve("Dados carregados!");
    }, 2000);
  });
}

buscarDados()
  .then(dados => console.log(dados))
  .catch(erro => console.error(erro));
```

### Async/Await

```javascript
async function carregarDados() {
  try {
    let dados = await buscarDados();
    console.log(dados);
  } catch (erro) {
    console.error(erro);
  }
}

carregarDados();
```

## 11. Callbacks

```javascript
function processarDados(dados, callback) {
  // Simula processamento
  setTimeout(() => {
    let resultado = dados.toUpperCase();
    callback(resultado);
  }, 1000);
}

processarDados("hello", (resultado) => {
  console.log(resultado); // "HELLO"
});
```

## 12. Closures

```javascript
function criarContador() {
  let contador = 0;
  
  return function() {
    contador++;
    return contador;
  };
}

let contador = criarContador();
console.log(contador()); // 1
console.log(contador()); // 2
console.log(contador()); // 3
```

## 13. Hoisting

```javascript
// Variáveis com var são "elevadas" (hoisted)
console.log(x); // undefined (não erro!)
var x = 5;

// let e const não são hoisted da mesma forma
// console.log(y); // ERRO!
let y = 10;

// Funções declaradas são hoisted
saudar(); // Funciona!
function saudar() {
  console.log("Olá!");
}
```

## 14. This

```javascript
// Em métodos de objeto
let pessoa = {
  nome: "João",
  saudar: function() {
    console.log(`Olá, sou ${this.nome}`);
  }
};

pessoa.saudar(); // "Olá, sou João"

// Arrow functions não têm seu próprio this
let pessoa2 = {
  nome: "Maria",
  saudar: () => {
    console.log(`Olá, sou ${this.nome}`); // this não é pessoa2
  }
};

// Bind, Call, Apply
let outraPessoa = { nome: "Pedro" };
pessoa.saudar.call(outraPessoa); // "Olá, sou Pedro"
```

## 15. Módulos (ES6)

### Exportar

```javascript
// modulo.js
export const PI = 3.14159;

export function somar(a, b) {
  return a + b;
}

export default class Calculadora {
  // ...
}
```

### Importar

```javascript
// main.js
import Calculadora, { PI, somar } from './modulo.js';

console.log(PI);
console.log(somar(2, 3));
let calc = new Calculadora();
```

## 16. Métodos Úteis de String

```javascript
let texto = "JavaScript é incrível";

console.log(texto.length);              // 23
console.log(texto.toUpperCase());       // "JAVASCRIPT É INCRÍVEL"
console.log(texto.toLowerCase());       // "javascript é incrível"
console.log(texto.includes("é"));       // true
console.log(texto.startsWith("Java"));  // true
console.log(texto.endsWith("incrível")); // true
console.log(texto.split(" "));          // ["JavaScript", "é", "incrível"]
console.log(texto.replace("incrível", "fantástico"));
```

## 17. JSON

```javascript
// Objeto para JSON
let pessoa = { nome: "João", idade: 30 };
let json = JSON.stringify(pessoa);
// '{"nome":"João","idade":30}'

// JSON para objeto
let objeto = JSON.parse(json);
// { nome: "João", idade: 30 }
```

## 18. Tratamento de Erros

```javascript
try {
  let resultado = 10 / 0;
  if (!isFinite(resultado)) {
    throw new Error("Divisão inválida");
  }
} catch (erro) {
  console.error("Erro:", erro.message);
} finally {
  console.log("Sempre executa");
}
```

## 19. Métodos Avançados de Array

```javascript
let numeros = [1, 2, 3, 4, 5];

// some - verifica se algum elemento passa no teste
console.log(numeros.some(n => n > 4)); // true

// every - verifica se todos passam no teste
console.log(numeros.every(n => n > 0)); // true

// slice - retorna parte do array
console.log(numeros.slice(1, 3)); // [2, 3]

// splice - modifica o array
let arr = [1, 2, 3, 4, 5];
arr.splice(2, 1, 99); // Remove 1 elemento no índice 2 e adiciona 99
// [1, 2, 99, 4, 5]

// sort
let letras = ["c", "a", "b"];
letras.sort(); // ["a", "b", "c"]

// reverse
numeros.reverse(); // [5, 4, 3, 2, 1]
```

## 20. Optional Chaining e Nullish Coalescing (ES2020)

```javascript
// Optional Chaining (?.)
let pessoa = {
  endereco: {
    rua: "Rua A"
  }
};

console.log(pessoa.endereco?.rua);     // "Rua A"
console.log(pessoa.contato?.telefone); // undefined (sem erro)

// Nullish Coalescing (??)
let nome = null;
let nomePadrao = nome ?? "Visitante"; // "Visitante"
// Diferente de || que também trata "" e 0 como falsy
```

## 21. Set e Map

```javascript
// Set - coleção de valores únicos
let conjunto = new Set([1, 2, 3, 3, 4]);
console.log(conjunto); // Set {1, 2, 3, 4}
conjunto.add(5);
conjunto.has(3); // true
conjunto.delete(2);

// Map - coleção de pares chave-valor
let mapa = new Map();
mapa.set("nome", "João");
mapa.set("idade", 30);
console.log(mapa.get("nome")); // "João"
mapa.has("idade"); // true
```

## 22. Event Loop e Assíncrono

```javascript
console.log("1");

setTimeout(() => {
  console.log("2");
}, 0);

Promise.resolve().then(() => {
  console.log("3");
});

console.log("4");

// Saída: 1, 4, 3, 2
// Explica a ordem de execução assíncrona
```

## Dicas Importantes

1. **Sempre use `const` por padrão**, `let` quando precisar reatribuir
2. **Evite `var`** - use `let` ou `const`
3. **Use `===` em vez de `==`** para comparações estritas
4. **Arrow functions** são mais concisas, mas cuidado com `this`
5. **Template literals** são preferíveis a concatenação de strings
6. **Destructuring** torna o código mais limpo
7. **Async/await** é mais legível que Promises encadeadas
8. **Métodos de array** (map, filter, reduce) são preferíveis a loops tradicionais
