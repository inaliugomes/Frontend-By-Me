#  📘 Novas de JavaScript

## Spread 

O operador spread e usado para espalhar os elementos de um array ou as propriedades de um objeto em outro lugar 

#### Pode ser usado para:
- clonar arrays ou objetos 
- Combinar arrays 
- Passar elementos como argumentos 

```js
const arr1 = [1,2];
const arr2 = [...arr1,3,4]//1,2,3,4

const obj1 = {a:1}
const obj2 = {...obj1,b:2}

console.log(obj2)//{a:1 , b:2}

```

## Rest(...)

O rest operator agrupa os argumentos restantes de uma função ou os valores restantes de um array/objeto em uma nova variável

Permite também criar funções que podem receber vários parâmetros, bastante bom quando não sabemos parâmetros vai ser preciso o utilizador passar. 

```js
//Desta forma podemos passar vários argumentos na minha função soma()
function soma(...numeros) {
  return numeros.reduce((a, b) => a + b, 0);
}

const [a, ...resto] = [1, 2, 3]; // a = 1, resto = [2, 3]

```

## Destructuring

**Destructuring** e a capacidade de "desconstruir" um array ou um objeto em ordem que seja possível  utilizar os valores da sua propriedade de forma isolada e desta forma não preciso de escrever, por exemplo, **Objeto.propriedade** ou, por exemplo, escrever 
**array[0]**

```js
const pessoa = { nome: "Ana", idade: 28 };
const { nome, idade } = pessoa;

const numeros = [10, 20];
const [x, y] = numeros;

```


## Import e Export 

Ambos nos permite criar modelos e classes reutilizáveis:

- Import: Permite importar uma função ou módulos para reutilizar um código 

- Export: Nos permite criar funções que podemos dizer que os meus podem ser utilizado em outros ficheiros ou classes.

```js

// utils.mjs
export function saudacao() {
  return "Olá!";
}

// app.mjs
import { saudacao } from './utils.mjs';


```

## Módulos 

Um módulo é um arquivo de código isolado que pode exportar e importar variáveis, funções, classes etc.

- Permite melhor organização, reutilização e manutenção do código.

- Em ambientes modernos, usamos extensões como .js ou .mjs.




