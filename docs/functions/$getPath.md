# $getPath
Получает параметр путя.

### Использование:
```
$getPath[параметр]
```

### Example:
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
