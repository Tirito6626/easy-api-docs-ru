# $getRoute
Получает значение путя

### Использование:
```
$getRoute[опция]

**Пример эндпоинта:**
```js
module.exports = {
    path: '/myendpoint',
    details: {
        description: 'Это описание лол',
        usage: '?text=String'
    },
    code: `...`
}
```

### Example:
```js
$getRoute[/myendpoint;path] // /myendpoint
$getRoute[/myendpoint;details.description] // Это описание лрл
$getRoute[/myendpoint;details.usage] // ?text=String
```
