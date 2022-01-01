# ES 6 javascript

The 6th edition, ECMAScript 6 (ES6) and later renamed to ECMAScript 2015, was finalised in June 2015. [\*](https://en.wikipedia.org/wiki/ECMAScript)

It introduces many changes to the language described below.

## let and const keywords

`let` and `const` replace `var`.

## for of loop

```js
const letters = ["a", "b", "c", "d", "e", "f"];

for (let letter of letters) {
    console.log(letter);
}
```

## template literals

Template literals provide an easy and clean way create multi-line strings and perform string interpolation.

```js
const a = 10;
const b = 20;

const result = `The sum of ${a} and ${b} is ${a+b}.`;

const multiLine = `This is a
    multiline string`;
```

## function argument default value

```js
function sayHello(name="World") {
    return `Hello ${name}!`;
}
```

## arrow functions

```js
const multiply = (arg1, arg2) => {
    return arg1 * arg2;
}

// simplified
const multiply = (arg1, arg2) => arg1 * arg2;
```

## classes

```js
class Person {
    constructor(name) {
        this.name = name;
    }

    hello = () => {
        console.log(this.name);
    }
}
```

## Promises

Promises are JavaScript's way to execute asynchronous code.

```js
const myFirstPromise = new Promise((resolve, reject) => {
    ...
});
```

## modules, import and export

```js
// default export = unamed export
export default (weight, height) => weight / (height * height);

// named exports
export const four = 4;

export const bmi = (weight, height) => weight / (height * height);

// default import
import bmiDefault from "./js/module.js";

// named imports
import {four} from "./js/module.js";
import {bmi} from "./js/module.js";

import {four as five} from "./js/module.js";

// import all named exports
import * as mod from "./js/module.js";
```

## spread and rest operator

`...`

```js
let myArray = [1,2,3];
let newArray = [...myArray, 4, 5, 6];

// shallow clone object
let myObject = {
    name: "8ctopus",
    color: "variable",
};

//
let shallowClone = {
    ...myObject,
};

shallowClone.name = "test";

// turn function arguments into array
const log = (...args) => {
    args.forEach((num) => console.log(num));
};
```

## destructuring

```js
// destructure array
const array = [1, 2, 3, 4, 5];

const [, , third, fourth] = array;
console.log("third, fourth", third, fourth);

// destructure object
const octopus = {
    name: "8ctopus",
    color: "variable",
    age: 5,
    vision: good,
}

const {color, age} = octopus;
console.log(color, age);
```

## variables copy vs. reference

Primitive types are copied, while `Array` and `Object` are a reference to the original object.
