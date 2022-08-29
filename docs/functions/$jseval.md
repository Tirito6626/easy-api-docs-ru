# $jsEval
использует javascript код.

### использование:
```js
$jsEval[возвращать?;код]
```
### пример:
```js
$jsEval[true;
const hi = "Hello world"
hi
] // return: Hello world
$jsEval[false;
const hi = "Hello world"
hi
] // return: 
```
