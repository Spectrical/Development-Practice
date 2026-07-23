# JavaScript Course Notes

Personal notes from a JavaScript fundamentals course (freeCodeCamp-style curriculum).

**Video checkpoints (total length 3:28:42):**
- 1:33:40
- 2:33:30
- 2:47:28
- 2:55:32
- 3:07:19

---

## Table of Contents

1. [Variables & Basic Types](#1-variables--basic-types)
2. [Numbers & Operators](#2-numbers--operators)
3. [Strings](#3-strings)
4. [Arrays](#4-arrays)
5. [Functions & Scope](#5-functions--scope)
6. [Comparison & Logical Operators](#6-comparison--logical-operators)
7. [Control Flow](#7-control-flow)
8. [Objects](#8-objects)
9. [Loops](#9-loops)
10. [Practical Exercises](#10-practical-exercises)
11. [Useful Built-ins](#11-useful-built-ins)
12. [ES6+: let, const & Immutability](#12-es6-let-const--immutability)
13. [Arrow Functions](#13-arrow-functions)
14. [Rest & Spread Operators](#14-rest--spread-operators)
15. [Destructuring Assignment](#15-destructuring-assignment)
16. [Template Literals](#16-template-literals)
17. [Concise Object/Function Syntax](#17-concise-objectfunction-syntax)
18. [Classes, Getters & Setters](#18-classes-getters--setters)
19. [Modules: import/export](#19-modules-importexport)
20. [Data Types Summary](#20-data-types-summary)

---

## 1. Variables & Basic Types

- **Part 1:** Assigning variables
- **Part 2:** Initializing variables w/ assignment operator
- **Part 3:** Uninitialized variables
- **Part 4:** Case sensitivity in variable names

## 2. Numbers & Operators

- **Part 5:** Adding, subtracting, multiplying, dividing numbers; incrementing (`++`) / decrementing (`--`); decimals (float); multiplying/dividing decimals; finding a remainder (`%`)
- **Part 6:** Compound assignment with augmented addition/subtraction (`+=`, `-=`)

## 3. Strings

- **Part 7:** Escape characters in strings (`\`, `'`, `` ` ``)
- **Part 8:** Escape sequences:
  - `\'` `\"` `\\`
  - `\n` newline
  - `\r` carriage return
  - `\t` tab
  - `\b` backspace
  - `\f` form feed
- **Part 9:** Concatenating strings with `+` and `+=`
  ```js
  var a = "I come first.";
  a += "I come second";
  ```
- **Part 10:** Construct strings with variables
- **Part 11:** Appending variables to strings
- **Part 12:** String length — `test.length`
- **Part 13:** Bracket notation for first character — `test[0]`
- **Part 14:** String immutability (string literals can't be changed)
- **Part 15:** Bracket notation for Nth character — `test[n]`
- **Part 16:** Last letter — `test[test.length - 1]`
- **Part 17:** Word Blanks — `function(..,..,..) { return }`

## 4. Arrays

- **Part 18:** Store multiple values with arrays — `array = [23, "qwen"]`
- **Part 19:** Multi-dimensional array — `multi = [[], []]`
- **Part 20:** Access array data with indexes
- **Part 21:** Modify array data with indexes
- **Part 22:** Access multi-dimensional array with indexes
- **Part 23:** Manipulate arrays with `push()`
  ```js
  var theArray = [[67, 25, 37], [780, 267, 188]];
  theArray.push(["Jason", "Queen"]);
  var theData = theArray[2][1];
  ```
- **Part 24:** Remove last element — `pop()`
- **Part 25:** Remove first element — `shift()`
- **Part 26:** Add element to the front — `unshift()`
- **Part 27:** Shopping list exercise using multi-dimensional arrays

## 5. Functions & Scope

- **Part 28:** Write reusable code with functions
- **Part 29:** Passing values with arguments
- **Part 30:** Global scope (Scrimba enforces `var` for global scope, excluding non-`var` globals)
- **Part 31:** Local scope
- **Part 32:** Return a value with `return`
- **Part 33:** Assignment with a return value
- **Part 34:** "Stand in Line" exercise

## 6. Comparison & Logical Operators

- **Part 35:** Strict equality `===` (not `==`)
  ```
  3 == 3     ✓
  3 == '3'   ✓
  3 === 3    ✓
  3 === '3'  ✗
  ```
- **Part 36:** Equality/inequality operator (`==` / `!=`)
- **Part 37:** Strict inequality operator `!==`
- **Part 38:** Comparison operators `>`, `<`, `<=`, `>=`
- **Part 39:** Logical AND (`&&`) and OR (`||`)

## 7. Control Flow

- **Part 40:** `else if` statements / chaining if-else
- **Part 41:** Switch statements
  ```js
  var test = "";
  switch (test) {
    case 1:
      break;
    case 2:
  }
  ```
- **Part 42:** Returning true/false from functions
- **Part 43:** Early return pattern
- **Part 44:** "Counting Cards" exercise

## 8. Objects

- **Part 45:** Build JavaScript objects (properties instead of indexes)
  ```js
  var ourDog = {
    "name": "camp",
    "legs": 4,
    "friends": ["everything"]
  };
  ```
- **Part 46:** Dot notation — `ourDog.name`
- **Part 47:** Bracket notation (required for property names with spaces)
  ```js
  ourDog["the name"];
  ```
- **Part 48:** Accessing object properties using variables
- **Part 49:** Add new properties — `test.bark = woof;` / `test['bark'] = woof;`
- **Part 50:** Delete a property — `delete test.bark;`
- **Part 51:** Object as a dictionary (switch-like lookup)
- **Part 52:** Testing objects for properties with `hasOwnProperty`
  ```js
  var myObj = { gift: "pony", pet: "kitten" };

  function checkObj(checkProp) {
    if (myObj.hasOwnProperty(checkProp)) {
      return myObj[checkProp];
    } else {
      return "Not Found";
    }
  }
  ```
- **Part 53:** Manipulating complex (nested) objects — music library example
- **Part 54:** Accessing nested objects with `{}`
  ```js
  var gloveBoxContents = myStorage.car.inside["glove box"];
  ```
- **Part 55:** Accessing nested arrays with `[]`
  ```js
  var findMyItem = myPlantsStorage[1].list[1];
  ```

## 9. Loops

- **Part 57:** Iterate with loops (`while`, `for`)
- **Part 58:** Iterate odd numbers with `for`
- **Part 59:** Count backwards with `for`
- **Part 60:** Nested `for` loops
- **Part 61:** Iterate with `do...while` loops

## 10. Practical Exercises

- **Part 56:** Record Collection — update a nested object collection
  ```js
  function updateRecords(id, prop, value) {
    if (value === "") {
      delete collection[id][prop];
    } else if (prop === "tracks") {
      collection[id][prop] = collection[id][prop] || [];
      collection[id][prop].push(value);
    } else {
      collection[id][prop] = value;
    }
    return collection;
  }
  ```
- **Part 62:** Profile Lookup — search array of contact objects
  ```js
  function lookupProfile(name, prop) {
    for (var i = 0; i < contacts.length; i++) {
      if (contacts[i].firstName === name) {
        return contacts[i][prop] || "Can't find the property you are looking for.";
      }
    }
    return "No contacts found.";
  }
  ```

## 11. Useful Built-ins

- **Part 63:** Generate random fractions/numbers — `Math.random()`, `Math.floor()`
- **Part 64:** `parseInt()` — string to integer
- **Part 65:** `parseInt()` with a radix (e.g. base 2 for binary)
- **Part 66:** Ternary operator `?:`
  ```js
  function checkSign(num) {
    return num > 0 ? "positive" : num < 0 ? "negative" : "zero";
  }
  ```

## 12. ES6+: let, const & Immutability

- **Part 67:** `var` vs `let` (introduced 2015; `let` prevents redeclaration)
- **Part 68:** Comparing scope of `var` vs `let`
- **Part 69:** Read-only variables with `const`
- **Part 70:** Mutating array contents declared with `const` (array itself is mutable, reference is not)
- **Part 71:** Preventing object mutation with `Object.freeze()`

## 13. Arrow Functions

- **Part 72:** Concise anonymous functions
  ```js
  var magic = () => new Date();
  var greet = () => console.log("HELLO WORLD");
  ```
- **Part 73:** Arrow functions with parameters
  ```js
  var myConcat = (arr1, arr2) => arr1.concat(arr2);
  ```
- **Part 74:** Higher order arrow functions (e.g. with `filter`)
- **Part 75:** Default parameters & IIFE (Immediately Invoked Function Expression)
  ```js
  const increment = (function() {
    return function increment(number, value = 1) {
      return number + value;
    };
  })();
  ```

## 14. Rest & Spread Operators

- **Part 76:** Rest operator (`...args`) with `reduce()`
  ```js
  const sum = (function() {
    return function sum(...args) {
      return args.reduce((a, b) => a + b, 0);
    };
  })();
  ```
- **Part 77:** Spread operator to evaluate arrays in-place
  ```js
  arr2 = [...arr1]; // expands/copies array
  ```

## 15. Destructuring Assignment

- **Part 78:** Assign variables from objects
  ```js
  const { x: a, y: b, z: c } = voxel;
  ```
- **Part 79:** Destructuring with nested objects
  ```js
  const { tomorrow: { max: maxOfTomorrow } } = forecast;
  ```
- **Part 80:** Destructuring assignment from arrays (with skipped values)
  ```js
  const [z, x, , y] = [1, 2, 3, 4, 5, 6];
  ```
- **Part 81:** Destructuring with the rest operator
  ```js
  function removeFirstTwo(list) {
    const [, , ...arr] = list;
    return arr;
  }
  ```
- **Part 82:** Destructuring an object directly as a function parameter
  ```js
  const half = function half({ max, min }) {
    return (max + min) / 2.0;
  };
  ```

## 16. Template Literals

- **Part 83:** Template literals with backticks — multi-line strings and `${}` interpolation
  ```js
  const greeting = `Hello, my name is ${person.name}!
  I am ${person.age} years old.`;
  ```

## 17. Concise Object/Function Syntax

- **Part 84:** Concise object literal declarations (shorthand properties)
  ```js
  const createPerson = (name, age, gender) => ({ name, age, gender });
  ```
- **Part 85:** Concise method declarations
  ```js
  const bicycle = {
    gear: 2,
    setGear(newGear) {
      this.gear = newGear;
    }
  };
  ```

## 18. Classes, Getters & Setters

- **Part 86:** `class` syntax as a substitute for constructor functions
  ```js
  class SpaceShuttle {
    constructor(targetPlanet) {
      this.targetPlanet = targetPlanet;
    }
  }
  var zeus = new SpaceShuttle('Jupiter');
  ```
- **Part 87:** Getters and setters to control access
  ```js
  class Thermostat {
    constructor(temp) {
      this._temp = 5 / 9 * (temp - 32);
    }
    get temperature() {
      return this._temp;
    }
    set temperature(updatedTemp) {
      this._temp = updatedTemp;
    }
  }
  ```

## 19. Modules: import/export

- **Part 88:** Differences between `import` and `require`
- **Part 89:** `export` to reuse a code block
  ```js
  export const capitalizeString = str => str.toUpperCase();
  ```
- **Part 90:** Import everything from a file with `*`
  ```js
  import * as capitalizeStrings from "capitalize_strings";
  ```
- **Part 91:** `export default` as a fallback export
  ```js
  export default function subtract(x, y) { return x - y; }
  ```

## 20. Data Types Summary

| Type | Description |
|---|---|
| `undefined` | Hasn't been set to anything yet |
| `null` | Represents "nothing" |
| `boolean` | `true` / `false` |
| `string` | Text data |
| `symbol` | Immutable primitive value that is unique |
| `number` | Numeric data |
| `object` | Stores key-value pairs |

**Variables:** Can be reassigned to other data types later (when declared with `var` or `let`).
