# Basic JS Syntax

---

## Variables

```
// var (es5)
var a = 'Hello';
var b = 1, c = 0, d;

// const, let (es6)
const A = 'Hello';
let b = 1, c = d = 0, e;
```

## Duck typing, types, typeof

  * `number` - any number: `1`, `-11`, `1.3486`, `Infinity`, `NaN`
  * `string` - line: `"Hello, world"`, `""`, `"123"`
  * `boolean` - logic type: `true` or `false`
  * `null` - it`s nothing, bitch: `null`
  * `undefined` - it`s nothing, for now: `undefined`
  * `object` - magic type: `{}`, `{a: 1, b: 'Moto'}`
  
 ```
typeof undefined // "undefined"
typeof 0 // "number"
typeof true // "boolean"
typeof "foo" // "string"
typeof {} // "object"
typeof null // "object"  (1)
typeof function(){} // "function"  (2)
```
## Basic Operators
