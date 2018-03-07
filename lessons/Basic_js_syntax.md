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

## Types, typeof

  * `number` - any number: `1`, `-11`, `1.3486`, `Infinity`, `NaN`
  * `string` - line: `"Hello, world"`, `""`, `"123"`
  * `boolean` - logic type: `true` or `false`
  * `null` - it's nothing, bitch: `null`
  * `undefined` - it's nothing, for now: `undefined`
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

## Arrays

```
var a = [];

a.push(1);
a.push(2);
a.push(3);

a; // [1, 2, 3]
a[0]; // 1
a[2]; // 3
```

## Objects

```
var a = {};

a.a = 1;
a.b = 2;

a; // {a: 1, b: 2}

delete a.b;

a; // {a: 1}
```

## Basic Operators

 * `+` / `-` / `/` / `*` / `%` - math operators
 * `+` - string concatenation
 * `++` / `--` - increment/decrement
 * `+=` / `-=` / `/=` / `*=` / `%=` short math operators

## Boolean Operators
 
 * `>` / `<` / `>=` / `<=`/ `==` / `!=` / `===` / `!==` - comparison operators
 * `&&` / `||` - logical operators
 
## Types comparison
 
```
alert( '2' > 1 ); // true
alert( '01' == 1 ); // true
alert( false == 0 ); // true
alert( true == 1 ); // true
```

## If ... else

```
var a = 3, b = 1;

if (a > b) {
    alert('1 is more than 2');
}

a = 1;
b = 3;

if (a > b) {
    alert('a is more than b');
} else {
    alert('a is not more than b');
}

a = 3;
b = 3;

if (a > b) {
    alert('a is more than b');
} else if (a < b) {
    alert('b is more then b');
} else {
    alert('a and b are equal');
}
```

## Functions

```
function sayHi() {
  alert( "Hi!" );
}

sayHi(); // Hi!
```

```
function sayHi(name) {
  alert( 'Hi, ' + name + '!' );
}

sayHi('Bitch'); // Hi, Bitch!
```

```
function getSumm(a, b) {
  return a + b;
}

alert(getSumm(1, 3)); // 3
```

## Loops

```
var str = "";

for (var i = 0; i < 9; i++) {
  str = str + i;
}

console.log(str);
// expected output: "012345678"
```

## Code example (authorization, max value in array)

## Homework

Create function, which will calculate x1 and x2 for Quadratic equation

```
function calculate(a, b, c) {
    var x1, x2;

    // write this code

    alert('Calculated: x1=' + x1 + '; x2=' + x2);
}
```
