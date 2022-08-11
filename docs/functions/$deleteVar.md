# $deleteVar
Удаляет переменную из датабазы.

### Использование:
```
$deleteVar[имя переменной]
```

### Пример:
```js
$getVar[hi] // неизвестно 
$deleteVar[hi]
$getVar[hi] // ok
$setVar[hi;ok]
```

> ⚠: Вам нужно установить датабазу для использования этой функции. Посмотрите [tips](tips.md?id=using-database)
