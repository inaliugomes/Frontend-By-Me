
# 📘 Notas de JavaScript

## 🔹 Scope

> Scope é simplesmente um "mundo" delimitado por `{ }`.  
Variáveis declaradas dentro de um **escopo** (como uma função ou bloco) **existem apenas ali dentro** e **não são acessíveis fora dele**.

- Variáveis de **escopo local** existem apenas dentro do bloco onde foram declaradas.
- Variáveis **globais** podem ser acessadas de **qualquer lugar**, inclusive **dentro de blocos** `{ }`.

```js
let globalVar = "sou global";

function exemplo() {
  let localVar = "sou local";
  console.log(globalVar); // funciona
  console.log(localVar);  // funciona
}

console.log(globalVar); // funciona
console.log(localVar);  // ERRO: localVar não está definida
```

---

## 🔹 IIFE (Immediately Invoked Function Expression)

IIFE permite criar **funções que se executam automaticamente** assim que são definidas.

```js
(function () {
  console.log("Executou imediatamente!");
})();
```

> Útil para evitar poluir o escopo global e criar módulos autoexecutáveis.

---

## 🔹 Hoisting

O **Hoisting** é o comportamento do JavaScript de **"levantar" declarações para o topo do escopo**, antes da execução do código.

```js
console.log(a); // undefined
var a = 5;
```

- Variáveis `var` são içadas com valor `undefined`.
- Funções declaradas com `function` são içadas **completamente** (podem ser chamadas antes da declaração).
- `let` e `const` **não são içadas da mesma forma** — causam erro se usadas antes da declaração.

---

## 🔹 Currying

Currying é uma técnica onde uma função **retorna outra função**, permitindo **passar argumentos em etapas**.

```js
function soma(a) {
  return function (b) {
    return a + b;
  };
}

console.log(soma(2)(3)); // 5
```

> Isso permite criar **funções especializadas e reutilizáveis**.

---

## 🔹 `call`, `apply`, `bind`

São métodos usados para **controlar o `this`** em funções:

- **`call`**: chama uma função com um contexto (`this`) e argumentos separados.
- **`apply`**: igual ao `call`, mas os argumentos são passados como array.
- **`bind`**: não executa a função de imediato, mas retorna uma nova função com `this` fixo.

```js
function saudacao(saudacao) {
  console.log(`${saudacao}, meu nome é ${this.nome}`);
}

const pessoa = { nome: "Ana" };

saudacao.call(pessoa, "Olá");           // Olá, meu nome é Ana
saudacao.apply(pessoa, ["Oi"]);         // Oi, meu nome é Ana
const f = saudacao.bind(pessoa, "Hey");
f();                                    // Hey, meu nome é Ana
```
