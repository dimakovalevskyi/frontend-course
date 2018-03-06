# Some code examples for checking your skills

```
var a = 3;
var b = 6;
var c = 8;
//---------
var a = 3,
    b = 6,
    c = 8;
//---------
var a;
var b;
var c;

a = 3;
b = 6;
c = 8;
```

```
var human = {
    firstName: 'John',
    secondName: 'Smith',
    age: 21,
    sex: 'male',
    isProgrammer: false
};
```

```
var a = {
    n: 1,
    s: 'string',
    f: function(argument) {
        return argument * 2;
    },
    b: true,
    o: {
      n: 1
    },
    'some-strange-name': 'this property has strange name, we need to take this in quot',
    'some-strange-name-2': {
        gg: 'wp'
    },
    'some-strange-name-3: function() {
        return 'Do you still understand ?';
    }
};

a;
a.n;
a.f();
a.o.n;
a['some-strange-name'];
a['some-strange-name-2'].gg;
a['some-strange-name-3']();
```

```
var a = function() {
    return {
       b: function() {
          return 'Hello';
       }
    };
};

a;
a();
a().b;
a().b();
```

```
var a = function() {
    return 'Text';
};

a;
a();
```

```
var a = function() {
    return function() {
      return 'Text';
    };
};

console.log(a);
console.log(a());
console.log(a()());
```
