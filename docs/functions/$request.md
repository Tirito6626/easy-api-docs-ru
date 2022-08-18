# $request

Производит http запрос.

### Использование:
```
$request[ссылка;конфиг(смотрите ниже)?;хэадеры?]
```
### Пример конфига:
```json
{
    method: string, // метод запроса (GET/POST)
    logError?: boolean, // если в консоли будет ошибка
    data?: any // Дата (Для POST запросов)
}
```

### Пример:

```js
// GET метод:
$request[https://api.miduwu.ga/json/calendar]

// POST метод:
$request[https://anylink;{
    method: 'POST',
    data: 'любой текст для запроса, может быть так-же json'
}]

// POST метод (с хэадерами) 
$request[https://anylink;{
    method: 'POST',
    data: 'anything'
};headerName:headerValue;headerName2:headerValue2]
```
> 💡: Вы можете использовать [**`$getData`**](/functions/$getData.md) для вывода данных запроса

### TIP: Вы можете отправлять логи с дискорд вебхуками: Новый запрос!
```
$request[https://discord.com/api/v9/webhooks/:id/:token;{
    method: 'POST',
    data: { content: 'Новый запрос!', embeds: [{title: 'Новый запрос!', description: 'В /endpoint'}] },
    logError: true
}]
```
