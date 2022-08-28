# $deleteObjectKey
Удаляет ключ из созданного объекта 

### Использование:
```
$deleteObjectKey[имя ключей]
```

### Пример:
```js
$deleteObjectKey[hello] // удалит этот ключ из объекта, Итог: { start: 'hiii' }
$createObject[{
"hello":"hi",
"start":"hiii"
}]
```
