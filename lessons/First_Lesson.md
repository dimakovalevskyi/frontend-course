# First Lesson

---

## What is JS, why was it invented ?

JavaScript, is a high-level, dynamic, weakly typed, prototype-based, multi-paradigm, and interpreted programming language.

## JS evolution.

* JS when it was used as intended
* jQuery
* SPA
* Backend
* Mobile, Desktop O_o

## JS versions.

* ECMAScript 1
* ECMAScript 2
* ECMAScript 3
* ECMAScript 5 (ES5) (2009)
* ECMAScript 6 (ES6)/ ECMAScript 2015 (ES2015)
* ECMAScript 2016 (ES7)
* ECMAScript Proposals

## JS today.

* SPA (React, Angular, Vue)
* Backend (Node.js)
* Mobile (React Native)
* Desktop (Electron)

## How js works in browser.

### How to add js in your page.

Script in `script` tag.
```
<script>
  alert(1);
</script>
```

Script in external file.
```
<script src="/path/to/script.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/lodash.js/4.3.0/lodash.js"></script>
```

```
<script src="file.js">
  alert(1); // ignored
</script>
```

### How js code will be executed.

```
<html>
<head>
  <script src="big.js"></script>
</head>
<body>
  This text will not be displayed until the browser execute big.js.
</body>
</html>
```

Save Our ~Souls~ information.

`async/defer` attributes.

```
<script src="1.js" async></script>
<script src="2.js" async></script>
```

```
<script src="1.js" defer></script>
<script src="2.js" defer></script>
```
