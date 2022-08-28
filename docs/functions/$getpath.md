# $getPath
Получает параметр путя.

### Использование:
```
$getPath[параметр]
```

### Пример:
```js
module.exports = {
    path: '/users/:id',
    code: `
    $send[200;json;{
        text: 'Айди: $getPath[id]'
    }]
    `
}
```
