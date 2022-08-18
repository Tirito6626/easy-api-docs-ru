# $timeout
Устанавливает максимальное время ожидания для роута "route" и JSON ответа.

### Использование:
```
$timeout[количество милисекунд;статус;ответ JSON]
```

### Пример:
```js
$send[wrong fields] // Это выдаст ошибку

//Через 30 секунд оно выдаст ошибку
$timeout[$parseTime[30s];500;{
    "error": "Something internal went wrong"
}]
```

!> Посмотрите как использовать **$parseTime** нажав: [here](functions/$parseTime.md)
