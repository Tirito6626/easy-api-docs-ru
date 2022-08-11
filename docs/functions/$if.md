# $if
Отправляет жсон если условие верное.

### использование:
$if[условие;статус;{жсон}]
### пример:
```js
// http://localhost:port/route

$if[$getQuery[text]==undefined;400;{
    "status": 400,
    "means": "Bad request.",
    "text": "Missing query parameter 'text'."
}]
```
