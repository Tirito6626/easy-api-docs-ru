# $deleteObjectKey
Удаляет ключ из созданного объекта.

### Использование:
```
$deleteObjectKey[имя ключа]
```

### Пример:
```js
$deleteObjectKey[hello] // удалит этот ключ из объекта, Итог: { start: 'hiii' }
$setObjectKey[hello;hi]
$setObjectKey[start;hiii]
$createObject
```
